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



# Contributing

Information on contributing to this repo is in the [Contributing Guide](https://github.com/AndcultureCode/AndcultureCode/blob/master/CONTRIBUTING.md).