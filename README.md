# docker-webgrind

[Webgrind](https://github.com/jokkedk/webgrind) is a [Xdebug](http://www.xdebug.org)
profiling web frontend in PHP5. It implements a subset of the features of [kcachegrind](http://kcachegrind.sourceforge.net/cgi-bin/show.cgi).
This is a [docker](https://www.docker.io) image that eases setup.

[![](http://jokke.dk/media/2008-webgrind/webgrind_small.png)](http://jokke.dk/media/2008-webgrind/webgrind_large.png)

## Usage

This docker image is available as a [trusted build on the docker index](https://index.docker.io/u/clue/webgrind/).
Using this image for the first time will start a download automatically.
Further runs will be immediate, as the image will be cached locally.

The recommended way to run this container looks like this:

```bash
$ sudo docker run -d -p 80:80 clue/webgrind
```

This will start the webgrind container in a detached session in the background and will expose
its HTTP port. So you can now browse to:

http://localhost/

This container is disposable, as it doesn't store any sensitive information at all.
If you don't need it anymore, you can `stop` and `remove` it.
