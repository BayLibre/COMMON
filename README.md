# Common Source Folder to building CI images #

With Kernel CI we will want to build a given kernel tag
for various platforms. We do not want to git clone the kernel
over and over. Let's make the different build craters use a
common git clone area for those gits that support 'O=' type
if SRC/BUILD splitting.

* kernel
* u-boot
* etc..

# How this is used #

ACME, ODROID, JUNO (etc...) setup scripts will seek after "~/COMMON" and try use
~/COMMON/linux as KERNEL_SRC location when possible.

# How to pull this stuff #

```
repo init -u git@github.com:Baylibre/manifests -m common/default.xml
repo sync
```

