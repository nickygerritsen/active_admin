# Installation

Installing Active Admin in a Rails application is as easy as adding the gem to
your Gemfile:

    # Gemfile
    gem 'activeadmin'

If you are using Rails >= 3.1, you must also include a beta version of
MetaSearch and sass-rails:

    # Gemfile in Rails >= 3.1
    gem 'activeadmin'
    gem 'sass-rails'
    gem "meta_search",    '>= 1.1.0.pre'

## Running the Generator

Once you have added the gem to your Gemfile (and any other dependencies), you
need to run the Active Admin install generator.

    $> rails generate active_admin:install

This will install Active Admin the default settings. It will not create a devise user
NOTE: You will need to configure the
settings in `config/intializers/active_admin.rb` to suite your needs.

After running the installer, run `rake db:migrate` to ensure that all db tables
are created.

## Upgrading

To upgrade Active Admin, simply update the version number in your Gemfile, then
run the assets generator:

    $> rails generate active_admin:assets

This command makes sure you have all the latest assets and your installation is
up to date. Each time you upgrade Active Admin, you should run this command.
