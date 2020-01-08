Setting up a new repository
======

Below is a quick checklist to use a guide when setting up a new repository to share on github for use publically.

Note: This differs from our setup of repositories privately for our clients.

* Create new repository on andcultureCode github account using established naming conventions
    ```csharp
        AndcultureCode.{LanguageName}.{PackageName}.{ChildPackageName}
        // ex. AndcultureCode.CSharp.Extensions

        AndcultureCode.{LanguageName}.{PopularPackageName}
        // ex. AndcultureCode.CSharp.FactoryGirl
    ```
* Configure the correct contributers from the development team
* Add relevent topics and description
* Unless otherwise specified: Select Apache 2.0 license
* Add default `CONTRIBUTING.md` document that links to this repository
    ```
    How to Contribute
    ======
    Information on contributing to this repo is in the [Contributing Guide](https://github.com/
    AndcultureCode/AndcultureCode/blob/master/CONTRIBUTING.md) in the Home repo.
    ```
* Setup project specific `.gitignore`
    * Dotnet C# projects: [VisualStudio.gitignore](https://github.com/github/gitignore/blob/master/VisualStudio.gitignore)
* Regardless of technology, please ensure the following...
    * Clear and concise setup and baseline usage guidelines in top-level README
    * Automated test projects setup
    * Continuous integration builds configured (See [Travis CI](https://travis-ci.org))


## Setting up Travis CI
See [Travis Tutorial](https://docs.travis-ci.com/user/tutorial/)

* Log into Travis CI organization account (github auth)
* Ensure your repository is public
* Go to settings for project and select following options...
    * General
        * Build pushed branches: yes
        * Build pushed pull requests: yes
* Add `.travis.yml` to top-level of repository
    ```yaml
    dotnet: 2.2.1
    env:
      global:
        - DOTNET_CLI_TELEMETRY_OPTOUT: 1
    language: csharp
    mono: none
    script:
      - dotnet restore
      - dotnet test
    solution: All.sln
    ```
* After push of `.travis.yml` file, force build (if not already triggered) and debug.
* Add status image for job to top-level README
    ```markdown
    [![Build Status](https://travis-ci.org/AndcultureCode/AndcultureCode.CSharp.Extensions.svg?branch=master)](https://travis-ci.org/AndcultureCode/AndcultureCode.CSharp.Extensions)
    ```

### Further Travis Customizations
#### Code Coverage with Coverlet and CodeCov

Assumes you've updated your respective project `.csproj` files with the necessary coverlet tooling

* Log into [codecov.io](https://codecov.io) with github
* Configure for desired repository
* Copy generated key into password locker
* Update travis job settings with codecov `CODECOV_TOKEN` environment variable
* Update `.travis.yml` lines
    ```yaml
    after_script:
        - bash <(curl -s https://codecov.io/bash)
    script:
        - dotnet test -p:CollectCoverage=true -p:CoverletOutputFormat=opencover -p:Threshold=75
    ```
* Add codecov badge to project readme
    ```markdown
    [![codecov](https://codecov.io/gh/AndcultureCode/AndcultureCode.CSharp.Extensions/branch/master/graph/badge.svg)](https://codecov.io/gh/AndcultureCode/AndcultureCode.CSharp.Extensions)
    ```
* Push and test it out!


#### Add slack build notifications

* Log into management section of slack `https://{organization}.slack.com/apps/manage`
* Install/Update Travis CI app integration
* Click 'Add Configuration'
* Select your desired slack channel
* Copy the generated slack token for next steps
* Install travis cli client on your machine (if not already)
    * Ensure ruby 1.9.3+ is installed
    * `$: gem install travis --no-rdoc --no-ri`
* Use the travis cli to generate a secure token
    * Reference [travis documentation](https://docs.travis-ci.com/user/notifications/#configuring-slack-notifications) if you run into any issues
    * Change directory (cd) to your repository (where the `.travis.yml` is located)
    * `$: travis encrypt "{organization}:{slack-token}" --add notifications.slack`
    * This should automatically update the travis configuration with a secure token