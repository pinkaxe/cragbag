
## Intro

This contains a ragbag of useful c libraries. Data-structures like queues but
also libraries for things like async execution and data pools. Basically
anything useful for other libraries or applications. The idea is to keep it
without external dependencies. Some of it is dependent on threads but some is
not and can be used where threads aren't available.

This was developed in pinkaxe/nodenet before so that has the history.

## Build

Build with,

    sudo apt-get install -y \
          autoconf automake build-essential libtool
    autoreconf --install --force
    ./configure --prefix=$PWD/out
    make -j$(nproc)
    make install

There should be libraries in out/lib and tests in out/bin.

## Code

See the individual directories eg. for linked list see ll/*.[ch]. For example
usage see the _test.c files in each lib directory.

The specific libraries are,

Library | Description
------- | -----------
**async_runner** | Provides a way to run code asynchronously similar as in other languages that supports it.
**bitmap** | Storage for quick setup/retrieval of bits
**db** | Interface to database that just wraps underlying data storage. This is disabled for now to avoid dependency.
**debug** | Functions to facilitate debugging.
**dpool** | Datapool that can be used to allocate memory once and then reuse it
**file** | Functions to work with files
**link** | Functions to link datas structures
**ll** | Linked list implementation
**log** | Logging functions
**que** | Queue implementation
**sbuf** | String buffer implementation
**sock_serv** | Library to build socket servers with
**sys** | Wrapper for thread so program could possibly be used where pthreads aren't suppported
**wrap** | Wrappers for memory allocation function for easier memory debugging

## TODO

- The tests has to be improved, output isn't informative without looking at the
source code and most just run in a loop and never end.
