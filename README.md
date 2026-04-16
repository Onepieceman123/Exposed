# Exposed
# exposed.dev
🔗 **[onepieceman123.github.io/Exposed](https://onepieceman123.github.io/Exposed)**

> **Your browser is already talking. This is what it's saying.**

A real-time browser fingerprinting demo that shows exactly what every website collects about you — no login, no cookies, no consent required.

---

## what it shows

| Section | Data Points |
|---|---|
| Identity & Network | Timezone, language, connection type, Do Not Track |
| IP Address & Location | Public IP, city, ISP, ASN, VPN detection, WebRTC local IP leak |
| Device & Hardware | Screen resolution, CPU cores, RAM, GPU renderer, OS, browser |
| Browser Capabilities | Cookies, localStorage, IndexedDB, Battery %, WebRTC, media devices |
| Canvas & Audio | SHA-256 canvas hash, pixel data, GLSL version, audio fingerprint |

**42 data points total.** All collected silently, in seconds, without asking.

---

## the scary part

Even with cookies disabled and a VPN running, websites can still identify you using:

- **Canvas fingerprinting** — your GPU renders pixels uniquely
- **Audio fingerprinting** — your hardware produces a unique signal
- **WebRTC leaks** — exposes your real local IP through the browser, bypassing VPNs
- **Hardware signals** — screen res + DPR + CPU cores + GPU = basically just you

---

## deploy

It's a single `index.html` file. No dependencies, no build step, no server.

```bash
git clone https://github.com/yourusername/exposed-dev
```

Then just open `index.html` in a browser — or push to GitHub Pages.

---

## github pages

1. Fork or upload `index.html` to a new repo
2. Settings → Pages → Source: `main` branch
3. Done — live at `yourusername.github.io/exposed-dev`

---

## how to protect yourself

- **Firefox** with `privacy.resistFingerprinting = true` in about:config
- **Tor Browser** — spoofs canvas, fonts, screen size and timezone
- **uBlock Origin** — blocks tracker scripts that harvest this data
- **CanvasBlocker** extension — randomises canvas & audio output each load
- Disable WebRTC in Firefox: `media.peerconnection.enabled = false`
- A VPN alone is **not enough** — it only hides your IP

---

## built by

**Bilal** — had the idea  
**Claude Sonnet 4.6** — wrote the code

---

> No data is collected, stored or transmitted. Everything runs locally in your browser.
