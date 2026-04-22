# PiPilot IDE Extensions

Official extension registry for [PiPilot IDE](https://github.com/pipilot-dev/pipilot-ide).

## Installing Extensions

Open PiPilot IDE → Activity Bar → Extensions tab → Browse and click **Install**.

## Creating Extensions

See [EXTENSION_API.md](EXTENSION_API.md) for the full API reference.

Extensions are single JS files that receive `(PiPilot, bus, api, state)` arguments:

```javascript
(function (PiPilot, bus, api, state) {
  // Your extension code
})(PiPilot, bus, api, state);
```

## Publishing

1. Add your `.js` file to `extensions/`
2. Add an entry to `registry.json`
3. Submit a PR

## Structure

```
registry.json          # Extension registry (fetched by IDE)
extensions/            # Extension JS files
  word-count.js        # Example: word count in status bar
EXTENSION_API.md       # Full API documentation
```
