# Bulma Darkify 🌗

Add a touch of darkness to your Bulma-powered websites. This project allows you to embrace the dark side of web design while maintaining the sleekness of Bulma's UI framework. Say goodbye to bright lights and welcome the relaxing warmth of dark mode.

## Features

- Fully customizable dark mode support.
- Ability to toggle between light and dark modes using the `[data-theme]` attribute.
- Compatibile with your existing Bulma styles.

## Getting Started

### Installation
```bash
pnpm add -D bulma-darkify
```

or

```bash
npm install bulma-darkify --save-dev
```

or

```bash
yarn add -D bulma-darkify
```

### Import

#### Full Import (Larger Bundle Size)
Include the provided SCSS file into your existing SASS/SCSS file:
```scss
@import "bulma/bulma";

// Import your own dark mode variables
@import "your-dark-mode-variables";
@import "bulma-darkify/bulma-darkify";
```

#### Modular Import (Smaller Bundle Size)
Include only the SCSS files that you need:
```scss
// Import the relevant Bulma files before importing from bulma-darkify
@import "bulma/sass/utilities/_all";
@import "bulma/sass/elements/button";

// Import your own dark mode variables
@import "your-dark-mode-variables";

// Import from bulma-darkify
@import "bulma-darkify/scss/utilities/_all";
@include color-mode(dark) {
    @import "bulma-darkify/scss/elements/button";
}
```

### Use
To use the dark mode, add the `data-theme` attribute to your HTML tag. For example:
```html
<html lang="en" data-theme="dark">

</html>
```

### Toggle
To toggle between themes, simply change this attribute to `light`:
```html
<html lang="en" data-theme="light">

</html>
```

### Customization
This library does not come with predefined styles for dark mode. This means that you will need to define how you want the dark mode styles to appear. To do this, follow Bulma's guide on customization using SASS variables: https://bulma.io/documentation/customize/variables/.

Then, append your style names with `-dark`.

For example, to change a button's default background color in light mode, you would normally define a variable like:
```scss
$button-background-color: #YOUR-COLOR-HERE
```

For dark mode, you can change the button's background color by simply adding `-dark` to this variable name:
```scss
$button-background-color-dark: #YOUR-COLOR-HERE
```

## Contributing

Contributions from the community are welcomed! If you encounter a bug, have a feature request, or want to enhance this library, please open a [pull request](https://github.com/aggarwal-h/bulma-darkify/pulls)

## License

This project is under the [MIT](LICENSE) license. Feel free to use, modify, and distribute it as you please.

---
