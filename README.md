# javascript-openhab-sse-example
A simple example using SSE with javascript to access the openHAB ItemEvents (in this example `ItemStateChangedEvent`).

# Pre-Configuration

Please make sure you allow `CORS` in openHAB by editing `sudo nano /etc/openhab/services/runtime.cfg`:

```
org.openhab.cors:enable=true
```

# Customization

Please edit following in the `sse.html` file:

```
    const baseUrl = "127.0.0.1:8080";
    const username = "openhab";
    const password = "habopen";
    const itemName = "*";
    const event = `openhab/items/${itemName}/state`

    const url = `http://${username}:${password}@${baseUrl}/rest/events?topics=${event}`;
```

- The current username is `openhab`. Please replace it with your `username`.
- The current password is `habopen`. Please replace it with your `password`.
- `*` means that every item is used for `ItemStateChangedEvent`. You can access a specific item if you want.
- Currently `127.0.0.1:8080` is used as `baseUrl`.
- The `ItemStateChangedEvent` is described with `openhab/items/${itemName}/state`. If you want to retrieve another Event you have to change the `event` variaable.
