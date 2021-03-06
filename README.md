Cucumber TCL
============

Drive your TCL code with Cucumber.

How to use
----------

This guide assumes you already have [Cucumber-Ruby](https://github.com/cucumber/cucumber) installed.

First, add the `cucumber-tcl` plugin to your Gemfile:

    gem 'cucumber-tcl'

Install it:

    bundle install

In a file in Cucumber's load path, like `features/support/env.rb`, add the following line:

    require 'cucumber/tcl'

Finally, add a TCL entry point, at `features/support/env.tcl`.

Your TCL program must implement two procs: `step_definition_exists` and `execute_step_definition`. For example:

    proc step_definition_exists {step_name} {
      return 1
    }

    proc execute_step_definition {step_name} {
      puts "Hello world"
    }
