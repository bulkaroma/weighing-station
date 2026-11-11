# Weighing Station

Live weighing web app for Bluetooth scales and older RS-232 scales (through a Bluetooth adapter such as HC-05 / HC-06 / BC04-B).

- Big live weight display with stable indicator, tare and full screen
- Target check (in range / under / over)
- Weighing log with Excel copy and CSV download
- Formula mode: weighs ingredients one by one from %, grams or parts, with a batch report
- Works on a Windows PC (Chrome or Edge) and Android phones (Chrome). Can be installed as an app.

No build step and no server code. It's a static site.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app |
| `manifest.webmanifest`, `icon-*.png`, `apple-touch-icon.png`, `favicon.svg` | App name and icons for "Install app" / "Add to Home screen" |
| `sw.js` | Lets the app open without internet |
| `vercel.json` | Hosting settings for Vercel |

## Deploy on Vercel

1. Upload these files to a GitHub repository (all files at the top level).
2. On vercel.com: **Add New → Project → Import** the repository.
3. Framework preset: **Other**. Leave the build and output settings empty. Click **Deploy**.

Every change pushed to GitHub redeploys automatically.

## Use it

- **Windows:** pair the scale in Bluetooth settings, open the site in Chrome or Edge, click **Connect scale**, and choose the *Outgoing* "Standard Serial over Bluetooth link" COM port.
- **Android:** pair the scale in Android Bluetooth settings, open the site in Chrome, tap **Connect scale**, and pick the scale.
- iPhone isn't supported, because iPhone browsers can't use Bluetooth serial.

Records and formulas are saved in the browser on each device. Use **Download CSV** to keep them.
