# brontopoint.com

Landing page for Brontopoint Systems Inc. A single static page served by GitHub Pages: `index.html`, `CNAME` (brontopoint.com) and `.nojekyll`. No build step.

## Go-live checklist

1. **Register the domain.** Buy `brontopoint.com` at a registrar (e.g. Cloudflare, Namecheap, Google-compatible registrars). If it is taken, pick the fallback and update `CNAME`, the mailto links and the JSON-LD in `index.html`.
2. **Create the GitHub org and repo.** Create the org `brontopoint` (separate from `zlhk100` and `hopbound`), then a repo named `brontopoint.github.io`. Push this folder:
   ```
   git remote add origin git@github.com:brontopoint/brontopoint.github.io.git
   git push -u origin main
   ```
3. **Verify the domain on GitHub first.** Org Settings → Pages → Add a verified domain → add the TXT record it gives you at your registrar. This prevents domain takeover.
4. **DNS records at the registrar.**
   - `A` @ → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` www → `brontopoint.github.io`
   (Check GitHub's "Managing a custom domain for your GitHub Pages site" docs for the current addresses.)
5. **Turn on Pages.** Repo Settings → Pages → Deploy from branch `main` / root → Custom domain `brontopoint.com` → tick **Enforce HTTPS** once the certificate is issued (can take from minutes up to about a day).
6. **Email.** Cloudflare Email Routing forwards `contact@` (public, on the site) and `lei.zhou@` to Gmail; catch-all is off. If a paid mailbox (Google Workspace or Microsoft 365) is added later, replace the routing MX records with the provider's and set up SPF, DKIM and DMARC for sending.
7. **Check.** Open https://brontopoint.com on a phone and a laptop; send a test email to contact@ from a personal account.

## Brand
- Mark: `assets/brontopoint-mark.svg` (on a white rounded square) and `assets/brontopoint-logo.svg` (transparent). A tensor of dots: random orange input settles through sky blue into a navy structure — non-deterministic in, predictable out.
- Palette, three colours only, shared with Lei Zhou's personal mark: orange `#F15A29`, sky blue `#37AFE4`, navy `#2E3192`.
