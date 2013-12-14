chumby8-linux-patches
=====================

Patches to make Chumby 8 work with newer mainline Linux kernels.

This probably doesn't work with a standard Chumby 8 root filesystem. My goal is to create a new custom root filesystem completely from scratch.

Inside the Linux directory, apply these patches in order:

```
for i in `ls ../chumby8-linux-patches/patches`; do
    patch -Np1 -i ../chumby8-linux-patches/patches/$i
done
```

Use the supplied chumby8-defconfig as your .config file and compile it. You will probably need to customize u-boot to load this kernel image instead of the kernel stored inside the SD card.
