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
on a single full-screen triangle, capped for efficiency and with a
reduced-motion / no-WebGL fallback.

---

Built by [Bar Moshe](https://github.com/barmoshe).
