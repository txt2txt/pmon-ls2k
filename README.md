# pmon-ls2k
Universal PMON source for LS2K targets

## Supported targets
- ls2k-pi2
- ls2k-edu

## How to compile
Set up toolchain according to [Loongson's guide](http://www.loongnix.org/index.php/PMON%E7%BC%96%E8%AF%91%E6%96%B9%E6%B3%95).
```
# Enter the source directory
cd zloader.ls2k-pi2 # Replace with your target
make cfg
make tgt=rom
make dtb
```
Please flash generated `gzrom-dtb.bin`.

## Boot protocol
This PMON support two boot protocols.
When env variable `oldpmon` is set (default behaviour), it will use loongson-3 style boot protocol, which is designed for universal kernel. Otherwise it will use Loongnix's DeviceTree boot protocol.  
