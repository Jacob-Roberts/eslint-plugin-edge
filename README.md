# ESLint Plugin Edge

This eslint environment will help ensure you have the environment set correctly for edge / browser development.

## Installation

You'll first need to install [ESLint](https://eslint.org/):

```sh
npm i eslint --save-dev
```

Next, install `eslint-plugin-edge`:

```sh
npm install eslint-plugin-edge --save-dev
```

## Usage

Add `edge` to the plugins section of your `.eslintrc` configuration file. You can omit the `eslint-plugin-` prefix:

```json
{
  "plugins": ["edge"]
}
```

Add the environment to your eslint config:

```json
{
  "env": {
    "eslint-plugin-edge/edge-and-browser": true, // If your code is for both edge and browser
    "eslint-plugin-edge/edge": true // If your code is for edge only (has more features)
  }
}
```

## Next.js

If your code is running on next.js, the edge has one extra polyfill for `AsyncLocalStorage`.

To add it, add the following global to your eslint config:

```json
{
  "globals": {
    "AsyncLocalStorage": "readonly"
  }
}
```
