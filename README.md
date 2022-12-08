[📖 Shopify GitHub integration](https://shopify.dev/themes/tools/github)

## Features

- Abstracting Shopify CLI command
- Bundle files with webpack
- Transpile SCSS to CSS with dart-sass
- Lint TS files with ESLint
- Lint SCSS files with Stylelint
- Format code with prettier
- Built-in test runner with Jest and Playwright
- Creating SVG sprites

## Requirements

- [Node v16+](https://nodejs.org/en/)
- [Shopify CLI v3.22.1+](https://shopify.dev/themes/tools/cli)

Note: Please refer to [Install Shopify CLI](https://shopify.dev/themes/tools/cli/installation) if you haven't installed Shopify CLI yet.

[📖 Upgrade or uninstall Shopify CLI](https://shopify.dev/themes/tools/cli/upgrade-uninstall)
## Main dependencies

- [Shopify CLI](https://shopify.dev/themes/tools/cli)
- [npm](https://www.npmjs.com/)
- [Webpack](https://webpack.js.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [Sass](https://sass-lang.com/)
- [ESLint](https://eslint.org/)
- [Stylelint](https://stylelint.io/)
- [Prettier](https://prettier.io/)
- [Jest](https://jestjs.io/)
- [Playwright](https://playwright.dev/)

## How to use

Clone this repository and install dependencies.

```bash
npm install
```

### Create a new theme

Use `newTheme` command to create a new theme from scratch. This command creates a copy of Dawn.

```bash
npm run newTheme
```

[📖 Theme commands - init](https://shopify.dev/themes/tools/cli/theme-commands#init)

### Customize an existing theme

Use `pull:new` command to customize an existing theme.

```bash
npm run pull:new
```

### Add CSS and JavaScript into your theme files

Add these tags in `<head></head>` section.

```liquid
{{ 'style.css' | asset_url | stylesheet_tag }}
```

```liquid
<script src="{{ 'main.js' | asset_url }}" defer></script>
```

## Available Commands

Recommend you to check out these commands before you get started.

### Start command

Start your project in development mode.

```bash
npm run start
```

### Build command

Build your project for production.

```bash
npm run build
```

Build your project for development.

```bash
npm run build:dev
```

<details>
<summary>Other support commands</summary>

### Pull command

Retrieve theme files from Shopify without deleting local files.

```bash
npm run pull
```

### Push command

Upload your local theme files to Shopify without deleting remote files.

```bash
npm run push
```

Push to your development theme. If you don't have a development theme, then one is created.

```bash
npm run push:dev
```

Upload the theme to the theme library as a new unpublished theme.

```bash
npm run push:upload
```

### Deploy command

Build your local files and upload them to Shopify as production.

```bash
npm run deploy
```

Build your local files and upload them to Shopify as development.

```bash
npm run deploy:dev
```

### Preview command
Returns links that let you preview the specified theme.

```bash
npm run preview
```

### Cheat command

Open Shopify Cheat Sheet.

```bash
npm run cheat
```

[Shopify Cheat Sheet](https://www.shopify.com/partners/shopify-cheat-sheet)

### Lint command

Lint this project code.

```bash
npm run lint
```

Fix this project code.

```bash
npm run lint:fix
```

### Test command

Run End-to-end testing and unit testing.

```bash
npm run test
```

Run unit testing.

```bash
npm run unit
```

```bash
npm run unit:watch
```

Run End-to-end testing in a headless.

```bash
npm run e2e
```

Run End-to-end testing with headed browser.

```bash
npm run e2e:headed
```

Generate End-to-end test code.

```bash
npm run e2e:codegen
```

### Share command
Uploads your theme as a new, unpublished theme in your theme library.

```bash
npm run share
```

### Package command
Packages your local theme files into a ZIP file that can be uploaded to Shopify.

```bash
npm run package
```

### PostInstall command

Install missing TypeScript typings.

```bash
npm run postInstall
```

</details>

## End-to-end test
Please create an env file and run this command if you want to do an End-to-end test.

Install supported browsers.

```bash
npm run e2e:install
```
## SVG sprite
You can manage SVG sprites with [svg-sprite-loader](https://www.npmjs.com/package/svg-sprite-loader).

Add SVG images into `sprite-image` folder.

```
src/ts/sprite-image/*.svg
```

Import SVG images at entrypoint.

```ts
// Import SVG Sprite Images
import './sprite-image/bag.svg';
```

The way of Using SVG Sprites in HTML and Liquid.

```html
<svg>
  <use xlink:href="#bag"></use>
</svg>
```

## Recommended IDE

[Visual Studio Code](https://code.visualstudio.com/)


## Contributes

Pull requests are always welcome.

## Support
I'll be trying to keep this starter kit as up-to-date as possible.
I hope you buy me a coffee if this starter kit is helpful for you.

<!-- BADGES/ -->
<p>
    <a href="https://buymeacoffee.com/ricebookspk" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-yellow.png" alt="Buy Me A Coffee" width="130"></a>
</p>
<!-- /BADGES -->

## License

MIT
