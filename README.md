# Hotely Apartments — QR Cavaliere Landing

Landing page for the Hotely.ai QR cavaliere offer for short-term rentals.

**Offer:** Pay $9.99 once → unlock the step-by-step tutorial + get the physical QR cavaliere shipped free + first month included. Then $9.99/month, cancel anytime.

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

On the Stripe Payment Link, enable:

- **Collect shipping address** (we need it for the cavaliere)
- A custom field for the logo upload, or redirect to a post-success page that collects it

## Brand

Built with the Hotely.ai brand identity (primary `#6C3AED`, accent `#06B6D4`, Inter, aurora-glass nav, animated-gradient CTAs).
