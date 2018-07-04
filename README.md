# Omniauth::Medium2

OmniAuth strategy for Medium.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'omniauth-medium2'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install omniauth-medium2

## Usage

Tell OmniAuth about the Medium provider. For a Ruby on Rails application, your ```config/initializers/omniauth.rb``` file should look like:

```ruby
Rails.application.config.middleware.use OmniAuth::Builder do
  provider :medium, ENV['MEDIUM_APP_ID'], ENV['MEDIUM_APP_SECRET']
end
```

Set the client keys from your [app](https://medium.com/me/applications) and restart your application. Redirect the user to ```/auth/medium``` for authentication.

## Response

An example to the authentication hash:

```ruby
{
  "provider" => "medium",
  "uid" => "59bd618b5274ef1474af059157611a014721dcebe704d04bca8353d79f61b928",
  "info" => {
    "id" => "59bd618b5274ef1474af059157611a014721dcebe704d04bca8353d79f61b928",
    "imageUrl" => "<URL>",
    "name" => "Anindya Mondal",
    "url" => "https://medium.com/@xyz",
    "username" => "xyz"
  },
  "credentials" => {
    "expires" => true,
    "expires_at" => 1535858205648,
    "refresh_token" => "1ec9c8b162ff7e460cfad7ea9312dde2ab9bd03a248a3339a196133aab700511",
    "token" => "38aa71b7ec1d9a0d1e53424a794dee0c77110087923b272c36576ab31f4df0a5"
  },
  "extra" => {}
}
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake test` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/Anindya91/omniauth-medium2.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
