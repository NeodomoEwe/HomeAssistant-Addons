# Hass.io Add-on: Dahua VTO to MQTT Broker

Sends Dahua Intercom events to the MQTT Broker

![Supports aarch64 Architecture][aarch64-shield] ![Supports amd64 Architecture][amd64-shield] ![Supports armhf Architecture][armhf-shield] ![Supports armv7 Architecture][armv7-shield] ![Supports i386 Architecture][i386-shield]

## Installation

The installation of this add-on is straightforward and easy to do.

1. Navigate in your Home Assistant frontend to **Hass.io** -> **Add-on Store**.
2. Add a new repository by URL `https://github.com/NeodomoEwe/HomeAssistant-Addons`
3. Find the "DahuaVTO2MQTT" add-on and click it.
4. Click on the "INSTALL" button.

## How to use

To use this add-on, you need to supply the config for your intercom and MQTT Broker

- Requires you to use one of the supported Dahua Intercoms
- Requires you to run a local MQTT server
- [DahuaVTO2MQTT's documentation][documentation]


## Configuration

Add-on configuration:

```json
{
    "intercom": {
      "host": "192.168.1.110",
      "ssl": false,
      "username": "admin",
      "password": "admin"
    },
    "mqtt": {
      "host": "core-mosquitto",
      "port": "1883",
      "username": "homeassistant",
      "password": "homeassistant",
      "topic_prefix": "DahuaVTO"
    }
}
```

## Known issues and limitations

- None. Let me know.

## Credits
Using [riogrande75's][original-author] PHP code that connects your intercom and publishes events via MQTT broker.
Thanks to [troykelly's][original-addon-author].
Thanks to [elad-bar's][current-addon-author].
