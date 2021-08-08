# cargs

[![CodeFactor](https://www.codefactor.io/repository/github/snowapril/cargs/badge)](https://www.codefactor.io/repository/github/snowapril/cargs)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/0a9769e2c95d4efba8c26196b882ad27)](https://www.codacy.com/gh/Snowapril/cargs/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Snowapril/cargs&amp;utm_campaign=Badge_Grade)
[![Ubuntu github action](https://github.com/Snowapril/cargs/actions/workflows/ubuntu.yml/badge.svg?branch=main)](https://github.com/snowapril/cargs/actions)
[![Window github action](https://github.com/Snowapril/cargs/actions/workflows/window.yml/badge.svg?branch=main)](https://github.com/snowapril/cargs/actions)
[![MacOS github action](https://github.com/Snowapril/cargs/actions/workflows/macos.yml/badge.svg?branch=main)](https://github.com/snowapril/cargs/actions)

## Demo
**TBA**

## Install Conan package manager (if you dont have)
```bash
pip3 install conan
```

## How to Build
```bash
git clone https://github.com/snowapril/cargs
cd cargs
mkdir build
conan install . -if build --build missing -s build_type=Release
cd build
cmake ..
cmake --build .
```

## dependency
*   doctest[>=2.4.6]

## License
<img align="right" src="http://opensource.org/trademarks/opensource/OSI-Approved-License-100x137.png">

The class is licensed under the [MIT License](http://opensource.org/licenses/MIT):

Copyright (c) 2021 Snowapril
*   [Jihong Shin](https://github.com/Snowapril)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
