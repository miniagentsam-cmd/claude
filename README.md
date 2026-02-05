# BTC Déjà Vu

A mobile-friendly web app that shows the current Bitcoin price and tells you when BTC first reached that same price level in history.

## Features

- **Real-time Bitcoin price** - Fetched from CoinGecko API
- **Historical price matching** - Finds the first date BTC hit the current price (within 2% tolerance)
- **Time elapsed display** - Shows how long ago Bitcoin first reached this price
- **Auto-refresh** - Updates every 60 seconds with countdown timer
- **Mobile-first design** - Responsive layout optimized for all screen sizes
- **Dark theme** - Easy on the eyes with Bitcoin's signature orange accent

## Usage

Simply open `index.html` in a web browser. No build step or server required.

You can also serve it with any static file server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve .
```

## How It Works

1. Fetches the current Bitcoin price from CoinGecko's free API
2. Retrieves historical daily BTC price data (all available history)
3. Searches for the earliest date when BTC was within 2% of the current price
4. Displays the result with a human-readable time difference

If the current price has never been reached before, the app celebrates the new all-time high!

## Technologies

- HTML5
- CSS3 (with CSS custom properties)
- Vanilla JavaScript (ES6+)
- CoinGecko API (free, no API key required)

## License

MIT
