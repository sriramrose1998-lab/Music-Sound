# Turning Wavelength into a real installable Android app

This folder contains a complete, installable **PWA** (Progressive Web App):
`index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`.

You need two short steps: **host it**, then **package it**.

---

## Step 1 — Host the files (free, ~5 minutes)

A PWA needs a real web address to be installable as an app. Pick one:

### Option A: Netlify Drop (easiest, no account needed to try)
1. Go to **https://app.netlify.com/drop**
2. Drag this whole folder onto the page.
3. Netlify gives you a live URL like `https://your-app-name.netlify.app`.

### Option B: GitHub Pages (free, good if you already use GitHub)
1. Create a new GitHub repository.
2. Upload all 5 files from this folder into it.
3. In the repo, go to **Settings → Pages**, set the source to the main branch, save.
4. GitHub gives you a URL like `https://yourusername.github.io/your-repo`.

Either way — open that URL on your phone first and confirm the app loads and
works, exactly like the version you tested before.

---

## Step 2 — Package it as a real Android app

1. Go to **https://www.pwabuilder.com**
2. Paste your hosted URL (from Step 1) into the box and click **Start**.
3. PWABuilder scans the site, confirms it's installable, and shows a score.
4. Click **Package for stores → Android**.
5. Download the generated **.apk** (installs directly on a phone) or **.aab**
   (the format the Play Store requires if you want to publish there).

To install the `.apk` directly on your own phone: transfer it to the phone,
open it, and allow "install from this source" if Android asks — no Play
Store needed.

---

## What you get vs. what stays the same

- **Real installable app**: shows up in your app drawer with the Wavelength
  icon, opens without a browser address bar, launches instantly from a cached
  app shell even with no signal.
- **Still true after packaging**: for privacy and security reasons, no phone
  app — native or otherwise — can silently keep permanent access to your
  music folder. You'll still tap "Add songs from this device" each time you
  open the app, the same as the web version. This is a device-level rule
  Android enforces for any app, not a limitation specific to this build.

If you'd rather skip Play Store packaging and just want the quicker route,
Step 1 alone (hosting it, then "Add to Home Screen" from Chrome) already
gets you an installable icon — this PWA version just makes that install
official (with the browser's install prompt) and adds offline loading of
the app shell.
