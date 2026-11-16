# LINKER FAIZAN

Cloudflare Worker link-in-bio maker using the existing Cloudflare KV namespace.

## Files
- `_worker.js` — application, page UI, SEO metadata, animated in-page brand mark, API and Google verification route.
- `wrangler.jsonc` — Worker name, entry file and existing KV binding.
- `googlefbc46c776af9c892.html` — Google Search Console verification file.

## Deploy from GitHub / Wrangler
1. Put these files in the root of the GitHub repository.
2. In Cloudflare Workers, connect the repository to the Worker named `faizan-fathima`.
3. Use the Wrangler deploy command: `npx wrangler deploy`.
4. Confirm that the Worker has the KV namespace binding variable named `LINKS` and that its namespace ID matches the ID in `wrangler.jsonc`.

## Important
- This configuration points to the existing KV namespace ID provided for this project. Do not create a new namespace or delete the existing one.
- The app needs the `LINKS` KV binding to save and load pages.
- Google verification is served at `/googlefbc46c776af9c892.html`. After deployment, open that path on your domain and then complete verification in Google Search Console.
- The logo animation is inside the webpage. The Android/PWA home-screen launcher icon itself remains static.
- SEO metadata helps search engines understand the site but does not guarantee indexing.
