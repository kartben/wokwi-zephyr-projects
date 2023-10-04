# esp32s3-sensor-shell

This is a Wokwi demo project for ESP32-S3 exposing a basic Zephyr shell.
ANSI/VT100 colors are disabled to look better on Wokwi's terminal.

To build the code yourself (assuming you're running from a Zephyr workspace containing the PR
above):

```bash
west build -p auto -b esp32s3_devkitm ./samples/sensor/sensor_shell -- \
     -DDTC_OVERLAY_FILE="<xxx>/boards/esp32s3_devkitm.overlay" \
     -DEXTRA_CONF_FILE="<xxx>/boards/esp32s3_devkitm.conf"
```