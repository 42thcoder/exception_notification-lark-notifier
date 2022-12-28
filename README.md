# Exception Notification - Lark Notifier

The [Exception Notification](https://github.com/smartinez87/exception_notification) gem provides a
set of notifiers for sending notifications when errors occur in a Rack/Rails application. This gem
adds support for delivering notifications to [Lark](https://www.larksuite.com).


## Installation

Add this line to your application's Gemfile:

```ruby
gem 'exception_notification'
gem 'exception_notification-lark-notifier'
```

And then execute:

    $ bundle install

Or install it yourself as:

    $ gem install exception_notification-lark-notifier


## Usage

In order to receive exceptions in Lark, you need to add a custom bot to the group chat.

To configure it, you need to set the webhook address, like this:

```ruby
Rails.application.config.middleware.use ExceptionNotification::Rack,
  lark: {
    webhook: 'https://open.larksuite.com/open-apis/bot/v2/hook/xxxxxxxxxxxxxxxxx'
  }
```


## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and the created tag, and push the `.gem` file to [rubygems.org](https://rubygems.org).


## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/souk4711/exception_notification-lark-notifier. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [code of conduct](https://github.com/souk4711/exception_notification-lark-notifier/blob/main/CODE_OF_CONDUCT.md).


## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).


## Code of Conduct

Everyone interacting in the exception_notification-lark-notifier project's codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/souk4711/exception_notification-lark-notifier/blob/main/CODE_OF_CONDUCT.md).
