# esp32s3-lvgl-with-encoder

This is a Wokwi demo project for ESP32-S3 DevkitM running the Zephyr LVGL sample.

To build the code yourself (assuming you're running from a Zephyr workspace containing the PR
above):

```bash
west build -p auto -b esp32s3_devkitm ./samples/subsys/display/lvgl -- \
     -DDTC_OVERLAY_FILE="<xxx>/boards/esp32s3_devkitm.overlay" \
     -DEXTRA_CONF_FILE="<xxx>/boards/esp32s3_devkitm.conf"
```