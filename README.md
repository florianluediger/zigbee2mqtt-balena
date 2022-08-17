# Smart Office Zigbee2MQTT

This repository contains the configuration of the balena container that runs Zigbee2MQTT in the Smart Office.

To run this container in Balena, do the following:

On your Balena host set `ZIGBEE2MQTT_CONFIG_MQTT_SERVER` to the mqtt server URL e.g. `mqtt://someting.iot.eu-central-1.amazonaws.com:8883`

On your Balena host create certificate files:

- `echo "<certificate content>" > /var/lib/docker/volumes/1_zigbee2mqtt-data/_data/AmazonRootCA1.pem`
- `echo "<certificate content>" > /var/lib/docker/volumes/1_zigbee2mqtt-data/_data/private.pem.key`
- `echo "<certificate content>" > /var/lib/docker/volumes/1_zigbee2mqtt-data/_data/certificate.pem.crt`