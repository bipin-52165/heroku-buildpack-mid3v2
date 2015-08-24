Heroku buildpack: mid3v2
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for using [mid3v2](http://manpages.ubuntu.com/manpages/utopic/man1/mid3v2.1.html) in your project. 

mid3v2 build is a custom vulcan build downloaded from (manpages.ubuntu.com/manpages.gz/utopic/man1/mid3v2.1.gz)

It doesn't do anything else, so to actually compile your app you should use [buildpack-mid3v2](https://github.com/soft-dave/heroku-buildpack-mid3v2) to combine it with a real buildpack.

Usage
-----
To use this buildpack, you should prepare .buildpacks file that contains this buildpack url and your real buildpack url.  

    $ ls
    .buildpacks
    ...
    
    $ cat .buildpacks
    https://github.com/soft-dave/heroku-buildpack-mid3v2

    $ heroku create --buildpack https://github.com/soft-dave/heroku-buildpack-mid3v2

    $ git push heroku master
    ...

You can verify installing ffmpeg by following command.

    $ heroku run "mid3v2"
