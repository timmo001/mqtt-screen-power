# MQTT Screen Power

MQTT Client written in Python for turning HDMI screen power on and off.
Made for the Rapsberry Pi 3B+ which is using a third-party touch screen which
 does not completely switch off the screen with screensaver / power saving

## Usage

- Copy `config.template.py` to `config.py` and change the properties to
 your MQTT setup/preferences

- Install `paho-mqtt`

  ```bash
  pip install paho-mqtt
  ```

- Run

  ```bash
  python paho-mqtt
  ```

## Example use in [Home Assistant](https://www.home-assistant.io)

```yaml
switch:
  - platform: mqtt
    name: "Touch Panel"
    icon: mdi:tablet
    command_topic: "screen/rpi"
    payload_on: 'on'
    payload_off: 'off'
```
