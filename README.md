# GES Promotion Question Bank: Android app (PWA)

An installable web app: it opens full screen from the home screen with its own icon, and works offline
after the first visit. Hosted free on GitHub Pages. Built by Appiatus EdTech Consults.

## Put it online (about 10 minutes)
1. Create a free account at github.com and click **New repository**. Name it, for example, `promotion-prep`. Choose **Public**.
2. Click **uploading an existing file**, drag in **everything inside this folder** (including `.nojekyll`), then **Commit changes**.
   Keep `index.html`, `sw.js` and `manifest.json` in the top level of the repository, not in a subfolder.
3. Open **Settings → Pages**. Under *Build and deployment* choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
4. After a minute your app is live at `https://YOUR-USERNAME.github.io/promotion-prep/`.

## Install on Android
Open the link in **Chrome** → tap **Install this app on your phone** on the first screen (or Chrome menu ⋮ → **Install app**).
The app appears on the home screen and opens like any other Android app.

## Releasing an update
Replace `index.html` in the repository, then change `const VERSION = "v1"` in `sw.js` to `"v2"` (then `"v3"`, and so on).
Phones pick up the new version the next time they open the app with internet.

## Things to know
- **Public repository:** anyone can read the files, including the questions and the stored unlock hashes. GitHub Pages
  on a private repository needs a paid GitHub plan. The server version (`ges-backend`) fixes this.
- **Accounts and the free trial are still stored on each phone.** Registering on one phone does not log you in on another,
  and the trial end depends on the phone's clock. For real accounts, deploy `ges-backend` and connect the page to it.
- **Offline:** all questions work offline once the app has been opened once with internet. Fonts fall back to the phone's own.
- **Google Play Store (optional):** this site can be wrapped into a Play Store app with PWABuilder (pwabuilder.com).
  You need a Google Play developer account (one-time fee) and a site address that uses HTTPS, which GitHub Pages provides.
- **Free limits:** GitHub Pages is free with usage limits (about 1 GB site size and 100 GB bandwidth a month).
