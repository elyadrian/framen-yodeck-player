# Framen Ad Player for Yodeck

Plays Framen ads on Yodeck digital signage screens with proper impression tracking.

## Quick Start

1. Push this repo to GitHub
2. Enable GitHub Pages (Settings → Pages → Source: main branch)
3. Visit: `https://elyadrian.github.io/framen-yodeck-player/?screen=YOUR_SCREEN_ID`

## Debug Mode

Press **D** on your keyboard to show/hide the debug log panel.

## How It Works

1. Player loads and reads the `?screen=` parameter from the URL
2. Calls Framen API to get the next ad/news for that screen
3. Plays the video or shows the HTML content
4. **Fires the "pop" URL** using Image beacon (bypasses CORS) to register the impression
5. Fetches the next ad and repeats

## Adding to Yodeck

1. In Yodeck, add a new **Web Page** media item
2. Set the URL to: `https://elyadrian.github.io/framen-yodeck-player/?screen=YOUR_SCREEN_ID`
3. Add it to your playlist
4. The player will run and track impressions automatically
