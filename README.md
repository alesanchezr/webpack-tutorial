# Introduction

This repository containas the basic steps (tutorial) to install Webpack for the following environments:

1. Standalone Javascript Application.
2. WordPress instalation.
3. React JS instalation (Not ready yet).

All of the configurations include JS, CSS, SASS and Image bundling.

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

# Choose your instalation

For the next steps you need to choose what type of aplication you are going to develop:

    - [Vanilla JS Application](http://www.github.com).
    - [WordPress Application](http://www.github.com).
    - [React JS Application](http://www.github.com).