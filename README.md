# Zizhao Tong — academic website

Minimal responsive personal site for `https://z2tong.github.io/`.

## Layout

- `index.html`: responsive research homepage (compact Research & Industry Experience and Education; no organization logos)
- `favicon.svg`: site icon
- `.nojekyll`: publish HTML and assets as-is
- `.github/workflows/sync-scope.yml`: copies all SCOPE published page resources from `z2tong/SCOPE` `page` branch to `SCOPE/` on an initial push or manual workflow dispatch; leaves the original repo unchanged.

## Deployment to GitHub

1. Create a **public** repository named exactly `z2tong.github.io` under the `z2tong` account, without an auto-created README or license.
2. Push this folder's contents to its `main` branch (including the hidden `.github/` and `.nojekyll`).
3. Visit the repository **Actions** tab and run **Sync SCOPE homepage assets** if it did not start automatically. Ensure its job succeeds and a commit adds `SCOPE/index.html` and `SCOPE/static/**`.
4. Visit **Settings > Pages**, select **Deploy from a branch**, `main`, `/(root)`, and save.
5. Check `https://z2tong.github.io/` and `https://z2tong.github.io/SCOPE/` after deployment and test SCOPE video playback. Keep the old SCOPE project's Pages setting intact until after this succeeds.

**Important:** `SCOPE/` binary assets (including videos) are intentionally not distributed in this small source archive. GitHub Actions copies them at the original quality from the existing `page` branch. If the workflow cannot push due to repository settings, allow GitHub Actions **Read and write permissions** in **Settings > Actions > General > Workflow permissions**, then rerun it.

The original `z2tong/uivid64.github.io` repository is not modified or needed.
