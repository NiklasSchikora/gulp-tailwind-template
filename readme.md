# Gulp & TailwindCSS Template ✨

This is a forked and modified version of [@lazymorek's](https://github.com/lazymozek/gulp-with-tailwindcss) [Gulp + Tailwind StarterKit](https://github.com/lazymozek/gulp-with-tailwindcss) that can be used for UI-projects and template-design. I added support of HTML-partials, preferably in the partials-directory and modified the structure and usage of scss-files. This version is uptdated to use sass instead of node-sass to enable support on M1-devices.

## Usage

1. Install Dev Depedencies

```sh
npm install // or yarn install
```

2. To start development and server for live preview

```sh
npm run dev // or yarn dev
```

3. To generate minifed files for production server

```sh
npm run prod // or yarn prod
```

# Partials

This template supports the usage of HTML-partials with gulp-fileinclude.

## Create partials

To use partials, gulp-fileinclude is configured to watch for .html-documents in the `./src/` directory. Therefore partials can be stored anywhere inside the `./src/` directory. By default they are stored under `./src/partials/`.

## Use partials

Partials can be embeded in HTML-files using the following syntax:

```
@@include("./partials/test.html")
@@include("./relative/path/to/partial.html")
```

# Configuration

To change the path of files and destination/build folder, edit options in **config.js** file

```sh
{
  config: {
      ...
      port: 9050 // browser preview port
  },
  paths: {
     root: "./",
     src: {
        base: "./src",
        css: "./src/css",
        js: "./src/js",
        img: "./src/img"
     },
     dist: {
         base: "./dist",
         css: "./dist/css",
         js: "./dist/js",
         img: "./dist/img"
     },
     build: {
         base: "./build",
         css: "./build/css",
         js: "./build/js",
         img: "./build/img"
     }
  }
  ...
}
```
