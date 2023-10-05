# rpi_pico-blinky

This is a Wokwi demo project for RP2040 running Zephyr Blinky example.

```bash
west build -p auto -b rpi_pico samples/basic/blinky -- \
     -DDTC_OVERLAY_FILE="<xxx>/boards/rpi_pico.overlay" \
     -DEXTRA_CONF_FILE="<xxx>/boards/rpi_pico.conf"
```