# Statue Duty

A silly survival game: you are a statue, and pigeons want to poop on you. Tap them away, buy upgrades with coins from tourists, and survive as long as you can.

**Play it:** https://henri1402.github.io

## What's in this folder

| File | What it does |
|---|---|
| `index.html` | The whole game: graphics, sounds and gameplay, all in one file. |
| `manifest.webmanifest` | The app's name, icon and colors, so phones can install it like an app. |
| `sw.js` | Lets the game work offline and makes sure players always get the newest version. |
| `icon.svg`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | The app icon in different sizes. |
| `privacy.html` | The privacy policy page that Google Play asks for. |
| `.nojekyll` | Tells GitHub to publish every file exactly as it is. Don't delete it. |

## How to update the game

1. Change `index.html` (in VS Code, or on github.com with the pencil icon).
2. Commit the change to the `main` branch.
3. Wait about a minute. The website updates automatically, and so does the Play Store app, because the app loads the game from this website.

You only need to rebuild the Android app in PWABuilder if you change the app's name or icon.

## Publishing on Google Play (short version)

1. Create a Google Play Console account and verify your identity.
2. Go to https://www.pwabuilder.com, enter https://henri1402.github.io, and download the Android package.
3. **Keep the signing key file from PWABuilder somewhere safe and private. Never upload it here.** You need it for every future Android update.
4. PWABuilder also gives you an `assetlinks.json` file. Put it in a folder called `.well-known` in this repository, so it is at https://henri1402.github.io/.well-known/assetlinks.json. This proves the app and the website belong together, and removes the browser bar from the app.
5. Upload the app to a closed test with at least 12 testers for 14 days, fill in the store listing (use https://henri1402.github.io/privacy.html as the privacy policy), then apply for production.

If you ever add ads, update `privacy.html` first.
