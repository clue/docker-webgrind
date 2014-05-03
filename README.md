# docker-webgrind

[Webgrind](https://github.com/jokkedk/webgrind) is a [Xdebug](http://www.xdebug.org)
profiling web frontend in PHP5. It implements a subset of the features of [kcachegrind](http://kcachegrind.sourceforge.net/cgi-bin/show.cgi).
This is a [docker](https://www.docker.io) image that eases setup.

[![](http://jokke.dk/media/2008-webgrind/webgrind_small.png)](http://jokke.dk/media/2008-webgrind/webgrind_large.png)

## Build

```bash
$ git clone https://github.com/clue/docker-webgrind.git
$ cd docker-webgrind
$ sudo docker build -t webgrind .
```

### Running

This container is disposable, as it doesn't store any sensitive
information at all.

#### Running Webgrind temporarily

```bash
$ sudo docker run -it --rm -p 80:80 webgrind
```

#### Running Webgrind daemonized

```bash
$ sudo docker run -d -p 80:80 webgrind
```

### Accessing your webinterface

The above examples expose the Webgrind webinterface on port 80, so that you can browse to:

http://localhost/

