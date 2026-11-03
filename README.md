# Harness Kit: pre-launch waitlist landing

Status: ready, NOT published. Product does not exist yet (page says so).

## Files
- index.html: static landing (English), waitlist + price test
- .nojekyll: disables Jekyll on GitHub Pages

## Price test
- Variants: A = US$ 49, B = US$ 79, 50/50 random via JS
- Stored in localStorage key `hk_price_variant` (same visitor sees same price)
- Variant goes in the email subject: `Harness Kit waitlist [variant A US$49]`

## Email capture (zero cost, no new accounts)
mailto: form to renandlsantos.ai@gmail.com. Opens the visitor's email app prefilled.
Limitations:
- Signup only counts if visitor actually presses send; no fallback without a mail client (webmail-only users may see nothing)
- No conversion data for visitors who don't send (cannot compute rate per variant without analytics)
- Counting = Gmail search `subject:"Harness Kit waitlist"`, split by `variant A` / `variant B`
- Possible future upgrade: free form backend (needs account, not done)

## Publish (Kanan)
1. Create public repo `harness-kit` in `renandlsantos-ai-agent`
2. Push index.html, .nojekyll, README.md to `main` root
3. Settings > Pages > Deploy from branch > main / (root)
4. Expected URL: https://renandlsantos-ai-agent.github.io/harness-kit/
