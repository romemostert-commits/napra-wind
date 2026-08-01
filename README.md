# NAPRA Wind Bracket

A wind-hold bracket calculator for NAPRA precision rifle matches. Log wind
readings per target across a stage, watch the min/max hold bracket build against
each target's width, and read off target-to-target offsets so one confirmed hit
corrects the rest. Pre-loaded with the NAPRA Heja and Outjo matchbooks (IPRF
class).

It's a single self-contained web page — no server, no build step, no accounts.

## Put it online with GitHub Pages

You only need a free GitHub account. Two ways: the website (no software) or the
command line.

### Option A — GitHub website only (easiest)

1. Go to https://github.com/new and create a repository.
   - Name it something like `napra-wind`.
   - Set it to **Public** (Pages needs Public on free accounts).
   - Leave everything else unchecked. Click **Create repository**.
2. On the new repo page, click **uploading an existing file** (the link in the
   "Quick setup" box), or go to **Add file → Upload files**.
3. Drag in **all** the files from this folder:
   - `index.html`
   - `manifest.webmanifest`
   - `icon.svg`, `icon-180.png`, `icon-192.png`, `icon-512.png`, `icon-512-maskable.png`
   - `.nojekyll`
   - `README.md` (optional)
   Then click **Commit changes**.
   - Tip: if the `.nojekyll` file is awkward to drag, it's optional but
     recommended. You can also create it via **Add file → Create new file**,
     name it exactly `.nojekyll`, leave it empty, and commit.
4. Go to the repo's **Settings → Pages** (left sidebar).
5. Under **Build and deployment → Source**, choose **Deploy from a branch**.
   Set **Branch** to `main` and folder to `/ (root)`. Click **Save**.
6. Wait ~1 minute, then refresh. Pages will show your live URL, like:
   `https://YOUR-USERNAME.github.io/napra-wind/`

That URL is your app. Open it on the iPhone (next section).

### Option B — command line (git)

```bash
cd napra-wind
git init
git add -A
git commit -m "NAPRA wind bracket app"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/napra-wind.git
git push -u origin main
```

Then do steps 4–6 above (Settings → Pages → deploy from `main` / root).

## Install on your iPhone (Add to Home Screen)

1. Open the Pages URL in **Safari** (must be Safari, not Chrome, for the app
   icon to work).
2. Tap the **Share** button (the square with the up arrow).
3. Scroll down and tap **Add to Home Screen**, then **Add**.

You'll get an app icon that launches fullscreen, with no browser bars — it
behaves like a native app.

## Saving your readings

Readings are held in the page while it's open and stay put as you move between
stages and matches. They do **not** automatically survive a full reload or
reopening the app. To keep them:

- Tap **Save** (top right) to download a `.json` file of all your readings (it
  lands in the iPhone **Files** app).
- Tap **Load** and pick that file to restore everything later.

Do a Save at the end of a stage or match if you want to review it afterward.

## Updating the app later

Edit `index.html` (or replace it), then upload/commit the new version to the
same repo. GitHub Pages redeploys automatically within a minute. On the iPhone,
close and reopen the home-screen app to pick up the new version.

## Files

| File | Purpose |
|---|---|
| `index.html` | The entire app |
| `manifest.webmanifest` | Makes it installable with a name + icon |
| `icon-*.png`, `icon.svg` | Home-screen / app icons |
| `.nojekyll` | Tells GitHub Pages to serve files as-is |
