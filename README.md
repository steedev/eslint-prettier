# ESLint & Prettier

![image](https://user-images.githubusercontent.com/71899777/121804013-0b9ee980-cc3c-11eb-86f6-3547fcfe0397.png)

## Installation and Usage

You can install ESLint using npm:

```
npm install eslint --save-dev
```

You should then set up a configuration file:

```
./node_modules/.bin/eslint --init
```

or

```
eslint --init
```

## Configuration

After running `eslint --init`, you'll want to setup a `package.json` file in your directory. In it, you'll see some scripts configured like this:

```json
"scripts": {
    "lint": "./node_modules/.bin/eslint .",
    "lint:fix": "./node_modules/.bin/eslint . --fix"
},
```

or

```json
"scripts": {
    "lint": "eslint .",
    "lint:fix": "eslint . --fix"
},
```

## Prettier

You can install Prettier using npm:

```
npm install prettier eslint-config-prettier eslint-plugin-prettier --save-dev
```

Then, in your `.eslintrc.js`:

```json
{
  "extends": ["plugin:prettier/recommended"],
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": "error"
  }
}
```

You can then set Prettier's own options inside a `.eslintrc.js` file:

```json
{
    "rules": {
        "prettier/prettier": [
          "error",
          { "semi": false, "trailingComma": "all", "singleQuote": true },
        ],
    },
}
```

## ESLint & Prettier VSCode settings

To setup your VSCode you can paste this code to your `settings.json` file:

```json
"editor.defaultFormatter": "dbaeumer.vscode-eslint",
  "eslint.format.enable": true,
  "eslint.lintTask.enable": true,
  "eslint.alwaysShowStatus": true,
  "eslint.validate": ["javascript", "typescript", "html"],
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "editor.formatOnSave": true,
```

## Configuration Files

To setup ESLint copy these `js` files:

* [`.eslintrc.js`](/configs/js/default/.eslintrc.js)
* [`package.json`](/configs/js/default/package.json)

To setup ESLint copy these `ts` files:

* [`.eslintrc.js`](/configs/ts/default/.eslintrc.js)
* [`package.json`](/configs/ts/default/package.json)
