# Hyper-V Launcher website

Source for the public website at https://hypervlauncher.andrezammit.com/. The site is custom static HTML and CSS, served by GitHub Pages. No theme, JavaScript, or build step is required.

## Publish

1. Create a **public** GitHub repository named `hypervlauncher-site` under `andrezammit`, without an initial README.
2. From this folder, run:

   ```powershell
   git push -u origin main
   ```

3. In the new repository's **Settings > Pages**, choose **Deploy from a branch**, `main`, `/(root)`. Check the temporary GitHub Pages URL and its images.
4. In the old `hypervlauncher` repository's **Settings > Pages**, remove the custom domain.
5. In the new repository's **Settings > Pages**, set `hypervlauncher.andrezammit.com` as the custom domain. GitHub will create the root `CNAME` file.
6. Check the custom-domain page and images, then make the application repository private.

## Downloads

The page links to setup EXE and MSI assets in this public repository's GitHub Releases. The application repository's Release workflow builds and verifies the setup files, then publishes them here using its `RELEASE_TOKEN` Actions secret. See the application repository's `Setup/README.md` for token setup and release instructions.

The `releases/latest/download/` links automatically follow the latest release. Keep the asset names `HyperVLauncher.Setup.exe` and `HyperVLauncher.Setup.Installer.msi` unchanged. Download links become available after the first successful release. Application source remains in the separate application repository; release tags here refer to website commits.

## Local preview

Serve this folder with any static HTTP server and open index.html. The landing page is in index.html and the illustrated usage guide is in guide.html, with styles.css and the original screenshots in Images/. The .nojekyll file disables theme processing.

The previous Markdown page is retained as reference; index.html is the website entry point. Download links remain pointed at this repository's latest public release.

## Search and sharing

Both pages have unique titles and descriptions, canonical URLs, Open Graph and Twitter preview metadata, and JSON-LD structured data. Preview images use the original application screenshots. The homepage describes the software without invented ratings or reviews; this does not claim eligibility for a Google software-app rich result.

The canonical domain is https://hypervlauncher.andrezammit.com/. Keep canonical URLs, structured data, social image URLs, robots.txt, and sitemap.xml in sync if this changes. The sitemap includes only the homepage and guide. Add new public HTML pages when they are created; do not add download assets or fragment links. No artificial last-modified dates are used.

After publishing:
- Confirm the custom domain, HTTPS, both pages, robots.txt, sitemap.xml, and social image URLs return successfully.
- Confirm the GitHub Pages address redirects to the custom domain.
- Add or verify the domain in Google Search Console, submit sitemap.xml, and inspect both page URLs.
- Validate deployed JSON-LD with Schema.org Validator and check actual indexing in Search Console. Metadata and valid structured data do not guarantee indexing or rich results.
