# ESP32C3
notes on using ESP32C3

## Rust API

* Training: https://esp-rs.github.io/espressif-trainings/
* Training github repository https://github.com/esp-rs/espressif-trainings
* Rust Bluetooth https://github.com/persello/bluedroid
* Another Rust Bluetooth support https://github.com/pyaillet/esp-idf-ble
* https://github.com/rtic-rs/rtic - Real-Time Interrupt-driven Concurrency (RTIC) framework for ARM Cortex-M microcontrollers
* https://embassy.dev - The next-generation framework for embedded applications (works with ESP32 as well as RP Pico)
* Comparison of Embassy and RTIC  - https://cohost.org/jamesmunns/post/67555-should-i-use-embassy
* https://github.com/esp-rs/esp-wifi

## C API

ensure that python is configured so that `python` runs `python3`:

```
sudo ln -s /Library/Developer/CommandLineTools/usr/bin/python3 /Library/Developer/CommandLineTools/usr/bin/python
```

From: <https://github.com/espressif/esp-idf/releases>

```
cd ~/esp
git clone -b v5.0.1 --recursive https://github.com/espressif/esp-idf.git esp-idf-v5.0.1
cd ~/esp/esp-idf-v5.0.1
./install.sh
source export.sh
```

Then compile an example:

```
cd example/get-started/hello_world
idf.py set-target esp32c3
idf.py build
idf.py -p /dev/tty.usbmodem14201 flash
idf.py monitor
```

Monitor see: <https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-guides/tools/idf-monitor.html>

`Ctrl+]` - to exit monitor
