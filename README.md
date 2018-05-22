# babel-vscode-skeleton
babel ES6 + node + vscode debugging environment project skeleton

# How to use?
1. Remove `README.md` and create yours
2. `yarn add --dev babel-cli babel-preset-env babel-plugin-transform-object-rest-spread`
3. Add the following to your `package.json`
```json
"scripts": {
    "start": "node dist/main.js",
    "build": "babel src --out-dir dist --source-maps"
},
```

4. Start your work in `src/main.js`
5. You can use vscode to debug your code

## Enable `err.stack` source mapping
1. `yarn add --dev source-map-support`
2. Put the following code at the top of `src/main.js` (before any `import` or `require`)
```js
import 'source-map-support/register';
```

3. Debug your code and `err.stack` will be source mapped
