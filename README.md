# NEOO GADGET BD — starter website

This is a starter implementation, not a fully launched store. It includes a responsive storefront, sample product cards, checkout form, delivery charge calculation (Dhaka ৳90 / outside Dhaka ৳150), and server-side API route placeholders.

## Run locally
1. Install Node.js 20 or later.
2. Extract this project.
3. Run `npm install`
4. Copy `.env.example` to `.env.local`.
5. Run `npm run dev` and open http://localhost:3000

## Deploy free
1. Push the project to a private GitHub repository.
2. Import it into Vercel.
3. Add environment variables in Vercel Project Settings → Environment Variables.
4. Deploy. Free hosting quotas and terms can change; review the provider's current limits.

## Business Koro integration
Do not guess the API endpoint or authentication scheme. Obtain the official Business Koro API documentation. Then set:
- `BUSINESS_KORO_API_KEY`
- `BUSINESS_KORO_API_BASE_URL`
- `BUSINESS_KORO_TEST_PATH`
- `BUSINESS_KORO_ORDER_PATH`

The test route intentionally does not make a request until the official authentication and endpoint contract is implemented. Order route currently validates and acknowledges a sample order but does not persist it or submit it to Business Koro. Add a database (e.g. Supabase) and implement the exact documented request/response mapping before accepting real orders.

## Payments
COD is the only enabled payment flow. bKash/Nagad options are displayed as pending and are rejected by the server until a verified merchant gateway is integrated. Obtain merchant credentials and official gateway documentation; never collect PINs or OTPs.

## Before going live
- Replace sample products, prices, descriptions, images, and contact information.
- Implement secure admin authentication (the current admin page is a UI placeholder, not production authentication).
- Add persistent database storage, order management, stock handling, and notifications.
- Implement and test Business Koro API against its official docs.
- Integrate verified bKash/Nagad merchant checkout.
- Add privacy policy, return/refund policy, terms, and customer support details.
- Test HTTPS, input validation, rate limiting, backups, and error handling.
