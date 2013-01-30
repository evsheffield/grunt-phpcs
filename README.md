# grunt-phpcs

> Grunt plugin for running PHP Code Sniffer.

_This plugin is developed for Grunt `0.4.0` and is not tested for backward compatibility with Grunt `0.3.x`._


##Getting Started
1. Install this grunt plugin with the following command:

	```shell
	npm install grunt-phpcst --save-dev
	```


2. [Install PHP Code Sniffer](https://github.com/squizlabs/PHP_CodeSniffer#installation) (preferably with [composer](https://github.com/composer/composer))
3. Add this to your project's `Gruntfile.js` gruntfile:

	```js
	grunt.loadNpmTasks('grunt-phpcs');
	```


##PHPUnit task
_Run this task with the `grunt phpunit` command._

_This task is a [multi task][] so any targets, files and options should be specified according to the [multi task][] documentation._

[multi task]: https://github.com/gruntjs/grunt/wiki/Configuring-tasks

###Target Properties
####dir
Type: `String`

The directory where phpunit should be run, i.e. where the test classes and the bootstrap are located in.

###Options
####bin
Type: `String`  Default: `'phpunit'`

Generate code coverage report in text format. This option can also be set by running the task with `--coverage`.

####debug
Type: `Boolean` Default: `false`

Display debbuging information during test execution. This option can also be set by running the task with `--debug`.

####verbose
Type: `Boolean` Default: `false`

Output more verbose information. This option can also be set by running the task with `--verbose`.

###Usage Example

```js
phpucs: {
	application: {
		dir: 'app/php/'
	},
	options: {
		bin: 'vendor/bin/phpcs'
	}
}
```