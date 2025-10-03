With the view to connect our services to your LNS, we need a connector. A
Webhook connector allow any LNS to push data using HTTPS protocol to our server.

## Setup your client

When you'll setup your LNS to push data to our HTTPS server, you'll need to
configure your LNS in different ways, depending on its underlying technology.

### The Things Network

If you use a TTN or TTI (The Things Industry) LNS, you'll have to configure
a new webhook the following way:

* `Webhook ID`: Fill in with the ID you want, `abeeway-webhook` for this example ;
* `Webhook format`: `JSON` ;
* `Base URL`: `https://configurationmanager.abeeway.io/api/v1/lns/tti` ;
* `Downlink API Key`: copy the API key you'll generate to allow Abeeway Server to
  push downlink (see below)
* `Additional headers`:
  * `X-Apikey`: `{guid}`.
* `Enabled Event Types`: don't forget to enable `Uplink message`.

You'll need to generate an API Key to allow the server to push downlink. For
that, you'll have to select `API Keys` menu, then click `+ Add API Key`, set
a name and sexpiration date, select `Grant individual rights`, and check 
`write downlink application traffic`. Once you'll click on `Create API Key`,
you'll be able to copy the newly generated API Key. For example:
`NNSXS.DSPAQ2WFHSEFDF3TMJWKWO6LMXBOH7GIUHCVXWI.S6QWYPJ5K347TI4Y6IRYA3FX5MG336GL2XFB3BNLI6RF4G613UFQ`.
It's the API Key that you'll have to copy to `Downlink API Key`, when creating
your webhook.