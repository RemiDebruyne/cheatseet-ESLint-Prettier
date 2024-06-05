# How to configure eslint and prettier

## Prettier

- Download `prettier` vscode extension
- `npm install --save-dev prettier` : install prettier package
- `npm install --save-dev eslint-config-prettier eslint-plugin-prettier` : disables formatting for ESLint and allows ESLint to show formatting errors
- Create `.prettierrc.json` with the following settings :
- 
```json
{
  "semi": false,
  "singleQuote": true,
  "tabWidth": 2,
  "useTabs": false,
  "endOfLine": "auto",
  "printWidth": 80,
  "arrowParens": "avoid",
  "proseWrap": "always",
  "htmlWhitespaceSensitivity": "strict",
  "jsxBracketSameLine": false,
  "bracketSpacing": true,
  "insertPragma": false,
  "requirePragma": false,
  "quoteProps": "as-needed",
  "trailingComma": "none",
  "eslintIntegration": true,
  "parser": "babel",
  "jsxSingleQuote": false,
  "vueIndentScriptAndStyle": false,
  "semi": false,
  "tabWidth": 2,
  "singleQuote": true
}
```


## Eslint

 - `npx install-peerdeps --dev eslint-config-airbnb` : installs eslint and airbnb config
 - Create `.eslintrc.json` and add :
```json
{
  "extends": "airbnb"
}
```
   
To automatically format your code, add the line bellow or use the eslint vscode extension   
- In your package.json
```json
"scripts": {
   "lint" : "./node_modules/.bin/eslint"
}
```

