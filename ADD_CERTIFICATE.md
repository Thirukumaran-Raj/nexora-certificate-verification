# How to add a certificate

1. Open `certificates.json`.
2. Add a unique certificate ID.
3. Keep `"status": "VALID"` for an active certificate.
4. Change the recipient, role and dates.
5. Commit the file to GitHub.
6. Wait for GitHub Pages to publish the change.
7. Generate a QR code containing the certificate's direct `verify.html?id=...` URL.
8. Put the QR code on the certificate.

To revoke a certificate, change its status to:

`"status": "REVOKED"`

The verification page will then show it as not valid.
