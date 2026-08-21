# coffee.han.life

Self-hosted buy-me-a-coffee page. Static HTML on S3 (`coffee.han.life`, ap-southeast-4) behind CloudFront (`E356Y1HU11XX9O`), DNS via Lightsail. Payments are Stripe Payment Links, so there is no backend.

## Deploy

Push to `main`. GitHub Actions (OIDC role `coffee-han-life-deploy`) syncs `site/` to S3 and invalidates CloudFront.

## Payment links

Four Stripe Payment Links are hardcoded in `site/index.html` (A$5 / A$15 / A$25 / custom amount). Currently **test mode** links (`donate.stripe.com/test_...`). To go live: create the same product/prices/links in livemode and replace the four hrefs.
