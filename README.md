# omniauth_crowd [![Build Status](https://travis-ci.org/robdimarco/omniauth_crowd.svg?branch=master)](https://travis-ci.org/robdimarco/omniauth_crowd)

The omniauth_crowd library is an OmniAuth provider that supports authentication against Atlassian Crowd.

A form is presented to the user within your application, where they are asked to enter their credentials.

## Helpful links

*	[Documentation](http://github.com/robdimarco/omniauth_crow)
*	[OmniAuth](https://github.com/intridea/omniauth/)
* [Atlassian Crowd](http://www.atlassian.com/software/crowd/)
* [Atlassian Crowd REST API](http://confluence.atlassian.com/display/CROWDDEV/Crowd+REST+APIs)

## Using this provider

If you're not already using OmniAuth in your project, see [OmniAuth](https://github.com/intridea/omniauth/) for more information.

### Add this gem to your Gemfile

```ruby
gem "omniauth", '>= 1.0'
gem "omniauth_crowd"
```

### Add to OmniAuth configuration

In Rails, this is generally done in `config/initializers/omniauth.rb`:

```ruby
Rails.application.config.middleware.use OmniAuth::Builder do
  provider :crowd, 
           crowd_server_url: "https://crowd.mycompanyname.com/crowd",
           application_name: "this app",
           application_password: "password"
end
```

* `crowd_server_url`: URL of the Crowd server.
* `application_name`: The name given to this application as set up in the Crowd server.
* `application_password`: The password assigned to this application in the Crowd server.

## Contributing to omniauth_crowd
 
* Check out the latest master to make sure the feature hasn't been implemented or the bug hasn't been fixed yet
* Check out the issue tracker to make sure someone already hasn't requested it and/or contributed it
* Fork the project
* Start a feature/bugfix branch
* Commit and push until you are happy with your contribution
* Make sure to add tests for it. This is important so I don't break it in a future version unintentionally.
* Please try not to mess with the Rakefile, version, or history. If you want to have your own version, or is otherwise necessary, that is fine, but please isolate to its own commit so I can cherry-pick around it.

## Copyright

Copyright (c) 2011-14 Rob Di Marco. See LICENSE.txt for
further details.
