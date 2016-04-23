# OAuth.io Demo

This repo contains example implementations of the [OAuth.io JavaScript SDK](https://github.com/oauth-io/oauth-js)

## Installation

```bash
$ git clone https://github.com/grokify/oauth-io-demo
$ cd oauth-io-demo
$ sh bower_install.sh
```

## Configuration

```bash
$ cd public
$ cp config-sample.js config.js
$ vi config.js
```

## Usage

Run the public directory as static HTML. The following example uses `http-server`.

```bash
$ npm install -g http-server
$ http-server public
```

Then visit the homepage and navigate to each provider page:

```
http://localhost:8080/providers/dropbox
http://localhost:8080/providers/facebook
```
