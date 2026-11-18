# ThriftDrift

## Run locally

This prototype is a standalone HTML page with no build step or external dependencies. From the project directory, start a local web server:

```sh
ruby -run -e httpd . -p 8000 -b 127.0.0.1
```

Then open [http://localhost:8000](http://localhost:8000) in a browser.

## Shared player name

The name entered before character setup is saved in browser `localStorage` under `thriftDrift.playerName`. Later category or popup code can read the current value with:

```js
const playerName = window.ThriftDrift.getPlayerName();
```

The accessor returns the saved, trimmed name, or an empty string if no name has been saved yet. The skin-tone step does not use or display the name.