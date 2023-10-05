# rpi_pico-helloworld

This is a Wokwi demo project for RP2040 running Zephyr Hello World example.

```bash
west build -p auto -b rpi_pico samples/hello_world -- \
     -DDTC_OVERLAY_FILE="<xxx>/boards/rpi_pico.overlay" \
     -DEXTRA_CONF_FILE="<xxx>/boards/rpi_pico.conf"
```