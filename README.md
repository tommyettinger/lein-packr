# packr

A leiningen plugin to bundle a JRE with an uberjar using Packr.

## Usage

Put `[clj.lein/packr "0.1.0-SNAPSHOT"]` into the `:plugins` vector of your project.clj.

To run, use

    $ lein packr

And then you can wait as it downloads a JRE for each of Windows, Linux (64-bit only), and Mac OS X from [alexkasko's builds](https://github.com/alexkasko/openjdk-unofficial-builds).
The time spent can be reduced by using
    
    $ lein packr windows
    
Which would only download a JRE for and generate an executable for the windows platform.  You can also use `linux` or `mac` in place of `windows` to only download that platform.  These JREs are cached in `~/.lein-packr-cache/` or the equivalent subdirectory of the user's home folder when run on Windows.  Currently minimization is not great, and you can't pass long arguments to the JVM (`-XX:+TieredCompilation` would be really handy but would only "work" if I upgraded to Packr 1.3, which isn't officially released as of January 18 2015, and breaks any non-Java projects with Packr anyway).  I hope this works for someone!

## License

Copyright © 2014 Tommy Ettinger

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
