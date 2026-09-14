# iPodify

A no-build, iPhone-optimized iPod-style PWA starter with Spotify PKCE login.

## Run locally

Serve this folder over HTTP (OAuth will not work from `file://`):

```bash
python3 -m http.server 8080
```

Open `http://localhost:8080` on your phone or desktop.

## Spotify setup

1. Create an app at https://developer.spotify.com/dashboard.
2. Add `http://localhost:8080/` as a Redirect URI.
3. In the browser console, run:

```js
localStorage.setItem('spotify_client_id', 'YOUR_CLIENT_ID')
```

4. Reload and choose **Connect Spotify**.

For production, register your real HTTPS URL. Full Web Playback SDK streaming normally requires Spotify Premium. This starter uses PKCE so no client secret is placed in the frontend.
