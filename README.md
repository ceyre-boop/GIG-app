# Sidequest

Paid side quests near you. Neighbors post small jobs (errands, moving help, pet walks, yard work, tech help) and anyone nearby can pick one up, tick off its steps, and turn it in for cash and XP.

It is a phone-first web app (PWA): open the link on your phone and add it to your home screen. It then opens full screen like an installed app, with its own icon, and works offline.

## What's in it

- **Explore**: an orienteering-style map of nearby quests (you are the start triangle, each quest is a numbered control), category filters, and a list sorted by distance, pay or time.
- **Quest sheet**: reward, XP, time, walking distance, the steps, and who posted it. Accept, tick steps, turn in.
- **Log**: active quests with progress, quests you posted, and finished ones.
- **Post**: the + button. Title, category, reward, time, place, and up to three steps.
- **Profile**: level and XP, earnings, a punch card that fills as you finish quests, and badges.
- **Wallet**: earnings history.

The quests on the map are sample data, and progress is saved in the phone's browser storage. There is no server yet.

## Files

- `index.html`: the whole app (HTML, CSS, JS, no build step)
- `manifest.webmanifest`, `icons/`: home-screen name, icon and colors
- `sw.js`: service worker that caches the app so it opens offline

## Run it on your phone

**GitHub Pages (free, this repo is set up for it).** In the repo go to Settings → Pages → Source and choose **GitHub Actions**. The workflow in `.github/workflows/pages.yml` deploys every push to the default branch to `https://ceyre-boop.github.io/GIG-app/`.

**Vercel.** Import the repo at vercel.com/new. It is a static site, so no settings are needed.

Then on the phone:

- **iPhone (Safari)**: open the link, tap Share, then **Add to Home Screen**.
- **Android (Chrome)**: open the link and tap **Install** in the banner, or menu → **Install app**.

## Run it locally

```bash
python3 -m http.server 8000
```

Open http://localhost:8000. To try it on your phone over Wi‑Fi, use your computer's local IP instead of localhost (install and offline need HTTPS, so use a deployed link for those).
