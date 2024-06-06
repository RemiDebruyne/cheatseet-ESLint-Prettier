# How to configure eslint and prettier

## Prettier
- `npm install --save-dev prettier eslint-config-prettier eslint-plugin-prettier` : disables formatting for ESLint and allows ESLint to show formatting errors
- Create `.prettierrc.json` :
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
}
```


## Eslint

 - `npx install-peerdeps --dev eslint-config-airbnb` : installs eslint and airbnb config
 - Create `.eslintrc.json` :
```json
 {
  "extends": ["airbnb-base", "prettier"],
  "plugins": ["prettier"],
  "parserOptions": {
      "project": "./tsconfig.json"
  },
  "rules": {
      //We can specify more rules that we need here
    "prettier/prettier": ["error"],
    "import/extensions": ["error", "ignorePackages", { "js": "never", "jsx": "never", "ts": "never", "tsx": "never" }]
  }
    }
```
   
To automatically format your code, add the line bellow or use the eslint vscode extension   

- In your package.json
```json
"scripts": {
   "lint" : "./node_modules/.bin/eslint"
}
```

