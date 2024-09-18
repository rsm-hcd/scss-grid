# Scss-Grid (RSM HCD)

## Getting Started

```shell
#npm
npm install --save-dev @rsm-hcd/scss-grid

# yarn
yarn add @rsm-hcd/scss-grid --dev
```

```scss
@import @rsm-hcd/scss-grid;
```

## Usage

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

### Development

```shell
npm install
npm run watch # automatically builds as changes are made
```

### Documentation

[Full documentation](https://andculturecode.github.io/AndcultureCode.Scss.Grid/docs)

## Contributing

Information on contributing to this repo is in the [Contributing Guide](CONTRIBUTING.md)
