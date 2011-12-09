Twelve
==================

This is an unofficial ruby client for the [Gauges API](http://get.gaug.es/documentation/api/). The end goal is a complete, simple, and intuitive ruby API for all things Gauges.

Usage
-----

Instantiate the client:

    access_token = "abcd1234"
    gg = Twelve.new(access_token)

### Your Information

Get your information:

    gg.me

Update your information:

    gg.me({
      :first_name => "John",
      :last_name => "Doe"
    })

Testing
-------

The test suite uses [VCR](https://github.com/myronmarston/vcr) to cache actual requests to the Gauges API in a directory called responses in the spec directory. In order for VCR to make and cache the actual calls to the Gauges API you will need to provide your Gauges access_token by placing it in a file named .access_token in the spec directory.

This file is ignored by git (see .gitignore) so you can commit any changes you make to the gem without having to worry about your token being released into the wild.

Now run the test suite:

    bundle
    bundle exec rake

CONTRIBUTE
----------

If you'd like to hack on Twelve, start by forking the repo on GitHub:

https://github.com/jonmagic/twelve

The best way to get your changes merged back into core is as follows:

1. Clone down your fork
1. Create a thoughtfully named topic branch to contain your change
1. Hack away
1. Add tests and make sure everything still passes by running `bundle exec rake`
1. If you are adding new functionality, document it in the README
1. Do not change the version number, we will do that on our end
1. If necessary, rebase your commits into logical chunks, without errors
1. Push the branch up to GitHub
1. Send a pull request for your branch