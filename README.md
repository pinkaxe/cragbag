
## Intro

This contains a ragbag of useful c libraries. Datastructures like queues but
also libraries for things like async execution, data pools etc. Basicly anything
useful for other libraries or applications. The idea is to keep it without
external dependencies. Some of it is dependent on threads but some is not and
can be used where threads aren't available.

This was developed in pinkaxe/nodenet before so check there for the history.

## Build

Build with,

    sudo apt-get install -y \
          autoconf automake build-essential libtool
    autoreconf --install --force
    ./configure --prefix=$PWD/out
    make -j$(nproc)
    make install

There should be libaries in out/lib and tests in out/bin.

## Code

See the individual directories eg. for linked list see ll/*.[ch]. For example
usage see the _test.c files in each lib directory.


## TODO

- The tests has to be improved, output isn't informative without looking at the
source code and most just run in a loop and never end.
