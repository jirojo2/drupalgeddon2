# Drupalgeddon 2

MSF exploit module for Drupalgeddon 2 (CVE-2018-7600 / SA-CORE-2018-002)

Drupal before 7.58, 8.x before 8.3.9, 8.4.x before 8.4.6, and 8.5.x before 8.5.1 allows remote attackers to execute arbitrary code because of an issue affecting multiple subsystems with default or common module configurations.

The module can load msf PHP arch payloads, using the php/base64 encoder.

The resulting RCE on Drupal looks like this:

```
php -r 'eval(base64_decode(#{PAYLOAD}));'
```

Developed during Madrid Hack&Beers.

## Disclaimer

This module is provided for academic and penetration testing professional use only.

## References

* [dreadlocked/Drupalgeddon2](https://github.com/dreadlocked/Drupalgeddon2) exploit ported to ruby and exploitation research

* [a2u/CVE-2018-7600](https://github.com/a2u/CVE-2018-7600) original exploit PoC

* [Checkpoint research](https://research.checkpoint.com/uncovering-drupalgeddon-2/) by Eyal Shalev, Rotem Reiss and Eran Vaknin

## MIT License

Copyright (c) 2018 José Ignacio Rojo

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
