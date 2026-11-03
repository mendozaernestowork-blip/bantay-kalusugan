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
   `index.html`, `privacy.html`, `images/`, `downloads/`, the icons, `og-image.jpg`,
   `robots.txt`, `sitemap.xml`, `.nojekyll`, `README.md`. Then click **Commit changes**.
4. Go to **Settings → Pages**. Under *Build and deployment*, set
   **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)**, then click **Save**.
5. Wait 1–2 minutes and refresh. GitHub shows "Your site is live at ...". Open it.

Only put website files in this repo. It is public, so never add the app's code, `.env`, or any respondent data.

## Before or soon after publishing

- [ ] In `index.html` and `privacy.html`, search for `EDIT` and add the team members, adviser,
      a contact email you will check, and the data-retention period from your ethics approval.
- [ ] Have your adviser or ethics reviewer read `privacy.html`.

## When the signed APK is ready

1. Upload it to the repo as `downloads/bantay-kalusugan.apk` (Add file → Upload files, inside the `downloads` folder).
2. In `index.html`, search for **WHEN THE APK IS READY** and swap the "coming soon" line for the download link shown there.
3. In the app info near the top of `index.html`, replace the `"_comment"` line with the `downloadUrl` line it shows.
4. Add the file size and release date (search `EDIT:` in `index.html`), and delete `downloads/PUT-APK-HERE.txt`.

GitHub updates the live site a minute or two after each commit.

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
- `downloads/`: where the APK goes
