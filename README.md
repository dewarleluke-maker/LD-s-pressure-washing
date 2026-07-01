# Gold Standard Pressure Washing — Website

A 4-page marketing website for Gold Standard Pressure Washing, serving
Riverbend and south Edmonton, Alberta. Plain HTML/CSS/JS — no build step,
no framework, deploys anywhere.

## Pages

- `index.html` — Home (hero, services, why us, FAQ)
- `services.html` — Driveway & concrete, deck & fence, square footage estimator
- `about.html` — About the business
- `contact.html` — Contact form + phone/email
- `thank-you.html` — Shown after a contact form submission

The Gallery page has been removed for now until real before/after job
photos are available. Re-add `gallery.html` and its nav link once you have
photos to show.

## Running locally

No build needed. Just open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

## Contact info

The site is live with real contact info:

- Phone: 587-905-6233
- Email: Luke@gold-standard-pressure-washing.ca

Remember: the first contact form submission triggers a FormSubmit
confirmation email to that address — click the link in it before
further submissions will be delivered (see "Contact form" below).

## Contact form

The contact form submits to [FormSubmit.co](https://formsubmit.co), which
emails submissions straight to the address in the form's `action` URL, with
no backend or account required.

**Important:** the first time the form is submitted, FormSubmit sends a
one-time confirmation email to that address. You must click the
confirmation link in that email before further submissions will be
delivered. After that, it works automatically.

Only Name, Phone, and Project Description are required — Email and Address
are optional fields for the customer.

## Square Footage Estimator

The estimator on `services.html` gives an instant price range based on
square footage and service type, calculated in `js/main.js`:

| Service             | Rate per sqft | Minimum |
|----------------------|---------------|---------|
| Driveway / Walkway   | $0.22–$0.28   | $150    |
| Deck Washing         | $0.25–$0.32   | $150    |
| Full Package         | $0.20–$0.26   | $200    |

Sealing uses a different formula instead of a per-sqft range: a flat $200
for any job 500 sqft or smaller, then $0.50/sqft for footage beyond 500
(so 600 sqft = $200 + 100 × $0.50 = $250). This guarantees a $200 minimum
per sealing job regardless of how small the driveway is.

These rates are estimate-only; the displayed note always clarifies that
final pricing is confirmed on-site.

## Placeholder images

All photos currently come from inline-generated SVG placeholders as
stand-ins. Replace the `src` attributes in the HTML with real job photos
when you have them — recommended size ~700x560 for hero/about images,
~500x400 for service cards.

## Deploying

Since this is a static site, any of these work with zero configuration:

- **Netlify** — drag-and-drop the folder onto [app.netlify.com/drop](https://app.netlify.com/drop), or connect the GitHub repo for continuous deployment
- **GitHub Pages** — push to a repo, enable Pages on the `main` branch
- **Vercel** — `vercel deploy` from this folder
