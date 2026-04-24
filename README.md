# Signal Keeper

## What this is

Signal Keeper is a cognitive training app built around go/no-go and 2-back paradigms — two well-studied tasks for practicing inhibition (stopping a habit response) and working memory. It runs entirely on your child's Android phone as a home screen app, with no accounts, no internet after first load, and no data leaving the device. Sessions are 15 minutes and designed to be opened voluntarily each day.

---

## Setup (10 minutes, one time)

### Step 1 — Create a GitHub account
1. Open [github.com](https://github.com) in a browser on your computer.
2. Click **Sign up** and create a free account with your email.
3. Verify your email when prompted.

### Step 2 — Create a new repository
1. After logging in, click the **+** icon in the top-right corner, then **New repository**.
2. Name it something like `signal-keeper` (lowercase, no spaces).
3. Set visibility to **Public**.
4. Leave everything else unchecked.
5. Click **Create repository**.

### Step 3 — Upload the app files
1. On the repository page, click **uploading an existing file** (or **Add file → Upload files**).
2. Drag and drop all six files at once into the upload area:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
   - `README.md`
3. Scroll down to **Commit changes**, leave the default message, and click **Commit changes**.

### Step 4 — Enable GitHub Pages
1. On the repository page, click **Settings** (tab near the top).
2. In the left sidebar, click **Pages**.
3. Under **Source**, set the branch to **main** and the folder to **/ (root)**.
4. Click **Save**.
5. Wait about 60 seconds, then refresh the page. You will see: *"Your site is live at https://\<your-username\>.github.io/signal-keeper/"*
6. Copy that URL.

---

## Installing on the child's phone

1. On the child's Android phone, open **Chrome** (not Samsung Internet or Firefox).
2. Paste the URL from Step 4 into the address bar and load the page.
3. Wait for it to finish loading fully (the title screen appears).
4. Tap the **three-dot menu** (⋮) in the top-right corner of Chrome.
5. Tap **Add to Home screen**.
6. Accept the suggested name or change it to "Signal Keeper," then tap **Add**.
7. The app icon now appears on the home screen and opens full-screen with no browser bar.

> **Note:** Chrome may prompt "Add to Home screen" automatically after a couple of visits — that is normal and expected behavior.

---

## Daily use

**What the child does:**
- Open Signal Keeper from the home screen.
- Tap **Begin watch** on the title screen.
- Read the one-line opening card and tap **Ready**.
- Play through the 15-minute session (or tap **Finish early** to end).
- See the closing card with ships guided, then tap **Return to shore**.

**What the parent does:**
- Nothing daily — the app runs itself.
- Periodically check the data (see Export section below).
- After session 10, an n-back overlay unlocks automatically — the app handles the transition with on-screen instructions.

---

## Exporting data

1. Open Signal Keeper on the phone.
2. On the title screen, **press and hold the location name** (e.g., "Northern Cape") in the center of the screen for 2 seconds.
3. The **Keeper's Log** (parent view) opens.
4. Tap **Export data**.
5. The Android share sheet appears — choose Gmail, WhatsApp, Drive, or any app to send the file to yourself.
6. The file is a `.csv` spreadsheet named `signalkeeper_<initials>_<date>.csv`.

If the share sheet does not appear (older Android), the file downloads automatically to the phone's Downloads folder.

---

## Asking questions about the data

1. Export the CSV as above and open the file on your computer.
2. Select all the text in the file (Ctrl+A / Cmd+A) and copy it.
3. Open [claude.ai](https://claude.ai) or the Claude app.
4. Paste the CSV text and ask your question.

**Example questions:**
- "How has accuracy changed over the last two weeks? Is the trend improving?"
- "What is the false alarm rate on no-go trials — is it staying flat, getting better, or getting worse?"
- "Are reaction times on go trials getting faster session by session?"

---

## Resetting data / uninstalling

**To wipe all data:**
1. Long-press the location name on the title screen to open the Keeper's Log.
2. Tap **Reset all data**.
3. Confirm the dialog. All trial and session history is deleted and the app returns to first run.

**To uninstall:**
1. On the Android home screen, press and hold the Signal Keeper icon.
2. Tap **Uninstall** or drag it to the Uninstall area.
3. To also clear cached data: go to Android Settings → Apps → Chrome → Storage → Clear cache.

---

## Troubleshooting

**The app says it needs internet even after first load.**
The service worker caches the app shell on first visit. If you loaded the page and closed it before it finished loading, the cache may be incomplete. Reconnect to wifi, reopen the URL in Chrome, wait for the title screen to appear, then go offline again.

**"Add to Home Screen" doesn't appear.**
Chrome shows the prompt automatically after 2–3 visits meeting certain criteria (page loaded, manifest found). If it never appears: tap the three-dot menu → **Add to Home screen** manually. It will still work.

**The share sheet doesn't appear when exporting.**
Web Share with files requires Android Chrome 75+ and HTTPS. GitHub Pages uses HTTPS, so this should work. If it doesn't, the app falls back to a download link — check the phone's Downloads folder (Files app → Downloads).

**After clearing Chrome data or switching phones, progress is gone.**
All data is stored in the browser's IndexedDB on that specific device and Chrome profile. It is not backed up to the cloud. Export regularly if you want to preserve the history.

**The service worker is serving an old version after I updated the files.**
On the phone, open Chrome, go to the app URL, tap the three-dot menu → **Settings** → **Privacy and security** → **Clear browsing data** → check only **Cached images and files** → **Clear data**. Reload the page.

---

## Disclaimer

Signal Keeper is not a medical device. It does not diagnose, treat, or cure any medical condition, including ADHD or any other attention or executive function disorder. It is intended solely as supplementary cognitive practice for home use. It is not a substitute for clinical assessment, medication management, or professional therapeutic services. Before starting any new cognitive training routine, discuss it with your child's pediatrician or treating clinician.
