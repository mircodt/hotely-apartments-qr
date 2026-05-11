# Hotely Apartments — QR Cavaliere Landing

Landing page for the Hotely.ai QR cavaliere offer for short-term rentals.

**Offer:** $19.99 / year per apartment + shipping → unlock the step-by-step tutorial + get the custom-branded QR cavaliere (your logo printed) shipped to your door. Renews yearly, cancel anytime.

## Live preview

A single static `index.html` file — no build step.

```bash
npx serve .
# or
python3 -m http.server 4321
```

Then open <http://localhost:4321>.

## Before going live

In `index.html`, search for `CHECKOUT_URL` and replace the placeholder with your real Stripe Payment Link:

```js
const CHECKOUT_URL = 'https://buy.stripe.com/REPLACE_ME';
```

On the Stripe Payment Link, configure:

- **Annual recurring price** of $19.99
- **Collect shipping address** (we need it for the cavaliere)
- **Shipping rates** per country (Stripe shipping rates)
- A custom field for the logo upload, or redirect to a post-success page that collects it

## Brand

Built with the Hotely.ai brand identity (primary `#6C3AED`, accent `#06B6D4`, Inter, aurora-glass nav, animated-gradient CTAs).
