# Magic 8 Ball

A minimal, single-file Magic 8 Ball web app. Ask a yes/no question, tap the ball, and a classic answer surfaces on the blue triangle inside a realistic 3D ball.

Built as one self-contained `index.html` — no build step, no dependencies.

## Features

- **Realistic ball** — glossy 3D sphere with a recessed window and an inverted blue triangular die that reveals the answer.
- **20 classic answers** with the traditional distribution (10 positive, 5 non-committal, 5 negative).
- **6 languages** via a dropdown: English, Türkçe, Français, Deutsch, 日本語, العربية — with automatic right-to-left layout for Arabic.
- **Auto-fit text** — the answer scales to fit the triangle for every answer and language, without breaking words.
- **Prophecies (history)** — every question and answer is listed; delete individually or clear all.
- **Light / dark theme** — follows the system preference, toggle to override.
- **Responsive** — fits a single screen on desktop, tablet, and most phones; scrolls only on very short screens.

## Usage

Open `index.html` in any modern browser. That's it.

To serve locally:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy

Any static host works (GitHub Pages, Netlify, Vercel, Cloudflare Pages). Point it at this folder; `index.html` is the entry point.

A GitHub Actions workflow (`.github/workflows/deploy.yml`) publishes to GitHub Pages on every push to `main`. Enable it under **Settings → Pages → Build and deployment → Source: GitHub Actions**.

## Notes

History is kept in memory for the session and resets on reload.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Notable changes are tracked in [CHANGELOG.md](CHANGELOG.md).

## License

[MIT](LICENSE)
