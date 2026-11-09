# The Living Studio — GitHub Pages website

A botanical, cozy, responsive static website with pages for art, dance, gardening, library archive, workshops, online classes, events, shop, and membership.

## Publish on GitHub Pages

1. Create a **public** GitHub repository (or use an existing one). Upload all files and folders from this package to the repository root.
2. In **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
3. Wait for GitHub to provide your site URL. Links use relative paths, so project repositories work too.
4. For a custom domain later, follow GitHub Pages custom-domain instructions.

## Add or edit classes, events, products

1. Open `editor.html` on your deployed site (or run a local HTTP server: `python -m http.server 8000` in this folder and open http://localhost:8000/editor.html).
2. Choose **Classes**, **Events**, or **Shop products**. Add, edit, or delete entries and click **Save locally**.
3. Click **Download JSON** for the collection you edited.
4. In GitHub, upload/replace `data/classes.json`, `data/events.json`, or `data/shop.json` with the downloaded file, then commit the change. Your public site will update after deployment.
5. Repeat for other collections. **Local browser edits are not public until you commit the exported JSON.** They are stored only in that browser; clearing browser storage removes drafts. Export regularly.

### Listing formats
- Classes: set **Library archive**, **In person**, or **Online** to determine which page shows a class.
- Events: use `YYYY-MM-DD` dates and optional start time; the calendar and home page update automatically.
- Products: enter a hosted checkout URL only after your payment provider has created one. Never collect card data directly in this static site.
- Images: use a publicly accessible `https://` image URL, or add your images to `assets/images/` and update the site to support relative image paths. The current editor accepts public HTTPS URLs.

## Important limitations

- This is a **static site**, not a secure member portal. `editor.html` is public and edits are browser-local, so it is not an authenticated administration interface. Anyone can open it, but only people with repository write access can publish changes.
- Paid subscriptions, customer accounts, class registration, email newsletter signups, live classes, and payments require third-party providers or a backend. The current website displays these as planned, not active.
- The included archive entries (Pipe Cleaner Orchids and Sea Glass Trees) are starting examples. Confirm details, dates, photos, and descriptions before launch.
- No real business email, address, prices, checkout links, or event dates have been invented.
- Test changes locally through an HTTP server, not by double-clicking `index.html`, because JSON loading uses fetch.

## Files

`index.html`, `library.html`, `workshops.html`, `calendar.html`, `online.html`, `shop.html`, `membership.html`, `about.html`, `editor.html`, `assets/style.css`, `assets/site.js`, and JSON files in `data/`.
