[![npm version](https://badge.fury.io/js/csscomb-config-rawbot.svg)](https://badge.fury.io/js/csscomb-config-rawbot)

# csscomb-config-rawbot

Rawbot CSSComb common configuration (i.e. CSS/SCSS styleguide).

Include coding style rules for stylesheets, with grouping and ordering of properties.

Check the `index.json` file if you want to know more about the rules applied.

## Install

```bash
npm install --save-dev csscomb-config-rawbot
```

CSSComb is required but not included, if you don’t have it already, install it with:

```bash
npm install --save-dev csscomb
```

## Use

You can now run CSSComb once with `npx` for example.

To lint files and output the results only:

```bash
npx csscomb -lv -c node_modules/csscomb-config-rawbot/index.json path/to/your/stylesheet/files
```

To update the files by automatically fixing all offenses:

```bash
npx csscomb -c node_modules/csscomb-config-rawbot/index.json path/to/your/stylesheet/files
```

Or create dedicated npm scripts to run easily, by adding the following lines to your `package.json`:

```json
"scripts": {
  "lint:style": "csscomb -lv -c node_modules/csscomb-config-rawbot/index.json path/to/your/stylesheet/files",
  "lint:style:fix": "csscomb -c node_modules/csscomb-config-rawbot/index.json path/to/your/stylesheet/files",
}
```

You can now run `npm run lint:style` and `npm run lint:style:fix` whenever you need.

Check the [CSSComb cli documentation](https://github.com/csscomb/csscomb.js/blob/dev/doc/usage-cli.md) for more details.
