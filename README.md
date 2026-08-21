# coffee.han.life

Self-hosted buy-me-a-coffee page. Static HTML on S3 (`coffee.han.life`, ap-southeast-4) behind CloudFront (`E356Y1HU11XX9O`), DNS via Lightsail. Payments are Stripe Payment Links, so there is no backend.

## Deploy

Push to `main`. GitHub Actions (OIDC role `coffee-han-life-deploy`) syncs `site/` to S3 and invalidates CloudFront.

## Payment links

Four live Stripe Payment Links are hardcoded in `site/index.html` (A$5 / A$15 / A$25 / custom amount), product `prod_V6v1l5HT3NH7ol`. Amount or link changes happen in Stripe, then update the hrefs here.
