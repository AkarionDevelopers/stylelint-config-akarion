# Akarion stylelint config

> This package provides the Akarion base .stylelintrc as an extensible shared config.

## Usage

```bash
npm install AkarionDevelopers/stylelint-config-akarion#v2.0.1 --save-dev
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

  "css.validate": false,
  "scss.validate": false
}
```

## Lintfixing on save in VSCode

To run lintfix on save follow these steps:
1. Install VSCode extension [Save and run](https://marketplace.visualstudio.com/items?itemName=wk-j.save-and-run#overview)
2. Place these lines in your `settings.json`:
   
```json
"saveAndRun": {
    "commands": [
        {
            "match": "\\.(vue|s?css)$",
            "cmd": "npx stylelint '${file}' --fix",
            "silent": true
        },
    ]
},
```

### Caveats / Gotchas

`CMD + S` isn't automatically triggering the plugin. `saveAndRun` only gets triggered if the *file actually has changed*.