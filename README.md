Guard-Steering examples
=======================

A sample repository to demonstrate Guard-Steering and Steering Ruby gems on some Handlebars templates and partials.

[Handlebars.js](http://handlebarsjs.com/) is a great JavaScript templating engine, based on [Mustache](http://mustache.github.com/), but adding the ability to precompile templates and to create custom helpers.

[Steering](https://github.com/pixeltrix/steering) is a Ruby wrapper for the Handlebars library, making it possible to compile and precompile templates, using the magic of the ExecJS engine.

[Guard-Steering](https://github.com/daaain/guard-steering) is a [Guard](https://github.com/guard/guard) built around Steering to make it possible to recompile templates as they are edited by watching the changes in your file system.

Now having all these out of the way let's see how to get set up:

1. Install [RubyGems](https://rubygems.org/) and [Bundler](http://gembundler.com/) if you haven't done so yet
2. Clone this repository and run `bundle install` on the command line inside the main folder (Bundler is configured to install everything under `vendor` in the project folder, so don't worry about your system being messed up)
3. Load each example into your favourite browser to first see how the templates are not working yet, only placeholder text is going to be displayed
4. Run `bundle exec guard` on the command line and you should see messages telling you that Guard-Steering has created the precompiled templates
5. Reload the examples in your browser and if everything went well you should see the templates nicely rendered

If you haven't done so, take a look at the `Guardfile` and the example folders to understand what has just happened.

## Basic example

A very simple example, a placeholder `div` will be replaced by small template.

## Partials example

In this example a list is generated with a few items. The trick is that the list itself is also a template, which then renders the list item template as partial.

In order to make this possible, you have to use the `:register_partials => true` option in the `Guardfile` so that Guard-Steering will register the templates as partials in the precompiled JavaScript files.

## License

Public domain – do whatever you feel like with it!