# AndcultureCode.Scss.Grid

[![Build Status](https://travis-ci.org/AndcultureCode/AndcultureCode.Scss.Grid.svg?branch=master)](https://travis-ci.org/AndcultureCode/AndcultureCode.Scss.Grid)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier) <!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-2-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

A Sass (scss) based grid library inspired by bourbon neat and flexbox.

Written by Zach McCleaf.

Published by Dylan Justice.

# Getting Started

```shell
#npm
npm install --save-dev andculturecode-scss-grid

# yarn
yarn add andculturecode-scss-grid --dev
```

```scss
@import andculturecode-scss-grid;
```

# Usage

```html
<div class="o-grid__container">
    <div class="o-grid__row -space-above"></div>
    <div class="o-grid__row -space-between"></div>
    <div class="o-grid__row -border-bottom"></div>
    <div class="o-grid__row">... More to come</div>
    <div class="o-grid__row">
        <div class="o-grid__col -span-one"></div>
        <div class="o-grid__col -span-two"></div>
        <div class="o-grid__col -span-twelve"></div>
    </div>
    <div class="o-grid__row">
        <div class="o-grid__col -push-one"></div>
        <div class="o-grid__col -push-eleven"></div>
    </div>
    <div class="o-grid__row">
        <div class="o-grid__col -span-one -y-align-top"></div>
        <div class="o-grid__col -span-one -y-align-center"></div>
        <div class="o-grid__col -span-one -y-align-bottom"></div>
        <div class="o-grid__col -span-one -justify-right"></div>
        <div class="o-grid__col -span-one -justify-center"></div>
    </div>
</div>
```

Add a Custom grid!

```scss
$my-custom-grid: (
        columns: 12,
        gutter: 20px
    )
    .c-row-of-stuff {
    &__column {
        @include span-col(8, $my-custom-grid);
    }
}
```

Add your own breakpoints

```scss
$breakpoints: (
        "phone": 480px,
        "tablet": 768px,
        "desktop": 1180px
    )
    .c-row-of-stuff {
    &__column {
        @include span-col(8, $my-custom-grid);

        @include respond-to("phone") {
            @include span-col(12, $my-custom-grid);
        }
    }
}
```

## Development

```shell
npm install
npm run watch # automatically builds as changes are made
```

## Documentation

[Full documentation](https://andculturecode.github.io/AndcultureCode.Scss.Grid/docs)

# Contributing

Information on contributing to this repo is in the [Contributing Guide](CONTRIBUTING.md)

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="http://resume.dylanjustice.com"><img src="https://avatars.githubusercontent.com/u/22502365?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Dylan Justice</b></sub></a><br /><a href="https://github.com/AndcultureCode/AndcultureCode.Scss.Grid/commits?author=dylanjustice" title="Code">💻</a> <a href="https://github.com/AndcultureCode/AndcultureCode.Scss.Grid/commits?author=dylanjustice" title="Documentation">📖</a></td>
    <td align="center"><a href="http://www.winton.me/"><img src="https://avatars.githubusercontent.com/u/48424?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Winton DeShong</b></sub></a><br /><a href="https://github.com/AndcultureCode/AndcultureCode.Scss.Grid/commits?author=wintondeshong" title="Code">💻</a> <a href="https://github.com/AndcultureCode/AndcultureCode.Scss.Grid/commits?author=wintondeshong" title="Documentation">📖</a> <a href="#maintenance-wintondeshong" title="Maintenance">🚧</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
