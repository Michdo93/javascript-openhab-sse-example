# javascript-openhab-sse-example
A simple example using SSE with javascript to access the openHAB ItemEvents.

# Pre-Configuration

Please make sure you allow `CORS` in openHAB by editing `sudo nano /etc/openhab/services/runtime.cfg`:

```
org.openhab.cors:enable=true
```
