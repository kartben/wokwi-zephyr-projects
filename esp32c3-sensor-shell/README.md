# esp32c3-sensor-shell

This is a Wokwi demo project for ESP32-C3 exposing a basic Zephyr shell.

To build the code yourself (assuming you're running from a Zephyr workspace containing the PR
above):

```bash
west build -p auto -b esp32c3_devkitm ./samples/sensor/sensor_shell -- \
     -DDTC_OVERLAY_FILE="<xxx>/boards/esp32c3_devkitm.overlay" \
     -DEXTRA_CONF_FILE="<xxx>/boards/esp32c3_devkitm.conf"
```

When the simulation is running, you can e.g. get a reading from the MPU6050 sensor by typing:

```
sensor get mpu6050@68
```