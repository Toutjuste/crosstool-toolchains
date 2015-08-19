Raspberry-pi toolchain on 64 bits host
===

- Run ``mkdir rpi-host-64-conf && cd rpi-host-64-conf``
- Run ``ct-ng menuconfig``

Now, Check the following options:

<h4>Paths and misc options:</h4>

- Check <b>Try features marked as EXPERIMENTAL</b>
- Check <b>Force downloads</b>
- Set <b>Number of parallel jobs</b> to your number of cores <b>x 1.5</b> (set to <b>6</b> if you have a quad-core CPU)

<h4>Target options:</h4>

- Set <b>Target Architecture</b> to ``arm``
- Set <b>Endianness</b> to ``Little endian``
- Set <b>Bitness</b> to ``32-bit``
- Set <b>Architecture level</b> to ``armv6zk``
- Set <b>Emit assembly for CPU</b> to ``arm1176jzf-s``
- Set <b>Tune for CPU</b> to ``arm1176jzf-s``
- Set <b>Use specific FPU</b> to ``vfp``
- Set <b>Floating point</b> to ``hardware (FPU)``
- Set <b>Default instruction set mode</b> to ``arm``
- Check <b>Use EABI</b>

<h4>Toolchain options:</h4>

- Set <b>Tuple's vender string</b> to ``rpi``

<h4>Operating system:</h4>

- Set <b>Target OS</b> to ``linux``
- Set <b>Linux kernel version</b> to ``4.0.4 (stable)``

<h4>Binary utilities:</h4>

- Set <b>Binary format</b> to ``ELF``
- Check <b>Show Linaro versions</b>
- Set <b>binutils version</b> to ``linaro-2.25.0-2015.01-2``

<h4>C-library:</h4>

- Set <b>C library</b> to ``glibc``
- Check <b>Show Linaro versions</b>
- Set <b>glibc version</b> to ``Linaro 2.20-2014.11``

<h4>C compiler:</h4>

- Check <b>Show Linaro versions</b>
- Set <b>gcc version</b> to ``linaro-4.9-2015.03``
- Check <b>C++</b>
- Set <b>gcc extra config</b> to ``--with-float=hard``
- Check <b>Link libstdc++ statically into gcc binary</b>


<h4>Debug facilities:</h4>

- Check <b>dmalloc, duma, gdb, ltrace, strace</b>
- For <b>gdb</b> check:
  - <b>Cross-gdb</b>
  - <b>Enable python scripting</b>
  - <b>gdbserver</b>
  - <b>Build a static gdbserver</b>
  - <b>Show Linaro versions</b> and set <b>gdb version</b> to ``linaro-7.8-2014.09``

<h4>Companian libraries:</h4>

- Set <b>ISL version</b> to ``0.12.2``

Now run ``ct-ng build`` to build the toolchain and add ``"$HOME/x-tools/arm-rpi-linux-gnueabi/bin"`` to your <b>PATH</b> variable.



