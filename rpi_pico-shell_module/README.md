# rpi_pico-shell_module

This is a Wokwi demo project for RP2040 running Zephyr "shell_module" example.

Note: Non-functional as of 2023-10-05.

```bash
west build -p auto -b rpi_pico samples/subsys/shell/shell_module -- \
     -DDTC_OVERLAY_FILE="<xxx>/boards/rpi_pico.overlay" \
     -DEXTRA_CONF_FILE="<xxx>/boards/rpi_pico.conf"
```