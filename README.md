# XVega

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/QuantStack/xvega/stable?urlpath=lab%2Ftree%2Fnotebooks%2Fdemo.ipynb)
[![Build Status](https://github.com/QuantStack/xvega/workflows/CMake%20Build/badge.svg)](https://github.com/QuantStack/xvega/actions)

A C++ backend for vega-lite (https://vega.github.io/vega-lite/).

**This is an early developer preview under active development.**

## Building from source

To build the package from source, execute the following:

```
mkdir build

cd build

cmake -DCMAKE_INSTALL_PREFIX=$CONDA_PREFIX .. -DCMAKE_BUILD_TYPE=Release

make -j ${CPU_COUNT} install
```

Use the library by including the following header:

```
#include "xvega/xvega.hpp"
```

## Dependencies

`xvega` depends on [xtl](https://github.com/xtensor-stack/xtl), 
[nlohmann json](https://github.com/nlohmann/json) and the 
[xproperty](https://github.com/jupyter-xeus/xproperty) libraries:

|  `xvega`  |  `xtl`  |  `nlohmann json`  |  `xproperty`  |
|-----------|---------|-------------------|---------------|
|  master   | ^0.6.11 |       ^3.7.3      |    ^0.10.4    |
|  0.0.4    | ^0.6.11 |       ^3.7.3      |    ^0.10.1    |

Note: Please make sure to have `jupyterlab` and `xeus-cling` installed in order to use `XVega` as a standalone library.

Also, `XVega` only works with `jupyterlab` (and not `jupyter notebook`) as of now.

## License

We use a shared copyright model that enables all contributors to maintain the copyright on their contributions.

This software is licensed under the BSD-3-Clause license. See the LICENSE file for details.
