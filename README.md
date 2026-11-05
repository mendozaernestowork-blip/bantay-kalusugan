# Bantay-Kalusugan website (GitHub Pages)

Live address once published: **https://mendozaernestowork-blip.github.io/bantay-kalusugan/**

This folder is the whole site. There is no build step.

## Publish (about 5 minutes, all in the browser)

1. Sign in to GitHub as **mendozaernestowork-blip**.
2. **New repository**
   - Name: `bantay-kalusugan` (exactly this, or the address above changes)
   - Visibility: **Public** (free GitHub Pages needs a public repo)
   - Leave "Add a README" unticked, then click **Create repository**.
3. On the empty repo page, click **uploading an existing file**.
   Drag in **everything inside** this folder, not the folder itself:
   `index.html`, `privacy.html`, `images/`, the icons, `og-image.jpg`,
   `robots.txt`, `sitemap.xml`, `.nojekyll`, `README.md`. Then click **Commit changes**.
4. Go to **Settings → Pages**. Under *Build and deployment*, set
   **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)**, then click **Save**.
5. Wait 1–2 minutes and refresh. GitHub shows "Your site is live at ...". Open it.

Only put website files in this repo. It is public, so never add the app's code, `.env`, or any respondent data.

## Before or soon after publishing

- [ ] In `index.html` and `privacy.html`, search for `EDIT` and add the team members, adviser,
      a contact email you will check, and the data-retention period from your ethics approval.
- [ ] Have your adviser or ethics reviewer read `privacy.html`.

## Publish a new APK version

The **Download APK** button links to
`https://github.com/mendozaernestowork-blip/bantay-kalusugan/releases/latest/download/bantay-kalusugan.apk`.
GitHub sends that address to the file named `bantay-kalusugan.apk` in the newest release, so the button never
needs editing. The page reads the version, size and date from that release by itself.

1. Rename the APK to exactly `bantay-kalusugan.apk` (all lowercase, no spaces).
2. On this repo's page, click **Releases** (right side), then **Draft a new release**.
3. Under the tag, type the version with a `v` in front, e.g. `v2.5`, and choose **Create new tag**.
   Title: `Bantay-Kalusugan 2.5`.
4. In the description, write two or three lines on what changed. The site's "Release notes" link opens this.
5. Drag `bantay-kalusugan.apk` into the box for binaries and wait for the upload to finish.
6. Leave **Set as a pre-release** unticked and **Set as the latest release** ticked, then click **Publish release**.
7. Open the site on a phone, tap **Download APK**, and install it to check.
8. Optional: in `index.html`, update `"softwareVersion"` near the top and the version and size text in the
   download section. Visitors only see that text when GitHub can't be reached.

Never commit the APK, keystores, `.env` or app code to this repo. It is public.

### Before you build the next version (in the app repo)

- In `android/app/build.gradle`, raise `versionCode` by 1 (it must always go up) and set `versionName`
  to the version you will tag, e.g. `"2.6"`. Phones show `versionName` under App info.
- Sign every version with the same key, or phones refuse the update ("App not installed") until the
  old app is uninstalled.
  - A debug APK (**Build → Build App Bundle(s) / APK(s) → Build APK(s)**; not the one the Run button
    makes, which phones won't install from a download) is signed with the debug key of the computer that
    built it (`%USERPROFILE%\.android\debug.keystore`). Build every update on that computer, or copy
    that file to the computer you build on.
  - A signed release APK: **Build → Generate Signed App Bundle or APK → APK**, create a keystore once,
    keep it and its passwords outside the repo with a backup, and pick **release**. The file is
    `android/app/release/app-release.apk`. Moving from a debug build to a release build means people
    uninstall the old app once; their saved results come back when they sign in.

## Get found on Google

1. Open **Google Search Console** → Add property → **URL prefix** →
   `https://mendozaernestowork-blip.github.io/bantay-kalusugan/`
2. Verify with the **HTML tag** method: copy the `<meta name="google-site-verification" ...>` tag
   into the `<head>` of `index.html`, commit, then click Verify.
3. Under **Sitemaps**, submit `sitemap.xml`.
4. Use **URL inspection** on the home page, then **Request indexing**.
5. Check the share preview by pasting the link into the Facebook Sharing Debugger.

Searches for "Bantay-Kalusugan" usually start showing the site within a few days to a few weeks.

Note: on a project site like this one, search engines only read `robots.txt` from the root of
`mendozaernestowork-blip.github.io`, so the included `robots.txt` is harmless but unused. Submitting the sitemap in Search Console (step 3) covers it.

## Files

- `index.html`: the page (English, with a Tagalog section)
- `privacy.html`: privacy policy (draft for review)
- `images/`: real app screenshots with sample answers (not real people)
- `og-image.jpg`: the picture shown when the link is shared
- `favicon.svg`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`: icons
- `sitemap.xml`, `robots.txt`: for search engines
- `.nojekyll`: tells GitHub to serve the files as-is
