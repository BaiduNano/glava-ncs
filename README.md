
<img align="left" width="200" height="200" src="https://thumbs.gfycat.com/DefiantInformalIndianspinyloach-size_restricted.gif" />

**glava-ncs** is modified GLava streamlined to to run Roonil's NCS_Spectrum_GLava.

**Compiling:**

```bash
$ git clone https://github.com/jarcode-foss/glava
$ cd glava
$ meson build --prefix /usr
$ ninja -C build
$ sudo ninja -C build install
$ glava-ncs -m ncs
```

**Requirements:**

- X11 (Xext, Xcomposite, & Xrender)
- PulseAudio
- Linux or BSD
- libBlocksRuntime if compiling with Clang

**Additional compile time requirements:**

- Meson
- OBS (disable with `-Dobs=false`)

**Optional requirements:**

- GLFW 3.1+ (optional, enable with `-Dglfw=true`)

**All configurations are available on GLava's documentations.**

**Credits & Acknowledgements**

GLava: The original lightweight OpenGL audio spectrum visualizer.
https://github.com/jarcode-foss/glava

NCS_Spectrum_GLava: The configuration that served as the primary inspiration and starting point for the custom aesthetic.
https://github.com/Roonil/NCS_Spectrum_GLava

## Licensing

GLava is licensed under the terms of the GPLv3, with the exemption of `khrplatform.h`, which is licensed under the terms in its header. GLava includes some (heavily modified) source code that originated from [cava](https://github.com/karlstav/cava), which was initially provided under the MIT license. The source files that originated from cava are the following:

- `[cava]/input/fifo.c -> [glava]/fifo.c`
- `[cava]/input/fifo.h -> [glava]/fifo.h`
- `[cava]/input/pulse.c -> [glava]/pulse_input.c`
- `[cava]/input/pulse.h -> [glava]/pulse_input.h`

The below copyright notice applies for the original versions of these files:

`Copyright (c) 2015 Karl Stavestrand <karl@stavestrand.no>`

GLava also contains GLFFT, an excellent FFT implementation using Opengl 4.3 compute shaders. This was also initiallly provided under the MIT license, and applies to the following source files (where `*` refers to both `hpp` and `cpp`):

- `glfft/glfft.*`
- `glfft/glfft_common.hpp`
- `glfft/glfft_gl_interface.*`
- `glfft/glfft_interface.hpp`
- `glfft/glfft_wisdom.*`

The below copyright notice applies for the original versions of these files:

`Copyright (c) 2015 Hans-Kristian Arntzen <maister@archlinux.us>`

**The noted files above are all sublicensed under the terms of the GPLv3**. The MIT license is included for your convenience and to satisfy the requirements of the original license, although it no longer applies to any code in this repository. You will find the original copyright notice and MIT license in the `LICENSE_ORIGINAL` file for cava, or `glfft/LICENSE_ORIGINAL` for GLFFT.

The below copyright applies for the modifications to the files listed above, and the remaining sources in the repository:

`Copyright (c) 2017 Levi Webb`
