# Webpack installation

During this small tutorial, will be installing webpack from scratch, you will need a computer with NPM and Node installed.

1. Check your version of NPM like this:

```sh
$ npm -v
```

Note: You need at least the 3.5 version of NPM to avoid any performance issues.

2. Create a new npm package

```sh
$ npm init -y
```


3. Install webpack

```sh
$ npm install --save-dev webpack
```

4. We want to be able to bunble CSS file into our JS bundles, for that we need the Style and CSS loaders.

```sh
$ npm install --save-dev style-loader css-loader
```

5. We also want to use SCSS (Sass) syntaxt.

```sh
$ npm install sass-loader node-sass webpack --save-dev
```


6. Create a ./src directory and a ./public directory

The src/ directory will contain your source code in javascript and scss.
The public/ directory will contain your HTML and images by default. Any other file will be automatically created by webpack.

7. Create a webpack.config.js file with the following content:

```
  const path = require('path');

  module.exports = {
    entry: './src/index.js',
    output: {
      filename: 'bundle.js',
      path: path.resolve(__dirname, 'public')
    },
    module: {
        rules: [
            {
                test: /\.css$/,
                use: [
                'style-loader',
                'css-loader'
                ]
            },
            {  //Here we are including the .scss loader to make it transpale Sass to CSS.
                test: /\.scss$/,
                use: [{
                    loader: "style-loader" // creates style nodes from JS strings
                }, {
                    loader: "css-loader" // translates CSS into CommonJS
                }, {
                    loader: "sass-loader" // compiles Sass to CSS
                }]
            }
        ]
    }
  };
```

8. Create a index.js file insite the ./src folder with the following content:

```
window.onload=function(){ alert('hello webpack'); }
```

9. Run webpack with the following command:

```sh
$ webpack
```

10. Make sure that webpack created the bundle, you should see an output like this:
```sh
    alesanchezr:~/workspace (master) $ webpack
    Hash: 69f7ef42fb105dfe89e9
    Version: webpack 3.5.4
    Time: 115ms
        Asset     Size  Chunks             Chunk Names
    bundle.js  2.52 kB       0  [emitted]  main
       [0] ./src/index.js 50 bytes {0} [built]
```

11. If everything went well, create an ./public/index.html file and import the bundle.js script. Run you index.html file and the alert should promt!