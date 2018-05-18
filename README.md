SpreePriceBooks
===============

Allows flexibility to show different list prices, sale prices, role prices, store prices, and whatever else you can think of.

Installation
------------

Add spree_price_books to your Gemfile:

```ruby
gem 'spree_price_books', github: 'spree-contrib/spree_price_books'
```

Bundle your dependencies and run the installation generator:

```shell
bundle
bundle exec rails g spree_price_books:install
```

Configuration
-------------

Once installed you can seed default currency exchange rates via Google's Currency API.

```shell
bundle exec rake price_books:currency_rates
```

Or configure from within the admin panels configuration tab.

The default currency for the store must match the default price books currency.

Testing
-------

First bundle your dependencies, then run `rake`. `rake` will default to building the dummy app if it does not exist, then it will run specs. The dummy app can be regenerated by using `rake test_app`.

On the first run you may need to create the Postgresql role (ex. `createuser -d postgres`)

```shell
bundle
bundle exec rake
```

When testing your applications integration with this extension you may use it's factories.
Simply add this require statement to your spec_helper:

```ruby
require 'spree_price_books/factories'
```

Credit
------

http://www.surfdome.com/ for sponsoring the project.

Copyright (c) 2014 Jeff Dutil, released under the New BSD License