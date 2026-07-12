# Smart IoT Dashboard

A real-time dashboard UI for monitoring connected IoT devices — temperature, humidity, air quality, and motion — with live gauges, sparklines, a multi-series stream chart, and a scrolling event log.

**[Live demo → open index.html in a browser]**

## Features
- Animated radial gauges with smooth transitions
- Live sparkline history per sensor
- Multi-series real-time chart (canvas-based, no dependencies)
- Simulated device registry and streaming event log
- Fully responsive, dark technical UI with a subtle grid overlay

## Tech
Vanilla HTML / CSS / JavaScript — no build step, no frameworks. Charts are hand-drawn on `<canvas>`.

## Running locally
Just open `index.html` in a browser, or serve the folder:
```bash
python -m http.server 8000
```

## Connecting real data
The dashboard currently simulates sensor readings in `script.js` (`tick()` function). To wire it to real hardware:
1. Replace the `tick()` simulation with a WebSocket or MQTT-over-WebSocket client.
2. Push incoming readings into the same `state` object and call the existing render functions (`setGauge`, `drawSpark`, `drawMainChart`, `addLog`).

## License
MIT — free to use in your own portfolio or projects.
