# ESlint & Prettier

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
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": "error"
  }
}
```
