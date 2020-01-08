# rhythm

A Sass (scss) based grid library inspired by bourbon neat and flexbox.

Written by Zach McCleaf.

Published by Dylan Justice.

# Getting Started

```bash
npm install andculturecode.scss.rhythm
```

```scss
@import andculturecode.scss.rhythm;
```

# Usage

```html
<div class="o-rhythm__container">
    <div class="o-rhythm__row -space-above"></div>
    <div class="o-rhythm__row -space-between"></div>
    <div class="o-rhythm__row -border-bottom"></div>
    <div class="o-rhythm__row">... More to come</div>
    <div class="o-rhythm__row">
        <div class="o-rhythm__col -span-one"></div>
        <div class="o-rhythm__col -span-two"></div>
        <div class="o-rhythm__col -span-twelve"></div>
    </div>
    <div class="o-rhythm__row">
        <div class="o-rhythm__col -push-one"></div>
        <div class="o-rhythm__col -push-eleven"></div>
    </div>
    <div class="o-rhythm__row">
        <div class="o-rhythm__col -span-one -y-align-top"></div>
        <div class="o-rhythm__col -span-one -y-align-center"></div>
        <div class="o-rhythm__col -span-one -y-align-bottom"></div>
        <div class="o-rhythm__col -span-one -justify-right"></div>
        <div class="o-rhythm__col -span-one -justify-center"></div>
    </div>
</div>
```


# AndcultureCode

We are the engineering team at andculture focused on developing technology solutions. Come build with us.

While we use a wide array of technologies at andculture, we tend to build primarily in .NET Core C# and React TypeScript. The goal of this repository is to document our engineering team best practices around specific technologies as well as the department at large.

<img src="https://avatars3.githubusercontent.com/u/32297579?s=460&v=4" alt="andCulture Logo" width="300" />


# Contributing

While we do a lot of work for private organizations, we strive to collaborate with the community as much as possible. We have a variety of repositories broken out by language and purpose.

Please browse our [github respositories](https://github.com/AndcultureCode?tab=repositories) using the following naming convention as a guide.

```csharp
AndcultureCode.{LanguageName}.{PackageName}.{ChildPackageName}
// ex. AndcultureCode.CSharp.Extensions

AndcultureCode.{LanguageName}.{PopularPackageName}
// ex. AndcultureCode.CSharp.FactoryGirl
```

Once you find a repository of interest, please give our [contributions guide](CONTRIBUTING.md) a read.