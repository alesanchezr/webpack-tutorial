# Webpack installation

During this short tutorial, we will be installing webpack from scratch.

## What do you need?
You will need a computer with Node and NPM installed.

1. Check your version of NPM:

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

4. We want to be able to bunble CSS file into our JS bundles, for that we need both the Style and CSS loaders.

```sh
$ npm install --save-dev style-loader css-loader
```

5. We also want to use SCSS (Sass) syntaxt.

```sh
$ npm install sass-loader node-sass webpack --save-dev
```

## Time to decide what type of installation do you want.

Click on the best option according to your needs.

 - [Vanilla JS application](/alesanchezr/webpack-tutorial/blob/master/configurations/VANILLAJS.md): A simple Javascript web application.
 - [WordPress](http://github.com): Use Webpack with your WordPress installation
 - [React JS](http://github.com): Install everything you need to start a basic react application.