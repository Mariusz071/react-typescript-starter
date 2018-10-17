# react-ts-webpack-starter

## Instructions:
Go to desired folder that will contain project files.
1. `npm init`

Follow steps to initiate npm module


2. `npm i -D @babel/core @babel/preset-env @babel/preset-typescript @babel/preset-react @babel/plugin-proposal-class-properties @babel/plugin-proposal-object-rest-spread typescript webpack webpack-cli webpack-dev-server webpack-merge`

You can additionally install typescript globally for easier usage


3. `npm i react react-dom @types/react @types/react-dom`


4. `touch .gitignore` and fill it up with:

```
/node_modules
/dist
```


5. `touch .babelrc` and fill it up with:

```json
{
  "presets": [
    "@babel/react",
    "@babel/typescript",
    "@babel/env"
  ],
  "plugins": [
    "@babel/proposal-class-properties",
    "@babel/proposal-object-rest-spread"
  ]
}
```


6. `./node_modules/.bin/tsc --init` or `tsc --init`

Generate basic tsconfig file then uncomment and modify:
- `"baseUrl": "./src"`
- `"allowSyntheticDefaultImports": true`
- `"experimentalDecorators": true`
- `"emitDecoratorMetadata": true`
- `"lib": ["dom", "es2017"]`
- `"module": "es6"` or `"module": "es2015"`
- `"moduleResolution": "node"`
- `"noUnusedLocals": true`
- `"noUnusedParameters": true`
- `"outDir": "./dist"`
- `"noEmit": true`
- `"paths": {}` here you are defining aliases used in typescript in key/value structure use your own structure or check example
- `"sourceMap": true`
- `"target": "esnext"`


7. `mkdir src && mkdir config && cd config && mkdir webpack && cd webpack && touch webpack.config.base.js && touch webpack.config.dev.js && touch webpack.config.prod.js`

Create `src` and `config/webpack` directories. Second directory will contain 3 files for webpack configuration. Webpack will be configured in JavaScript.


8. `npm i -D html-webpack-plugin clean-webpack-plugin mini-css-extract-plugin babel-loader style-loader css-loader file-loader url-loader`

Configure `Webpack` for your needs, install needed loaders, check example if you need help.


9. Add starting scripts to `package.json`

```json
"scripts": {
  "build:prod": "./node_modules/.bin/webpack --config ./config/webpack/webpack.config.prod.js",
  "build:dev": "./node_modules/.bin/webpack --config ./config/webpack/webpack.config.dev.js",
  "watch": "./node_modules/.bin/webpack-dev-server --config ./config/webpack/webpack.config.dev.js"
},
```


9. Start coding in React on Typescript :)
