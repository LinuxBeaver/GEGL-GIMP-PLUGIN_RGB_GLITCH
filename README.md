# RGB Glitch - Make a RGB Glitch effect with this GIMP Plugin


Make an RGB Glitch effect on your image with this GIMP plugin by moving the red, green, and blue channel vertically and or horizontally independently.

Download ready binaries and code here

https://github.com/LinuxBeaver/GEGL-GIMP-PLUGIN_RGB_GLITCH/releases/


<img width="1332" height="796" alt="image" src="https://github.com/user-attachments/assets/c725f6df-d211-4c9a-aae3-46d157c0d8fa" />

<img width="1031" height="721" alt="image" src="https://github.com/user-attachments/assets/132b7a3e-b1df-40be-8f92-5c17dd16afc9" />



## Directory to put Binaries (They do NOT go in the normal plugins folder)

**Windows**
C:\Users\USERNAME\AppData\Local\gegl-0.4\plug-ins

**Linux** 
`~/.local/share/gegl-0.4/plug-ins`

**Linux (Flatpak)**
`~/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins`


Then Restart Gimp and go to Filters>Artistic and look for "RGB Glitch" or just search for it with /

GIMP 2.10 users will only find this in GEGL Operation drop down list and it will only work on 2.10 if they are using GEGL 0.4.50+, all normal windows builds of GIMP 2.10 ship with GEGL 0.4.48

## Compiling and Installing

on Linux run `./build_plugin_linux.sh `
or if on Windows `./build_plugin_windows.sh` with mysys2 installed

Explanation of what the build_plugin script is doing below or if you want to compile it manually without the auto compile script

### Linux

To compile and install you will need the GEGL header files (`libgegl-dev` on
Debian based distributions or `gegl` on Arch Linux) and meson (`meson` on
most distributions).

```bash
meson setup --buildtype=release build
ninja -C build

```

### Windows

The easiest way to compile this project on Windows is by using msys2.  Download
and install it from here: https://www.msys2.org/

Open a msys2 terminal with `C:\msys64\mingw64.exe`.  Run the following to
install required build dependencies:

```bash
pacman --noconfirm -S base-devel mingw-w64-x86_64-toolchain mingw-w64-x86_64-meson mingw-w64-x86_64-gegl
```

Then build the same way you would on Linux:

```bash
meson setup --buildtype=release build
ninja -C build
```

## More previews of this based plugin

<img width="1029" height="793" alt="image" src="https://github.com/user-attachments/assets/736e5eed-1b4b-4772-9801-1065c82215cf" />

<img width="1136" height="777" alt="image" src="https://github.com/user-attachments/assets/d966d7ee-2ce6-4c18-8376-fcd2c796cd8f" />




