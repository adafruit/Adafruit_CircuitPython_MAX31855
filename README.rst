Introduction
============

.. image:: https://readthedocs.org/projects/adafruit-circuitpython-MAX31855/badge/?version=latest
    :target: https://circuitpython.readthedocs.io/projects/MAX31855/en/latest/
    :alt: Documentation Status

.. image:: https://badges.gitter.im/adafruit/circuitpython.svg
    :target: https://gitter.im/adafruit/circuitpython?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge
    :alt: Gitter


Dependencies
=============

This driver depends on the `Bus Device
<https://github.com/adafruit/Adafruit_CircuitPython_BusDevice>`_ library.
Please ensure is is also available on the CircuitPython filesystem.  This is
easily achieved by downloading `a library and driver bundle
<https://github.com/adafruit/Adafruit_CircuitPython_Bundle>`_.


Usage Notes
===========

Of course, you must import the library to use it:

.. code:: python

    import adafruit_max31855

You also need to create an SPI interface object, and a pin object for the
chip select pin. You can use any pin for the CS, but we use D5 here:


.. code:: python

    from busio import SPI
    from digitalio import DigitalInOut
    import board

    spi = SPI(clock=board.SCK, MISO=board.MISO, MOSI=board.MOSI)
    cs = DigitalInOut(board.D5)

Next, just create the sensor object:

.. code:: python

    sensor = adafruit_max31855.MAX31855(spi, cs)

And you can start making measurements:

.. code:: python

    print(sensor.temperature)

The temperature is read in degrees Celsius (°C). You have to convert it to
other units yourself, if you need it.


Contributing
============

Contributions are welcome! Please read our `Code of Conduct
<https://github.com/adafruit/Adafruit_CircuitPython_MAX21855/blob/master/CODE_OF_CONDUCT.md>`_
before contributing to help this project stay welcoming.


API Reference
=============

.. toctree::
   :maxdepth: 2

   api
