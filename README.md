# Shortlist — finance internship application assistant

This repository hosts **Shortlist**, a single-page website for tracking internship applications, researching companies, drafting application materials, and preparing outreach and interviews.

## Publish on GitHub Pages (no installation required)

1. Upload **`index.html`**, **`.nojekyll`**, and **`README.md`** into the **root** of your GitHub repository. Do **not** upload only the ZIP file or leave the website under a nested `shortlist/` folder. If the repository already has a README, replace it or keep its text with these instructions.
2. In the repository open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select **`main`** and **`/(root)`**, then **Save**.
5. Open **Visit site** on that same Pages settings screen once GitHub has published it. A project's address is generally `https://YOUR-USERNAME.github.io/YOUR-REPO/`.

**Repository visibility:** GitHub Free generally requires a **public repository** for Pages. Private repositories can use Pages with eligible paid GitHub plans. **The published site may still be public even when its source repository is private.** Do not include private information, an API key, a resume, or a saved profile in the repository.

## Run the app

1. Open the Pages website.
2. Go to **Me → Settings**, add your **own Anthropic API key** and choose a model. A ChatGPT subscription does not provide an Anthropic API key; the Anthropic API has usage-based charges.
3. Use **Test connection**. Then use **Me** to fill in or import your profile.
4. Paste a real job posting to create an application workspace. Drafting and research require API access. The user interface, application tracking, and local data can work without a key.

### Privacy and limitations

- GitHub Pages is **static hosting**, not a private server. **This version sends your API requests directly from your browser to Anthropic.** The key is held in that browser's local storage, **not** in this repository; nevertheless, browser-stored keys carry security risk. Use a key with a strict spend limit, only on a trusted computer/browser, and clear it in Settings when finished. For a hardened production or shared application, add a secure serverless API proxy with authentication, rate limits, and server-managed secrets before allowing other users to use it.
- Profiles and applications are stored locally in that browser. They do **not** synchronize across browsers, devices, or GitHub. Export backups before clearing browser data. Research, hiring timelines and estimates must be checked against primary sources.
- Word buttons download individual `.docx` files. PDF opens a browser print dialog; choose **Save as PDF**. This is **not** an automatic direct PDF download.
- Word and PDF print views use 12-point Times New Roman for standard paragraphs, double spacing, and 1-inch page margins. Length varies by content and may exceed one page.
- Google Docs on the public website opens a new Doc and copies the text for you to paste; automatic Google Drive creation only works with a separate supported integration.
- This is an application **assistant**. It does not log into Handshake or LinkedIn or submit applications without your action.

## Troubleshooting

- **GitHub displays the README instead of the app:** `index.html` isn't in the publishing root, or Pages hasn't been enabled.
- **404:** verify Pages publishing source is `main` and `/(root)` and open the exact Visit site URL (includes the repository path for project sites).
- **Can't enable Pages on private repo:** make the repository public *only after checking that nothing sensitive is committed*, or use a plan that supports private-repo Pages.
- **API errors:** check the browser console, the exact model availability in your Anthropic account, billing status, and key permissions. Direct browser API calls can be blocked or unsupported by a provider policy; this site cannot resolve that without a backend.
- **PDF doesn't download automatically:** choose **Save as PDF** in the print dialog.

## Files

- `index.html` — complete application, no build step.
- `.nojekyll` — tells GitHub Pages not to process the site with Jekyll.
- `README.md` — setup and usage.