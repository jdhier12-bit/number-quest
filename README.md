# Number Quest — The Crystal Keep

A brand-new, original kid-friendly fantasy math game. No dependencies or build tools. All game art is CSS, SVG, and emoji; no copied previous game code.

## Open locally

```sh
cd /workspace/number-quest
python3 -m http.server 8080
```

Open **http://localhost:8080** on the same computer. For a phone/tablet on the same Wi-Fi, use the hosting computer's LAN IP and port (basic play works; PWA installation/offline need HTTPS or localhost). Opening `index.html` directly also plays, but service workers require an HTTP server.

## Play

Choose multiplication, long division, or both; choose 2–5-digit main numbers. Multiplication uses a 1–2-digit multiplier, division a 1-digit divisor with an exact integer answer. Type the answer and press Enter or tap Cast spell. Correct spells award 10 gems; each third consecutive correct answer adds 15 bonus gems. Mistakes reset the combo, but never remove gems or lives. Each cleared room earns 1–3 stars depending on retries. Rooms 4, 8 and 12 are guardians requiring three correct spells. Clear all 12 for the victory crown. Use the step-by-step guide to see partial products or the complete long-division method. Audio is optional and starts only on interaction. No account, tracking, ads, or purchases.

Keyboard: Tab through controls, Enter to cast, Enter again on the focused next-room button. Touch: tap controls and enter numbers with the numeric keyboard. Reduced-motion preferences are respected.

## Install / offline

Serve this directory on any static HTTPS host. Desktop Chrome/Edge: browser install icon or the in-game install button when available. iPhone/iPad: Safari → Share → Add to Home Screen. Android: browser menu → Install app. Once loaded, core game files are cached for offline use. External optional Google fonts fall back to system fonts offline. Best completed-run gem score is stored on this device; an in-progress run is not saved.

## Validate

`node tests/smoke.cjs` tests 1,600 generated problems and a complete 12-room run with all bosses, wrong answers, guides, scoring and victory. `node --check app.js` validates JS syntax. Browser/device install behavior still requires manual testing. No deployment or GitHub push has been performed.
