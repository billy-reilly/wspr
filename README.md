[![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#)

# WSPR
WebSocket proxy for post http requests. Perfect for testing purposes/mocks 🚀

![wssExample](https://user-images.githubusercontent.com/2823336/88941927-814ad280-d281-11ea-8624-9637c13ee868.jpg)

### Installation

```
npm i -g wspr
```

### Usage

Just run
```
wspr
```

after, you will see output with 2 urls:
```
WebSocket server started ws://localhost:3005
HTPP proxy server started http://localhost:3006
```

### Broadcast message to clients: 
To broadcast message to clients send a  post requests with a string/json body (via postman or curl) to http enpoint provided
on the previous step.

```
curl -d "{"hello": "world"}" -X POST http://localhost:3006
```

### Websocket over secure connection

If you want to run the websocket server over a secure connection, follow these steps:

1. create self signed certificates: https://letsencrypt.org/docs/certificates-for-localhost/#making-and-trusting-your-own-certificates

2. trust the self signed certs, eg on mac: https://tosbourn.com/getting-os-x-to-trust-self-signed-ssl-certificates/

3. pass the paths to the certificate and key using the `--cert` and `--key` CLI args, eg: 

```bash
wspr --cert=./localhost.crt --key=./localhost.key
```

4. you should see the websocket is now running over wss:

```
WebSocket server started wss://localhost:3005
```

## Enjoy 🚀🥤
