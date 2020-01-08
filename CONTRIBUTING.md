# How to contribute

One of the easiest ways to contribute is to participate in discussions on GitHub issues. You can also contribute by submitting pull requests with code changes.

### Pull Request Checklist
* Provide a clear description of the problem accompanied by your solution
* Descriptive comments
* Read code and try your best to follow established code conventions (ie. format, regions, etc...)
* Automated tests for new and/ or changed code paths
* Ensure Travis CI build related to your branch is passing

### Merging and Versioning
While any and everyone is free to create pull requests per the checklist above, the process of merging and publishing versions is limited to core contributors established by andculture engineering leadership.

For andculture itself, project technical leads and architects will have access to merge and publish versions. Addition of external (non-andculture) employees from the community will be assessed and added as core contributors upon merit on an ongoing basis.

#### Setting up your fork
Create a new fork on your own github account and clone that to your local development machine.

Add the source AndcultureCode repository as a new remote branch.

```bash
$: git remote add upstream git://github.com/AndcultureCode/AndcultureCode.{REPOSITORY_NAME}.git
$: git remote -v
```

From there you should regularly update `upstream/master` and merge into your branches

```bash
$: git fetch upstream
$: git checkout master
$: git merge upstream/master
```


## General feedback and discussions?
Start a discussion on the project's [repository issue tracker example](https://github.com/AndcultureCode/AndcultureCode.CSharp.Extensions/issues).

## Are you a core contributor preparing a release?
See our [release guide](RELEASES.md)