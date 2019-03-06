# Akarion stylelint config

> This package provides the Akarion base .stylelintrc as an extensible shared config.

## Usage

```bash
npm install AkarionDevelopers/stylelint-config-akarion#v1.0.0 --save-dev
```

```js
// .stylelintrc
{
  "extends": "stylelint-config-akarion"
}
```

## Tooling / IDE

If you are using VSCode with Vetur and ESLint extensions installed, be sure to copy following settings into your settings.json for correct linting:
```json
{
  // settings.json

  // ... Your custom settings here

  // START COMMON AKARION SETTINGS
  "editor.tabSize": 2,
  "eslint.validate": [
    {
      "language": "vue",
      "autoFix": true
    },
    {
      "language": "html",
      "autoFix": true
    },
    {
      "language": "javascript",
      "autoFix": true
    }
  ],
  "eslint.alwaysShowStatus": true,
  "eslint.autoFixOnSave": true,

  "vetur.validation.script": false,
  "vetur.validation.style": false,

  // Stylelint
  "css.validate": false,
  "scss.validate": false
  // END COMMON AKARION SETTINGS
}
```
