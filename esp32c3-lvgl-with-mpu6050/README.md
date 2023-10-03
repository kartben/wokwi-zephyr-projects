# esp32c3-lvgl-with-mpu6050

This is a Wokwi demo project for ESP32-C3 DevkitM + ILI9341 + MPU6050.

This contains the binary files corresponding to the demo available at:
https://github.com/zephyrproject-rtos/zephyr/pull/63375 (hopefully soon merged upstream).

To build the code yourself (assuming you're running from a Zephyr workspace containing the PR
above):

```bash
west build -p auto -b esp32c3_devkitm .\samples\modules\lvgl\accelerometer_chart\ -- \
     -DDTC_OVERLAY_FILE="<xxx>/boards/esp32c3_devkitm.overlay" \
     -DEXTRA_CONF_FILE="<xxx>/boards/esp32c3_devkitm.conf"
```