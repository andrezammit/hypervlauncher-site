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

Serve this folder with any static HTTP server and open index.html. The custom page is in index.html, with styles.css and the original screenshots in Images/. The .nojekyll file disables theme processing.

The previous Markdown page is retained as reference; index.html is the website entry point. Download links remain pointed at this repository's latest public release.
