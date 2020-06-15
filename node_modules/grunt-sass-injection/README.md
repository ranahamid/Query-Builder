# grunt-sass-injection

> Compile an import file based on scss files in a directory.

## Getting Started
This plugin requires Grunt `~0.4.0`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-sass-injection --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-sass-injection');
```

## The "sass_injection" task

### Overview
In your project's Gruntfile, add a section named `sass_compile_imports` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  sass_injection: {
    options: {
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    },
  },
});
```

The following comments need to be placed in your site.scss/app.scss for the plugin to work properly. 
```
// import

// endimport
```
If you have some scss files that need to go to the top of the file you can optionally add the following to your scss file: 
```
// topImport

// endtopImport
```
This will take any scss partial file with a double underscore in the name and place it at between the two comment tags. Otherwise the files all go into the regular import call which should be further down in your main scss file. 


### Options

#### options.removeExtension
Type: `Boolean`
Default value: `true`

Flag specifying if the generated paths should exclude the .scss extension.

#### options.quiet
Type: `Boolean`
Default value: `false`

A flag used to specify if the task should output information about the files it is importing


