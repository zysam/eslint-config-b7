# eslint-config-b7

Node Style Guide for b7. fork eslint-config-egg

## Install

```bash
npm i eslint eslint-config-b7 --save-dev
```

## Usage

- `package.json`

```json
{
  "devDependencies": {
    "eslint-config-b7": "3",
    "eslint": "3"
  }
}
```

- `.eslintrc.js`

```js
module.exports = {
  extends: 'eslint-config-b7',
};
```

### Use with Experimental Features

If you want to use eslint-config-b7 with experimental features such as `async function`, you should use `babel-eslint` parser:

- `package.json`

```json
{
  "devDependencies": {
    "eslint-config-b7": "3",
    "eslint": "3",
    "babel-eslint": "6"
  }
}
```

- `.eslintrc.js`

```js
module.exports = {
  extends: 'eslint-config-b7',
  // for experimental features support
  parser: 'babel-eslint',
  rules: {
    // see https://github.com/eslint/eslint/issues/6274
    'generator-star-spacing': 'off',
    'babel/generator-star-spacing': 'off',
  }
};
```

### Use with React in Front-End

If you want to use eslint-config-b7 with react, jsx and es6 modules:

- `package.json`

```json
{
  "devDependencies": {
    "eslint-config-b7": "3",
    "eslint": "3",
    "babel-eslint": "6",
    "eslint-plugin-react": "4"
  }
}
```

- `.eslintrc.js`

```js
module.exports = {
  extends: 'eslint-config-b7',
  // for experimental features support
  parser: 'babel-eslint',
  parserOptions: {
    // for es6 module
    sourceType: 'module',
  },
  plugins: [
    'react',
  ],
  rules: {
    // for variables in jsx
    'react/jsx-uses-vars': 'error',
    // see https://github.com/eslint/eslint/issues/6274
    'generator-star-spacing': 'off',
    'babel/generator-star-spacing': 'off',
  },
};
```

## License

[MIT](LICENSE)
