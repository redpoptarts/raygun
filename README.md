<img src="https://raw.github.com/carbonfive/raygun/master/marvin.jpg" align="right"/>

# Raygun

Command line Rails application generator that builds a new project skeleton configured with all of the Carbon Five
best practices baked right in.

Major tools/libraries:

* Rails
* PostgreSQL
* Slim
* Less
* Bootstrap
* Sorcery
* Cancan
* RSpec
* Factory Girl
* Jasmine
* Guard (rspec, jasmine, livereload)

And many tweaks, patterns and common recipes.

Inspired by Xavier Shay and ThoughtBot's Suspenders. Thanks!

## Projects Goals

Raygun...

* should generate a new rails application that's ready for feature development immediately.
* should generate an application that has best practices that apply to most projects baked in.
* is a forum for discussing what should or should not be included as part of a standard stack.

## Installation

    $ gem install raygun

## Prerequisites

Be sure you met these requirements before using raygun, otherwise you won't make it very far (misfire!).

* Ruby 1.9.2+ (rvm and rbenv supported)
* PostgreSQL 9.x with superuser 'postgres' with no password (```createuser -s postgres```)
* PhantomJS for JavaScript testing (```brew install phantomjs```)

## Usage

    $ raygun your-project

Once your project is baked out, you can easily kick the wheels:

    $ cd your-project
    $ gem install bundler
    $ bundle update

    # Prepare the database: schema and reference / sample data
    $ rake db:setup db:sample_data

    # Run the specs
    $ rake

    # Fire up the app and open it in a browser
    $ foreman start
    $ open http://0.0.0.0:3000

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

### Development

Generate an example app using your local development version of raygun

    ./bin/raygun tmp/example_app

## Changes

### 0.0.14 [2012-12-??]

* Basic usage information.
* Added guard-livereload to Guardfile.
* Gemfile, rvmrc, rbenv files configured with the ruby version used to generate the app.
* Better specs for auth flows (register, password reset, sign in).