# laravel-mix-usage-sample

## [How this project was created](https://laravel-mix.com/docs/5.0/installation)
```
mkdir laravel-mix-usage-sample && cd laravel-mix-usage-sample
npm install laravel-mix --save-dev
cp ./node_modules/laravel-mix/setup/webpack.mix.js ./
node_modules/.bin/webpack --config=node_modules/laravel-mix/setup/webpack.config.js
npm i -D cross-env
```

### `package.json`
```json
"scripts": {
  "dev": "npm run development",
  "development": "cross-env NODE_ENV=development node_modules/webpack/bin/webpack.js --progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js",
  "watch": "npm run development -- --watch",
  "hot": "cross-env NODE_ENV=development node_modules/webpack-dev-server/bin/webpack-dev-server.js --inline --hot --config=node_modules/laravel-mix/setup/webpack.config.js",
  "prod": "npm run production",
  "production": "cross-env NODE_ENV=production node_modules/webpack/bin/webpack.js --no-progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js"
},
```
