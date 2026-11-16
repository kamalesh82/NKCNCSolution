# NK CNC Solution

Static storefront for NK CNC Solution, Bengaluru: filterable tools and spares catalogue with variant pricing, cart, machine quote band and service request form. Plain HTML, CSS and JavaScript, with no build step.

## Structure

```
index.html          page markup
css/styles.css      all styles (light and dark mode)
js/app.js           product data, catalogue, cart, forms
assets/nk-logo.png  logo
.github/workflows/  GitHub Pages deploy
```

## Run locally

Open `index.html` in a browser, or serve the folder:

```
python3 -m http.server 8000
```

## Publish with GitHub Pages

1. Create a new repository on GitHub and push this folder to the `main` branch.
2. In the repo go to **Settings > Pages** and set **Source** to **GitHub Actions**.
3. Push to `main`. The workflow in `.github/workflows/pages.yml` publishes the site at `https://<your-user>.github.io/<repo>/`.

## Editing

- Products and prices: the `F` array near the top of `js/app.js`. Format is `{id, cat, name, fin, v:[[label, price], ...]}`.
- Categories: the `CATS` array in the same file.
- Contact details: `index.html` (hero plate, contact band and footer).

## Known limits

This is a preview. The cart is kept in the browser (localStorage), and the checkout and service forms do not send anywhere or take payment. For real orders, connect a payment provider and a form backend, or use the Shopify theme version.
