# Rasoi landing page

This version includes a working waitlist form.

## What changed
- `index.html` now POSTs signups to `/api/waitlist`
- `api/waitlist.js` saves each signup as JSON in Vercel Blob
- `package.json` installs `@vercel/blob`

## 2-minute Vercel setup
1. Replace your repo files with the files in this ZIP and push to `main`.
2. In Vercel, open the Rasoi project.
3. Go to **Storage**.
4. Create a **Blob** store and connect it to this project.
5. Vercel automatically adds `BLOB_READ_WRITE_TOKEN`.
6. Redeploy if Vercel does not redeploy automatically after the storage connection.

After that, the waitlist form really persists signups.

## Where the signups are stored
Vercel Blob paths:

`waitlist/YYYY-MM-DD/<uuid>.json`

Each record contains:
- name
- contact
- source
- createdAt
- userAgent

## Fastest deployment
Because your Vercel project is already linked to GitHub, simply upload/commit these files to the repo's `main` branch. Vercel should redeploy automatically.
