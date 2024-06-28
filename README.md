# VoidScreenshare
Browser-based screen share over WebRTC P2P connections. Adapted for local use.

Based on https://github.com/haojiezhe12345/ScreenShare-WebRTC

## Deploy
Deploy with docker. Example compose file provided. Put it behind a reverse proxy with HTTPS.

## Prerequisites
- Clone the source or download zip
- Have Node.js 20 installed (lower version may work, but not tested)

## Run
Install all required packages with:

```npm install```

Then run the main server with:

```node main.js```

## Usage
Host (source) page: ```/host.html```

Client (receiver) page: ```/client.html```

WebSocket signaling channel: ```/signal?name=<name>&type=<host|client>```

Peers list: ```/peers```

**To start streaming, the host and client should enter a common name.\
Once both sides are registered on the server, the stream will start.**

The stream is transmitted over P2P connections, so it's best used under LANs, or peers with open NAT.
