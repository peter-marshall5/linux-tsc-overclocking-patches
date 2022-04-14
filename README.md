# linux-tsc-overclocking-patches

Kernel patches to keep TSC clocksource functionality when using software overclocking

tsc-khz.patch: Allows manually specifying a TSC frequency on boot (in KHz) via "tsc_khz=x"

tsc-manual-calibrate.patch: Creates a sysfs entry at /sys/devices/system/cpu/cpu0/tsc_refine_khz. Reading this file causes the kernel to recalibrate the TSC frequency.

Make sure to pass "clocksource=tsc tsc=reliable" on the kernel cmdline when using these patches.
