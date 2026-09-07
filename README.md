# Raj Kikani — portfolio

A single-page graphic design portfolio. Plain HTML, CSS and JavaScript — no build step, no dependencies.

## Files

```
index.html                  the whole site (markup, styles and scripts in one file)
.nojekyll                   tells GitHub Pages to serve the files as-is
assets/RESUME_RAJ_KIKANI.pdf
assets/img/                 ten optimised WebP images (1.2 MB total)
```

## Put it online

1. Create a new repository on GitHub. Name it `raj-kikani` (or anything you like).
2. Upload every file and folder above, keeping the structure exactly as it is. `index.html` must sit at the top level, not inside a folder.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
5. Wait about a minute. Your site is live at `https://YOUR-USERNAME.github.io/raj-kikani/`.

To use `https://YOUR-USERNAME.github.io/` instead, name the repository `YOUR-USERNAME.github.io`.

## Before you share the link

**Make the Figma files public**, or the three prototype tiles will show a permission error. In each file: **Share → Anyone with the link → can view**. The three files are Nike Shoe, Juice Spin Animation and Food Delivery App.

Check the site on your phone too — the hero, grids and navigation all reflow, but it's worth seeing it yourself.

## Changing things

Everything lives in `index.html`. Search for what you want to edit.

**Colours** — the `:root` block at the top of the `<style>` section:

```css
--flame:#EF4A15;    /* AVAHAN orange, used across the poster half */
--violet:#4B21D9;   /* Feedspot purple, used across the editorial half */
--concrete:#DEDCD5; /* page background */
--paper:#FBFAF8;    /* light section background */
```

**Adding a project** — copy an existing `<figure class="print ...">` block, point `src` and `data-lb` at your new image, and rewrite the `alt`, `data-cap` and `<figcaption>`. The lightbox picks up new pieces automatically.

Save new images as WebP around 1500px on the long edge to keep the page fast. Column widths come from the `g-` and `f-` classes (`span 5`, `span 7`, and so on, out of 12).

**Adding a prototype** — copy an `<article class="tile">` block. The `data-embed` URL is your Figma link with `www.figma.com` swapped for `embed.figma.com` and `&embed-host=share` added to the end.

## Notes

- Type is Anton and Archivo, loaded from Google Fonts.
- The hero split responds to mouse, touch and arrow keys, and holds still if the visitor has reduced motion turned on.
- Prototypes only load when clicked, so the page stays light for someone on mobile data.
