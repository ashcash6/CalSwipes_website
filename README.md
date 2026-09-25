# CalSwipes website

A dependency-free static website with Home, Support, and Privacy Policy pages. No client JavaScript, database, authentication, tracking, external fonts, or stock photography.

## Run locally

Install Node.js if needed, open a terminal in this folder, and run:

```sh
node serve.mjs
```

Open http://127.0.0.1:4173. Stop the server with Ctrl+C. All published files are in `dist/`; no build is necessary.

## Deploy to GitHub Pages

1. Create a GitHub repository and upload this folder's contents, including `dist/` and `.github/workflows/pages.yml`.
2. In the repository's Settings → Pages, select **GitHub Actions** as the source.
3. Push to the `main` branch (or run the “Deploy static website” workflow manually).
4. Open the URL shown by the successful Pages deployment.

The workflow publishes only `dist/`. Relative links work for both a repository URL (such as `https://USERNAME.github.io/REPOSITORY/`) and a custom domain. `/support` and `/privacy` resolve to directory pages; GitHub Pages normally redirects these to `/support/` and `/privacy/`. Under a repository URL, include the repository prefix. Use the final Pages URL plus `support/` and `privacy/` in App Store Connect.

The `.openai/hosting.json` file is used only for the separately hosted Sites copy. GitHub Pages does not need it.

## Add the App Store URL

In `dist/index.html`, search for `APP_STORE_URL`. Replace the disabled button with the anchor described in that comment, using the real, verified App Store listing URL. Remove the “App Store link coming soon” text, keeping “Free for iPhone” if still accurate. No App Store URL has been invented.

## Update support email

Search for `support.calswipes@gmail.com` in `dist/support/index.html` and `dist/privacy/index.html`. Replace both the visible email text and every `mailto:` destination.

## Update the privacy policy

Edit `dist/privacy/index.html`. Search for `Last updated: September 24, 2026` to change the date. Keep the policy aligned with the released app's actual behavior. The current text uses only the supplied facts. Manual dining-hall selection is deliberately omitted because it was unverified.

## Connect a custom domain later

For GitHub Pages, add the domain in Settings → Pages → Custom domain, and configure the DNS records at your domain provider following GitHub's official guide. Enable HTTPS once available. For this Actions deployment, keep the custom domain configured in the repository settings. If migrating the domain to another host, update DNS for that host instead.

- [GitHub Pages publishing setup](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [Custom domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

## Editing

Edit the HTML files directly. Shared presentation is in `dist/styles.css`; each page embeds the same small CalSwipes favicon. Keep relative links intact. After any edit, preview all three pages at desktop and mobile sizes and redeploy.

© 2026 Ashkon Chaghajerdi and Dylan Brown
