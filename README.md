# Hyper-V Launcher website

Source for the public website at https://hypervlauncher.andrezammit.com/. The page uses GitHub Pages with the Cayman Jekyll theme.

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

The site does not link to the application repository or releases; those become inaccessible to public visitors after the application repository is made private.
