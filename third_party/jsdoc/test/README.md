Testing JSDoc 3
===============

Running Tests
-------------

Running tests is easy.  Just change your working directory to the jsdoc folder
and run the following command on Windows:

    jsdoc -T

Or on OS X, Linux, and other POSIX-compliant platforms:

    ./jsdoc -T

If you can't get the short-form commands to work, try invoking Java directly:

    java -cp lib/js.jar org.mozilla.javascript.tools.shell.Main \
    -modules node_modules -modules rhino -modules lib -modules . \
    jsdoc.js -T

Writing Tests
-------------

Adding tests is pretty easy, too.  You can write tests for JSDoc itself (to
make sure tags and the parser, etc. are working properly), tests for plugins, and/or
tests for templates.

JSDoc 3 uses Jasmine (https://github.com/pivotal/jasmine) as its testing framework.
Take a look at that project's wiki for documentation on writing tests in general.

### Tests for JSDoc

Take a look at the files in the ```test``` directory for many examples of
writing tests for JSDoc itself. The ```test\fixtures``` directory hold fixtures
for use in the tests, and the ```test\specs``` directory holds the tests themselves.

### Tests for plugins

Tests for plugins are found in the ```plugins\test``` directory. Plugins containing
tests that were installed with the Jakefile install task will be run automatically.

### Tests for templates

TODO
