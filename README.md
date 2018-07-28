# TTY:PieChart [![Gitter](https://badges.gitter.im/Join%20Chat.svg)][gitter]

> Draw pie charts in your terminal window

**TTY::PieChart** provides pie chart drawing component for [TTY](https://github.com/piotrmurach/tty) toolkit.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'tty-pie_chart'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install tty-pie_chart

## Contents

* [1. Usage](#1-usage)
* [2. Interface](#2-interface)

## 1. Usage

To draw a pie chart you need to provide an array of data items:

```ruby
data = [
  { name: 'BTC', value: 5977, color: :bright_yellow, fill: '*' },
  { name: 'BCH', value: 3045, color: :bright_green, fill: 'x' },
  { name: 'LTC', value: 2030, color: :bright_magenta, fill: '@' },
  { name: 'ETH', value: 2350, color: :bright_cyan, fill: '+' }
]
```

Then pass data to **TTY::PieChart** instance with a given radius:

```ruby
pie_chart = TTY::PieChart.new(data, radius: 5)
```

and print the pie chart in your terminal window:

```ruby
print pie_chart.draw
# =>
#         ++***
#     ++++++*******        * BTC 44.60%
#   @@@+++++*********
#  @@@@@@+++**********     x BCH 22.72%
# @@@@@@@@@+***********
# @@@@@@@@@@x**********    @ LTC 15.15%
# @@@@@@@@@xx**********
#  @@@@@@xxxx*********     + ETH 17.53%
#   @@@xxxxxxx*******
#     xxxxxxxx*****
#         xxxx*
# 
```

## 2. Interface

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/tty-pie_chart. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the Tty::PieChart project’s codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/[USERNAME]/tty-pie_chart/blob/master/CODE_OF_CONDUCT.md).