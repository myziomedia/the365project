# 400 Photo Grid Website

This folder turns the local photo grid into a view-only website.

## Files

- `index.html` is the public page. Visitors can only view it.
- `editor.html` is your editing page. Anyone can open it, but only someone with your GitHub token can publish changes.
- `grid-data.json` is the public data file that stores the saved grid.

## How Updates Work

The original local file saved into your own browser, so nobody else could see those changes.

This version keeps the same local autosave, and it can also publish `grid-data.json` to GitHub. When GitHub Pages serves this folder, visitors see the latest published `grid-data.json`.

## GitHub Pages Setup

1. Create a GitHub repository, for example `photo-grid`.
2. Upload these three files to the repository root:
   - `index.html`
   - `editor.html`
   - `grid-data.json`
3. In GitHub, open the repository settings and turn on Pages for the `main` branch.
4. Open the public Pages URL to view the grid.
5. Open `/editor.html` on that same site to edit.

## Publishing Settings

In `editor.html`, open **Publishing Settings** and fill in:

- GitHub owner: your GitHub username
- Repository: the repository name
- Branch: usually `main`
- GitHub token: a fine-grained token with Contents read/write access for that repository

Then click **Save Settings**.

After that, edits autosave in your browser and publish online automatically. You can also use **Publish Now**.

Images are resized for web viewing before they are saved, which keeps the public `grid-data.json` from becoming too large.

## Privacy Note

The GitHub token is stored only in your browser's local storage. Do not enter it on someone else's computer. Visitors without the token can view `index.html`, but they cannot change the hosted site.
