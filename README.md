# Mesos Python Example

A slightly modified and stand alone variant of the Python examples
distributed with Apache Mesos.

## Why?

I found myself in a vagrant environment with Mesos already setup and
couldn't find Python examples and didn't want to rebuild
Mesos. Likewise, wanted to use as client from host without Mesos
setup. All of the Mesos examples I could find for Python seem to
require a full Mesos build.

## Running Example

1. Setup Mesos (see [Playa Mesos][playa] for instance)

1. Download

  ```bash
  git clone https://github.com/jmchilton/python-mesos-examples
  cd python-mesos-examples
  ```

1. Setup [virtualenv](https://pypi.python.org/pypi/virtualenv) for example

  ```bash
  sudo apt-get install python-virtualenv 
  virtualenv venv
  . venv/bin/activate
  easy_install http://downloads.mesosphere.io/master/ubuntu/14.04/mesos-0.19.0_rc2-py2.7-linux-x86_64.egg
  ```

  You will need to find the proper egg for your Mesos version and OS on [Mesosphere's Download Site](http://mesosphere.io/downloads/).


1. Run Example

   ```bash
   ./test-framework http://10.0.1.1:5050
   ```

   Here you will need to plugin your Mesos master URL - this happened to mine for [Playa Mesos][playa].


[playa]: https://github.com/mesosphere/playa-mesos
