# Nexora Technologies — Free Certificate Verification System

This is a simple, database-free certificate verification system designed for GitHub Pages.

## What it does

- Public certificate verification page
- Certificate IDs such as `NEX-2026-00001`
- Certificate records stored in `certificates.json`
- Direct verification URLs:
  `verify.html?id=NEX-2026-00001`
- No paid hosting
- No backend
- No database
- Works with GitHub Pages

## 1. Create a GitHub repository

Create a repository named, for example:

`nexora-certificate-verification`

You can use a normal public GitHub account.

## 2. Upload these files

Upload:

- `index.html`
- `verify.html`
- `app.js`
- `style.css`
- `certificates.json`

Do NOT upload private information that should not be publicly accessible. GitHub Pages is public.

## 3. Enable GitHub Pages

In your repository:

Settings → Pages

Under "Build and deployment":

- Source: Deploy from a branch
- Branch: `main`
- Folder: `/ (root)`
- Save

After GitHub publishes it, your address will normally look like:

`https://YOUR-GITHUB-USERNAME.github.io/nexora-certificate-verification/`

## 4. Add certificates

Open `certificates.json`.

Add another record inside the JSON object. Example:

```json
"NEX-2026-00002": {
  "recipientName": "Arun Kumar",
  "role": "Python Development",
  "organization": "Nexora Technologies",
  "certificateType": "Certificate of Internship",
  "startDate": "01/09/2026",
  "endDate": "30/09/2026",
  "issueDate": "30/09/2026",
  "status": "VALID"
}
```

Then commit the change.

The direct verification link becomes:

`https://YOUR-GITHUB-USERNAME.github.io/nexora-certificate-verification/verify.html?id=NEX-2026-00002`

## 5. QR codes

For every certificate, encode its direct verification URL into a QR code.

Example:

`https://YOUR-GITHUB-USERNAME.github.io/nexora-certificate-verification/verify.html?id=NEX-2026-00001`

Put that QR code on the certificate.

## Important security note

This is a lightweight verification system, not a tamper-proof certificate authority. Anyone who can modify the public JSON through the GitHub repository can change records. Protect the GitHub account with a strong password and two-factor authentication.

Do not put passwords, API keys, personal addresses, phone numbers, or other private information into `certificates.json`.

## Contact

Nexora Technologies  
Email: nexora.ntechnologies@gmail.com  
Phone: +91 7708859311 / +91 8073827841
