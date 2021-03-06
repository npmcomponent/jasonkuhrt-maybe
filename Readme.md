*This repository is a mirror of the [component](http://component.io) module [jasonkuhrt/maybe](http://github.com/jasonkuhrt/maybe). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/jasonkuhrt-maybe`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# maybe [![Code Climate](https://codeclimate.com/github/jasonkuhrt/maybe.png)](https://codeclimate.com/github/jasonkuhrt/maybe)

  Correct implementation of the Maybe monad in JavaScript

## Installation

  Install with [component(1)](http://component.io):

    $ component install jasonkuhrt/maybe

  Install with [npm(1)](https://npmjs.org)

    $ npm install jasonkuhrt/maybe

## API

#### Constructor

##### Maybe
    (a) -> Maybe a

==========

#### Instance methods

##### .bind()
    (a -> b) -> Maybe b

  Passed function is automatically lifted.

##### .{package_function}()
  All package functions are partially applied with the monadic-value and exposed as properties on the `Maybe a` value. e.g.:

    var some_unstable_value = Maybe(null);

    // Pure style
    Maybe.is_nothing(some_unstable_value)  // true

    // Chain style
    some_unstable_value.is_nothing()       // true

==========

#### Package Functions {...}

##### maybe
    (else_value, (a -> b), Maybe a) -> b

##### is_nothing
    (Maybe a) -> Bool

##### is_just
    (Maybe a) -> Bool

##### from_just
    (Maybe a) -> Bool

##### from_maybe
    (else_value, Maybe a) -> a


## License

  BSD-2-Clause
