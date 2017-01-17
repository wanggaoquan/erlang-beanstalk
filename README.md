# erlang-beanstalk


An Erlang client for [beanstalkd](http://kr.github.com/beanstalkd/).


## Quick start

    $ make
    ...
    $ erl -pa ebin
    ...
    1> {ok, Q} = beanstalk:connect().
    ...
    2> {inserted, ID} = beanstalk:put(Q, <<"hello world">>).
    ...
    3> {reserved, ID, <<"hello world">>} = beanstalk:reserve(Q).
    ...
    4> {deleted} = beanstalk:delete(Q, ID).
    ...
    5> ok = beanstalk:close(Q).
    ...

## License

This project is licensed under the terms of the [MIT license](https://opensource.org/licenses/MIT).
