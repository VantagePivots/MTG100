# Mini Tray G

Website for Mini Tray G, the 3D-printed sunroof and roof mount for Starlink Mini by Vantage Pivots. It has a product page and a reader for the print and assembly manual, MTG-100.

## What is here

| Path | What it is |
| --- | --- |
| `index.html` | Product page |
| `manual/index.html` | Manual reader: the manual's own pages, with a section list, search and a PDF download |
| `files/MTG-100_Rev_B.pdf` | The manual |
| `assets/site.css` | Styles for both pages |
| `assets/reader.js` | The reader. It loads PDF.js 3.11.174 from cdnjs |
| `img/` | Renders used on the product page |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

The print files, STEP files and the other guides are not in this repository. They come with the plans.

## Publish with GitHub Pages

1. Create a new repository on GitHub. On a free account it must be public for Pages to work.
2. Upload everything in this folder to the root of the repository, keeping the folders as they are.
3. In the repository go to **Settings → Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*, the branch to `main` and the folder to `/ (root)`. Save.
4. After a minute or two the site is live at `https://<your-user>.github.io/<repository>/`.

To use your own domain, enter it under **Settings → Pages → Custom domain** and add the DNS record GitHub shows you.

## Set the store link

Near the end of `index.html`, set `STORE_URL` to the address of your plans listing. The **Buy the plans** button stays hidden while it is empty.

## Update the manual

1. Replace `files/MTG-100_Rev_B.pdf` with the new PDF.
2. If the file name changes (for example to `MTG-100_Rev_C.pdf`), change `PDF_URL` in `assets/reader.js` and the PDF links in `index.html` and `manual/index.html`.
3. If sections move to different pages, update `SECTIONS` in `assets/reader.js` and the page numbers in the manual list in `index.html`.
4. Change the revision shown under the title in `manual/index.html`.

## Link preview

`img/og.jpg` is a 1200 × 630 preview picture. Once you know the site's address, add this line to the `<head>` of `index.html`:

```html
<meta property="og:image" content="https://<your-site>/img/og.jpg">
```

## Rights

The manual, images and text are © 2026 Vantage Pivots. All rights reserved.

Starlink is a trademark of Space Exploration Technologies Corp. Mini Tray G is an independent design and is not affiliated with or endorsed by SpaceX.
