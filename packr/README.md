# packr

A leiningen plugin to bundle a JRE with an uberjar using Packr.

## Usage

Put `[clj.lein/packr "0.1.0-SNAPSHOT"]` into the `:plugins` vector of your project.clj.

To run, use

    $ lein packr

And then you can wait as it downloads a JRE for windows, Linux 32-bit, Linux 64-bit, and Mac OS X.
The time spent can be reduced by using
    
    $ lein packr windows
    
Which would only download a JRE for and generate an executable for the windows platform.

## License

Copyright © 2014 Tommy Ettinger

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
