# KEDCO Technical Department — Single-File GitHub Pages Pilot

Digitization, Asset Management and Quality Assurance Unit.

## Deploy to GitHub Pages (no Node.js required)

1. Create a GitHub repository for this **public, non-confidential demonstration**.
2. Upload `index.html` to the repository root. All images, design styles, application logic, login forms and browser-video features are embedded directly in that file; an `assets/` directory is **not** required.
3. Optionally upload the empty `.nojekyll` file from this package.
4. In repository **Settings → Pages → Build and deployment**, select **Deploy from a branch**, branch **main**, folder **/(root)**, then Save.
5. Wait for GitHub's publishing process. Open the Pages URL displayed in Settings → Pages.

## First use

- On the published HTTPS site, open **Staff Pilot Login**. On the first visit *in that specific browser*, choose **First-Time Setup**.
- Create a local pilot profile with a name, email and a password of at least 10 characters including letters and numbers. No default password is embedded.
- The first local profile has a demo-admin role. In the **Local Accounts** tab it can create additional *profiles on that same browser only*. Viewers have read-only UI; editors can add/edit pilot register records. These roles are **not** true security boundaries.
- The Digitization, Assets, and QA tabs store training-only records in browser `localStorage`. Use Overview & Backups to export a JSON file, or export the active register as CSV. A JSON backup can be imported manually on another device, but **local profiles/passwords are not included** in the backup.
- The Media section can preview an approved video selected from your device or generate a short (~10 seconds) WebM slideshow video locally; this is an animated-image presentation, **not a live video feed or AI text-to-video synthesis**.

## Security and storage limitations

This is a **static training/pilot prototype**, not a secure staff system. The entire HTML/JavaScript source is public on GitHub Pages; a visitor can inspect or modify their own browser state, bypass local role checks, and create their own initial local profile. Passwords are locally salted and hashed using browser Web Crypto (PBKDF2), but this does **not** make GitHub Pages a centralized identity system. Records can be lost when browser storage is cleared and are not shared between users or devices.

**Never enter or publish real login credentials, personal staff details, confidential KEDCO documents, customer data, network vulnerabilities, or other restricted information in this pilot.** For genuine KEDCO staff authentication and shared operations data, connect a proper hosted identity and data service with enforceable server-side authorization.

## Editing

Everything required to run the website is inside `index.html`, including embedded illustrative JPEG photos. They are AI-generated depictions and **must not be presented as real KEDCO staff or documented site activity**. Replace them only with appropriately licensed and approved corporate media. The page has no third-party JavaScript dependencies, but uses modern HTML5 browser APIs. Use GitHub Pages over HTTPS for local password hashing and WebM creation. Test in current Chrome / Edge.

## Notes

- Demo accounts are stored in `localStorage`; current local session is in `sessionStorage`.
- Visual numbers refer to fixed public categories or counts derived from demo records — not live operations data.
- Changing the repository HTML on GitHub does not synchronize data stored in any user's browser.
