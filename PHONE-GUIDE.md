# Build a REAL APK — entirely from your phone 📱

No computer needed. GitHub's free cloud machines will build the app for you.
Total time: about 20 minutes, most of it waiting for the build.

You'll need: this kit's 5 files (unzip them first) and a free GitHub account.

---

## Part 1 — Create your GitHub account (skip if you have one)

1. In your phone browser, go to **github.com** and tap **Sign up**
2. Follow the steps (email, password, username). Free plan is all you need.

## Part 2 — Create the project

1. Tap the **+** (top right) → **New repository**
2. Repository name: `chandanpur-brawl`
3. Keep it **Public**, leave everything else as is → tap **Create repository**

## Part 3 — Upload the game files

1. On the new repo page, tap the link **"uploading an existing file"**
   (it's in the setup text). If you don't see it, tap **Add file → Upload files**.
2. Tap the file picker and select these 4 files from the unzipped kit:
   - `index.html`
   - `package.json`
   - `capacitor.config.json`
   - `icon.png`
3. Tap **Commit changes** at the bottom.

*Tip: if the upload page is awkward on mobile, turn on "Desktop site" in your
browser menu (⋮).*

## Part 4 — Add the build instructions file

This one file tells GitHub how to build your APK.

1. Open `build.yml` from the kit in any text viewer, **select all, copy**
2. Back in your repo: **Add file → Create new file**
3. In the name box type exactly:  `.github/workflows/build.yml`
   (typing the `/` creates the folders automatically)
4. Paste the copied text into the big box
5. Tap **Commit changes**

## Part 5 — Watch it build, then download your APK

1. The build starts by itself. Tap the **Actions** tab at the top of the repo.
2. You'll see "Build Chandanpur Brawl APK" running with a yellow dot.
   Wait ~5–10 minutes until it turns into a green check ✅
3. Tap the finished run → scroll down to **Artifacts** →
   tap **chandanpur-brawl-apk** to download it
4. It downloads as a small zip — open it with your Files app and extract
   **app-debug.apk**

## Part 6 — Install it

1. Tap **app-debug.apk**
2. Android asks permission to install from this source — allow it
3. Tap **Install**

Done. 🎉 Chandanpur Brawl is now a real installed app with its own icon.
Send the same APK file to friends on WhatsApp — they install it the same way,
anywhere in the world.

---

## Updating the game later

When Claude gives you a new `index.html`: in your repo open `index.html` →
tap the pencil (edit) → replace the content (or delete and re-upload the file)
→ Commit. GitHub automatically builds a fresh APK — download it from Actions
like before.

## If the build shows a red ❌

Tap the failed run → tap the step with the ❌ to see the log. The two common
causes: a file is missing (check all 4 from Part 3 are in the repo) or the
workflow file name/path has a typo (must be exactly
`.github/workflows/build.yml`). Show Claude a screenshot of the log and it
will fix it.
