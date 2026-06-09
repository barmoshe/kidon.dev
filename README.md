# kidon.dev

Personal site for **Daniel Kidon** — Backend Guild Lead @ HoneyBook, Tel Aviv.

A single static page: a cursor-reactive variable-weight wordmark over a WebGL
"black silk" shader background, linking out to LinkedIn, GitHub, and Medium.

## Run locally

It's one file — open `index.html` in a browser, or serve it:

```sh
python3 -m http.server
```

## Deploy

Hosted on Vercel; `kidon.dev` points at it via an A record (`@ → 76.76.21.21`).
No build step — Vercel serves `index.html` as-is.

## Stack

Plain HTML/CSS/JS, no framework. Fonts: Fraunces + Inter (Google Fonts).
Background is a hand-written GLSL fragment shader (domain-warped fbm) rendered
on a single full-screen triangle, capped for efficiency (DPR ≤ 0.66, ≤ 1.2 MP,
low-power hint, hidden-tab pause) and with a reduced-motion / no-WebGL fallback.

## Interaction model

- **Desktop:** the cursor is a warm light on the silk; KIDON's letters swell
  in weight toward it (Fraunces variable font, per-letter).
- **Mobile (no cursor):** the finger is the cursor while touching (with a
  2.5 s linger); every tap fires a light pulse at the touch point; when nobody
  touches, the light tours the page on waypoints — wordmark, identity line,
  CTA rows — and the letters run a slow breathing wave.
- `prefers-reduced-motion` disables all of it; the page stays static black.

---

Built by [Bar Moshe](https://github.com/barmoshe).
