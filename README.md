
Arduino Cryptography Library
============================

This distribution contains a libraries and example applications to perform
cryptography operations on Arduino devices.  They are distributed under the
terms of the MIT license.

This has been forked from https://github.com/rweather/arduinolibs in order
to extract Cryptographic library and give it modern Arduino library format.

The [documentation](http://rweather.github.io/arduinolibs/crypto.html)
contains more information on the libraries and examples.

This repository used to contain a number of other examples and libraries
for other areas of Arduino functionality but most users are only interested
in the cryptography code.  The other projects have been moved to a
separate [repository](https://github.com/rweather/arduino-projects) and
only the cryptography code remains in this repository.

For more information on these libraries, to report bugs, or to suggest
improvements, please contact the author Rhys Weatherley via
[email](mailto:rhys.weatherley@gmail.com).

Recent significant changes to the library
-----------------------------------------

Mar 2022:

* HMAC-BLAKE2b and HMAC-BLAKE2s were giving incorrect results when the
message being authenticated was zero-length.

Jan 2022:

* All-in-one hmac() function in Hash.h for simplified HMAC computations.
* New API for the HKDF hash-based key derivation function.
* Make the ESP32 version of AES less dependent on include file locations.

Apr 2018:

* Acorn128 and Ascon128 authenticated ciphers (finalists in the CAESAR AEAD
  competition in the light-weight category).
* Split the library into Crypto (core), CryptoLW (light-weight), and
  CryptoLegacy (deprecated algorithms).
* Tiny and small versions of AES for reducing memory requirements.
* Port the library to ESP8266 and ESP32.
* Make the RNG class more robust if the app doesn't call begin() or loop().

Nov 2017:

* Fix the AVR assembly version of Speck and speed it up a little.
* API improvements to the RNG class.
