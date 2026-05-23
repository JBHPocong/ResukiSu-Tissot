# ReSukiSU-Tissot

Custom kernel for Xiaomi Mi A1 (Tissot) with integrated ReSukiSU v4.1.0

## Features
- Linux kernel 4.9
- ReSukiSU v4.1.0 (Manual Hook)
- Full manual hook integration:
  - ksu_handle_execveat (do_execveat_common)
  - ksu_handle_faccessat
  - ksu_handle_stat
  - ksu_handle_newfstat_ret
  - ksu_handle_fstat64_ret
  - ksu_handle_sys_reboot
- Built for Non-GKI
- Supports: MKSU, RKSU, KOWSU, SukiSU-Ultra, ReSukiSU

## Build
```bash
export ARCH=arm64
export CROSS_COMPILE=aarch64-linux-gnu-
make O=out tissot_defconfig
make -j$(nproc) O=out

