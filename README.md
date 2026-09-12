# maddalenagrignani.github.io

Source for https://maddalenagrignani.github.io — plain HTML, no build step.
GitHub Pages publishes whatever is on `main`.

```
index.html              home page
research/index.html     /research/
teaching/index.html     /teaching/
style.css               shared styles for all three pages
images/                 photos (banners + portrait)
papers/                 CV and working papers (PDF)
sitemap.xml, robots.txt search-engine files - update sitemap lastmod when pages change
googled181db49c38ee583.html   Search Console verification - must stay at the root
```

## Adding a working paper

1. Upload the PDF to `papers/` with a stable name, e.g. `papers/Grignani_JMP.pdf`.
   Keep the same filename when you upload a new version, so links never break.
2. In `research/index.html` (and `index.html` if it is in Selected Work), make the
   title the link:

   ```html
   <div class="paper-title"><a href="/papers/Grignani_JMP.pdf" target="_blank" rel="noopener">Title of the paper</a></div>
   ```

## Swapping a banner photo

Change the filename in the `.banner-*` rule in `style.css`, and set that rule's
`aspect-ratio` to the new image's pixel size (e.g. `2000 / 524`) so it shows whole.
Then bump the `?v=` number on the `style.css` link in all three HTML files so
browsers fetch the new stylesheet.
