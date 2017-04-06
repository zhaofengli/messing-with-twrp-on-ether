## Investigation
Use [my device tree](https://github.com/zhaofengli/android_device_nextbit_ether_twrp), with updated blobs and kernel.

### 1. System Vold without including `qseecomd`
```
cd recovery/root/sbin
rm *.so qseecomd
```
Build TWRP, decryption works, but `/system` cannot be mounted (`Failed to mount '/system' (Device or resource busy)`

Logs available under `no-qseecomd`

### 2. System Vold with `qseecomd` and all libs
Restore `qseecomd` and all libs. Build TWRP, decryption fails.

Logs available under `with-qseecomd-and-so`

