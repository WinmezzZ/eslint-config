# eslint-config

#### An ESLint [Shareable Config](http://eslint.org/docs/developer-guide/shareable-configs) for Typescript React Base Style with Prettier.

### Features
- **ESLint**: ✅
- **TypeScript** ✅
- **React**: ✅
- **Prettier**: ✅

### Install

This module is for advanced users. You probably want to use `react-base` instead :)

```bash
npm install @winme/eslint-config -D
```

### Usage

Shareable configs are designed to work with the `extends` feature of `.eslintrc` files.
You can learn more about
[Shareable Configs](http://eslint.org/docs/developer-guide/shareable-configs) on the
official ESLint website.

Then, add this to your `.eslintrc` file:

```
{
  "extends": ["@winme/eslint-config"]
}
```

You can override settings from the shareable config by adding them directly into your
`.eslintrc` file.

For auto fix problem, strongly recommanded you add below options into `.vscode/settings.json` at root of directory;

```json
{
  "typescript.tsdk": "node_modules/typescript/lib",
  "eslint.validate": ["javascript", "javascriptreact", "typescript", "typescriptreact"],
  "eslint.options": {
    "extensions": [".js", ".jsx", ".ts", ".tsx"]
  },
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "editor.formatOnSave": true,
  "[javascript]": {
    "editor.formatOnSave": false
  },
  "[javascriptreact]": {
    "editor.formatOnSave": false
  },
  "[typescript]": {
    "editor.formatOnSave": false
  },
  "[typescriptreact]": {
    "editor.formatOnSave": false
  }
}
```

For global lint/format, add below scripts in `package.json`
```json
"scripts": {
  "lint": "eslint . --ext js,ts,tsx",
  "format": "eslint . --ext js,ts,tsx --fix"
}
```

### License

MIT. Copyright (c) eslint-config.
