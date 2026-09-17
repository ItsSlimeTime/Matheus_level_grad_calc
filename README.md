# SloApp

**SloApp** (Slope App) is a calculator for levels, gradients and ramp landings on architecture projects.

**Open it here:** https://itsslimetime.github.io/Matheus_level_grad_calc/SloApp.html

You can use it straight from that link in any browser. You can also **install it as an app** on your phone or computer. It then gets its own icon, opens full-screen without the browser bar, and **works with no signal** (handy on site).

---

## Install it as an app

You only need to do this once per device. Nothing is downloaded from an app store, and it takes about 30 seconds.

### Android phone (Chrome)

1. Open **Chrome** and go to https://itsslimetime.github.io/Matheus_level_grad_calc/SloApp.html
2. Tap the **⋮** menu (three dots, top right).
3. Tap **Add to home screen**, then choose **Install**. On some phones this menu item is called **Install app**.
4. Tap **Install** again to confirm.
5. The **SloApp** icon appears on your home screen and in your app list. Open it from there from now on.

> Chrome may also show an **Install app** banner at the bottom of the screen after a few seconds. Tapping it does the same thing.

### Android phone (Samsung Internet)

1. Open the link in **Samsung Internet**.
2. Tap the **☰** menu (bottom right).
3. Tap **Add page to** → **Home screen**.

### iPhone / iPad (Safari)

The steps only work in **Safari**. Chrome on iPhone can't install apps like this.

1. Open **Safari** and go to https://itsslimetime.github.io/Matheus_level_grad_calc/SloApp.html
2. Tap the **Share** button (square with an arrow pointing up). On iPhone it's at the bottom of the screen, and on iPad it's at the top.
3. Scroll down and tap **Add to Home Screen**.
4. Tap **Add** (top right).

### Windows or Mac computer (Chrome or Edge)

1. Open the link in **Chrome** or **Microsoft Edge**.
2. Look for the small **install icon** at the right-hand end of the address bar (a monitor with a down arrow, or a **+** in a square). Click it, then click **Install**.
   - If you can't see the icon: in **Chrome**, open the **⋮** menu → **Cast, save and share** → **Install page as app**. In **Edge**, open the **…** menu → **Apps** → **Install this site as an app**.
3. The calculator opens in its own window and can be pinned to the taskbar or dock like any other program.

---

## Using the installed app

- **Offline:** open the app once while you're online after installing. After that it works without internet.
- **Updates:** updates happen automatically. When a new version is published, the app picks it up the next time it's opened with a connection. If you don't see a change, close the app fully and open it again.
- **Uninstalling:** remove it like any other app. On Android, press and hold the icon → **Uninstall**. On iPhone, press and hold → **Remove App**. On a computer, open the app → **⋮** / **…** menu → **Uninstall**.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| No "Install" or "Add to home screen" option | Make sure you're using Chrome on Android or Safari on iPhone, not an in-app browser such as the one inside Outlook, Teams or WhatsApp. Copy the link into the real browser. |
| Work phone or laptop won't let you install | Your IT department may block installing apps. You can still bookmark the link and use it in the browser. |
| The app shows an old version | Close the app completely and reopen it while online. |
| The text font looks slightly different offline | That's normal. The app falls back to the phone's standard font when it can't reach Google Fonts. |

---

## For whoever maintains this repo

Everything is static and there is no build step. GitHub Pages publishes the `main` branch automatically, usually within a minute of a push.

| File | Purpose |
| --- | --- |
| `SloApp.html` | The whole app (HTML, CSS, JS and embedded logo). |
| `index.html` | Tiny redirect so the short link (`.../Matheus_level_grad_calc/`) still opens SloApp. |
| `manifest.webmanifest` | App name, colours and icons used when installing. |
| `sw.js` | Service worker that makes the app work offline. |
| `icons/` | App icons made from SloApp's favicon (`favicon.svg` is the source). |

**Updating the app:** if you replace `SloApp.html` with a new version, copy across the two blocks marked `<!-- PWA ... -->` (one in `<head>`, one just before `</body>`). Without them the app can no longer be installed and won't work offline.

**Adding or renaming files:** add them to the `PRECACHE` list in `sw.js` and bump `CACHE_VERSION`, so installed copies pick them up offline.
