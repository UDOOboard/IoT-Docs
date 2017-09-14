# UDOO IoT Documentation

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](https://github.com/UDOOboard/X86-Docs/LICENSE)

Travis build status: [![Build Status](https://travis-ci.org/UDOOboard/IoT-Docs.svg?branch=master)](https://travis-ci.org/UDOOboard/IoT-Docs)

## Build the documentation locally
On PHP7+ install XML and mbstring modules:

    sudo apt-get install php7.0-xml php7.0-mbstring

Then build the documentation with

    ./daux.phar && ( cd static; cp -rp ../img .)

To serve the documentation from a development webserver, run

    cd static && php -S localhost:8080


