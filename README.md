[![Travis build status](https://travis-ci.org/nicosmaris/example-groovy.png?branch=master)](https://travis-ci.org/nicosmaris/example-groovy) [![codecov.io](http://codecov.io/github/nicosmaris/example-groovy/coverage.svg?branch=master)](https://codecov.io/gh/nicosmaris/example-groovy/branch/master) 

Groovy project with selenium tests. The only supported browser for the moment is Firefox 45.


To run it locally, you need first to install:

ubuntu 16.10
sudo apt-get install -y xvfb openjdk-8-jdk
unzip ui/firefox-45.5.1-esr.zip -d ui

To run it locally, you need:

export DISPLAY=':99.0'
Xvfb :99 -screen 0 1024x768x24 > /dev/null 2>&1 &
mvn test
  

The specific firefox and the specific selenium version are more stable than the latest released ones.

For parallel UI tests, make sure that the environment property DISPLAY of the instance of FirefoxBinary matches with the parameter of the executable Xvfb
