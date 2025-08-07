With the view to connect our services to your LNS, we need a connector. A
MQTT connector allow any LNS to push data using MQTT protocol to our server.

## Setup your client

When you'll setup your LNS to push data to our MQTT broker, you'll need to
configure your client in the following way :

* broker: `websocket.iot.fr-par.scw.cloud:443` ;
* protocol: `WSS` ;
* username: `{username}` ;
* uplink topic: `{guid}/uplink/` ;
* downlink topic: `{guid}/downlink/`.

For now, connectors have only been tested with [Actility](https://actility.com).