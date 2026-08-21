# coffee.han.life

Self-hosted buy-me-a-coffee page. Static HTML on S3 behind CloudFront, DNS via Lightsail. Payments are Stripe Payment Links, so there is no backend.

## Deploy

Push to `main`. GitHub Actions (OIDC) syncs `site/` to S3 and invalidates CloudFront.

Payment links are hardcoded in `site/index.html`; amount changes happen in Stripe, then update the hrefs.
