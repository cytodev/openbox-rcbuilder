# [Openbox](http://openbox.org/) RCBuilder v1.0.0
This is a collection of split rc files and a build script to create semi-modular openbox rc's.

## Index
 - [Installation](#installation)
 - [Configuration](#configuration)
 - [Contributing](#contributing)
 - [License](#license)

## Installation
To install RCBuilder you need to make sure a few things are already present on your system. I'm guessing they already are, but just to be safe, these packages are needed:
 1. openbox
 2. bash

RCBuilder does not really care where you install it, so it does not matter where you clone it.

To clone this repo via ssh:
```shell
user@hostname:~$ git clone git@github.com:CytoDev/openbox-rcbuilder.git
```

Or via http:
```shell
user@hostname:~$ git clone https://github.com/CytoDev/openbox-rcbuilder.git
```

Congratiulations, you now own your very own copy of RCBuilder!

## Configuration
Before you can start using rcbuilder it is important to open the "build" file and change the path to the openbox config directory. If you do not set this directory correctly, the entire script is pretty much useless. The variable to change currently resides on line 3 and looks like this:
```shell
OPENBOXDIR="/your-full-path/to-the-config/of/openbox"
```

The openbox sections found in a default `rc.xml` are split into multiple files in the `config` folder (main folder of this repository) and numbered by order of import (e.g. `00_resistance.xml`, `05_focus.xml`). To change the theme of your openbox setup you would change the contents of `15_theme.xml` and rebuild with the bundled "build" file (not an official build file like you would expect it to be, it's just a shell script).

You can also take a look at my own (compiled) configuration in the `presets` directory. Feel free to use it, modify it, etc. but if you made something awesome, please consider filing a pull request to place it in the `presets` directory of this repository.

__note:__
All config files included in this repo are emptied (they have no values between the xml tags). To start using RCBuilder the way it was intended I suggest seperating your current openbox rc into the files included in config - or just let openbox crash because of the empty values...

## Contributing
You are free to modify the existing "build" file to make it even more modular. I do not want to have millions of custom rc's hanging around in this repo though, so please use the `presets` directory for those (if you feel like sharing them).

## License
```
The MIT License (MIT)

Copyright (c) 2016 Roel Walraven

Permission is  hereby granted,  free of  charge, to any person obtaining a
copy of this software and associated documentation files (the "Software"),
to deal in  the Software without restriction, including without limitation
the  rights to use,  copy, modify, merge, publish, distribute, sublicense,
and/or sell  copies of the  Software, and to  permit persons  to whom  the
Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT  NOT LIMITED TO THE WARRANTIES  OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR  PURPOSE  AND NONINFRINGEMENT. IN  NO EVENT SHALL
THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER  IN AN ACTION  OF  CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF  OR  IN  CONNECTION WITH  THE SOFTWARE  OR  THE  USE OR OTHER
DEALINGS IN THE SOFTWARE.
```