# Push the prepared personal website

This checkout has an initial commit on `main` with the remote set to
`https://github.com/z2tong/z2tong.github.io.git`.

From inside this folder, with authenticated GitHub access:

    git push -u origin main

Then enable **GitHub Pages** under **Settings > Pages** (Deploy from a branch,
main, /root) if not already enabled.

The included GitHub Actions workflow (`Sync SCOPE homepage assets`) copies the
full `page` branch from the original `z2tong/SCOPE` project into `SCOPE/` and
commits it. If the action does not run on initial push, trigger it from Actions.
The project's source repository is never changed by this workflow.

If Actions cannot push, enable **Read and write permissions** for GitHub Actions
under **Settings > Actions > General** and rerun the workflow.
