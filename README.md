# grunt-noflo-manifest

> Grunt plugin for updating NoFlo package manifests

## Getting Started
This plugin requires Grunt `~0.4.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-noflo-manifest --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-noflo-manifest');
```

## The "noflo_manifest" task

### Overview
In your project's Gruntfile, add a section named `noflo_manifest` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  noflo_manifest: {
    update: {
      // Target-specific file lists and/or options go here.
    },
  },
});
```

### Usage Examples

#### Updating both manifest files

```js
grunt.initConfig({
  noflo_manifest: {
    both: {
      files: {
        'package.json': ['graphs/*', 'components/*'],
        'component.json': ['graphs/*', 'components/*']
      },
    }
  },
});
```
#### Updating only the Node.js package file

```js
grunt.initConfig({
  noflo_manifest: {
    nodeonly: {
      files: {
        'package.json': ['graphs/*', 'components/*']
      },
    }
  },
});
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).
