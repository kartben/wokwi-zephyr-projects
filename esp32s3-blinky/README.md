# esp32s3-blinky

This is a Wokwi demo project for ESP32-S3 running Zephyr Blinky.

Default sample has been ever so slightly modified to `print` info re: timing of the LED toggles.

```c
int main(void)
{
	int ret;
	bool led_state = false;

	if (!gpio_is_ready_dt(&led)) {
		return 0;
	}

	ret = gpio_pin_configure_dt(&led, GPIO_OUTPUT_INACTIVE);
	if (ret < 0) {
		return 0;
	}


	while (1) {
		ret = gpio_pin_toggle_dt(&led);
		if (ret < 0) {
			return 0;
		}

		led_state = !led_state;
		printf("LED state: %s @ %lld\n", led_state ? "ON" : "OFF", k_uptime_get());
		k_msleep(SLEEP_TIME_MS);
	}
	return 0;
}
```

To build the code yourself (assuming you're running from a Zephyr workspace containing the PR
above):

```bash
west build -p auto -b esp32s3_devkitm ./samples/basic/blinky -- \
     -DDTC_OVERLAY_FILE="<xxx>/boards/esp32s3_devkitm.overlay" \
     -DEXTRA_CONF_FILE="<xxx>/boards/esp32s3_devkitm.conf"
```