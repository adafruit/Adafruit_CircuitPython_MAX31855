Introduction
=============

.. image:: https://readthedocs.org/projects/adafruit-circuitpython-max31855/badge/?version=latest
    :target: https://docs.circuitpython.org/projects/max31855/en/latest/
    :alt: Documentation Status

.. image:: https://img.shields.io/discord/327254708534116352.svg
    :target: https://adafru.it/discord
    :alt: Discord

.. image:: https://github.com/adafruit/Adafruit_CircuitPython_MAX31855/workflows/Build%20CI/badge.svg
    :target: https://github.com/adafruit/Adafruit_CircuitPython_MAX31855/actions/
    :alt: Build Status

CircuitPython driver for the `MAX31855 Thermocouple Amplifier Breakout <https://www.adafruit.com/product/269>`_

Dependencies
=============
This driver depends on:

* `Adafruit CircuitPython <https://github.com/adafruit/circuitpython>`_
* `Bus Device <https://github.com/adafruit/Adafruit_CircuitPython_BusDevice>`_

Please ensure all dependencies are available on the CircuitPython filesystem.
This is easily achieved by downloading
`the Adafruit library and driver bundle <https://github.com/adafruit/Adafruit_CircuitPython_Bundle>`_.

Installing from PyPI
====================

On supported GNU/Linux systems like the Raspberry Pi, you can install the driver locally `from
PyPI <https://pypi.org/project/adafruit-circuitpython-max31855/>`_. To install for current user:

.. code-block:: shell

    pip3 install adafruit-circuitpython-max31855

To install system-wide (this may be required in some cases):

.. code-block:: shell

    sudo pip3 install adafruit-circuitpython-max31855

To install in a virtual environment in your current project:

.. code-block:: shell

    mkdir project-name && cd project-name
    python3 -m venv .env
    source .env/bin/activate
    pip3 install adafruit-circuitpython-max31855

Usage Example
==============

Of course, you must import the library to use it:

.. code:: python3

    import adafruit_max31855

You also need to create an SPI interface object, and a pin object for the
chip select pin. You can use any pin for the CS, but we use D5 here:


.. code:: python3

    from digitalio import DigitalInOut
    import board

    spi = board.SPI()
    cs = DigitalInOut(board.D5)

Next, just create the sensor object:

.. code:: python3

    sensor = adafruit_max31855.MAX31855(spi, cs)

And you can start making measurements:

.. code:: python3

    print(sensor.temperature)

The temperature is read in degrees Celsius (°C). You have to convert it to
other units yourself, if you need it.


Documentation
=============

API documentation for this library can be found on `Read the Docs <https://docs.circuitpython.org/projects/max31855/en/latest/>`_.

Contributing
============

Contributions are welcome! Please read our `Code of Conduct
<https://github.com/adafruit/Adafruit_CircuitPython_MAX21855/blob/main/CODE_OF_CONDUCT.md>`_
before contributing to help this project stay welcoming.

Documentation
=============

For information on building library documentation, please check out `this guide <https://learn.adafruit.com/creating-and-sharing-a-circuitpython-library/sharing-our-docs-on-readthedocs#sphinx-5-1>`_.
