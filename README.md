# Good Habits for Life (Hugo)

This is the Hugo-based static site for https://goodhabitsforlife.com.

## Local dev (optional)
- Install Hugo Extended.
- Run: `hugo server -D`

## Deploy
Pushing to `main` triggers GitHub Actions to build and deploy the generated `public/` folder to your cPanel `public_html` via FTPS.

### Required GitHub Secrets
- `FTP_HOST` = your server IP (e.g., 162.241.116.114)
- `FTP_USERNAME` = FTP user
- `FTP_PASSWORD` = FTP password
- `FTP_PATH` = `/public_html`

## Next up
- [ ] Replace sample posts with real content
- [ ] Add favicon and social image in /static
- [ ] Configure Cloudflare cache rules for /css and /images
