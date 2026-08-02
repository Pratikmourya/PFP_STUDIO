# PFP//STUDIO

A browser-based tool that recolors the default Instagram-style avatar (background + person)
and exports it as a free PNG. No sign-up, no server, no uploads — everything renders and
downloads client-side.

## Publish it on GitHub Pages

1. Create a new repo on GitHub (e.g. `pfp-studio`), public.
2. From this folder:
   ```bash
   git init
   git add index.html privacy-policy.html README.md
   git commit -m "Initial PFP Studio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch →
   Branch: main / (root)**. Save.
4. Your site goes live at `https://<your-username>.github.io/<repo-name>/` within a minute
   or two. `index.html` is the file GitHub Pages looks for by default — it's already named
   correctly here.
5. Optional: add a custom domain under **Settings → Pages → Custom domain**, and set a
   `CNAME` DNS record pointing at `<your-username>.github.io`.

## Adding ads

The HTML already has two placeholder ad slots (top banner, under the header; bottom banner,
above the footer) marked `<!-- AD SLOT -->`, plus a commented loader script in `<head>`.

Most people start with **Google AdSense** since it doesn't require pre-existing traffic to
apply, but a few things are worth knowing before you count on it as income:

- **You need to apply and get approved first.** AdSense reviews the site for original
  content, a working privacy policy (included here — fill in the placeholders), and no
  policy violations. Approval can take anywhere from a day to a few weeks.
- **A single-tool page like this tends to get a fairly low RPM** (revenue per 1,000 views)
  compared to content sites, because there's only one page and people leave quickly after
  downloading. Realistic expectations: meaningful passive income needs real, recurring
  traffic — usually from search (SEO), social sharing, or being embedded/linked elsewhere —
  not just having ads installed.
- **Once approved**, uncomment the loader `<script>` tag in `<head>` and the `<ins
  class="adsbygoogle">` block inside each `.ad-frame`, and replace `ca-pub-XXXXXXXXXXXXXXXX`
  / `data-ad-slot="XXXXXXXXXX"` with the values from your AdSense account.
- **Create an `ads.txt` file** at the site root once you have your publisher ID — AdSense
  gives you the exact line to put in it. Without it, AdSense will flag the site.
- **Alternatives to AdSense** if you don't get approved or want to compare: Media.net,
  Ezoic (better for lower-traffic sites), or direct/affiliate placements (e.g. a link to a
  design tool or hosting service relevant to your audience) — these don't need the same
  approval bar.
- Keep it to the two slots already placed. Stacking more ads on a one-page utility tool
  usually hurts both user experience and AdSense's own policy compliance review.

## Files

- `index.html` — the site (same as `pfp-generator.html`, duplicated so GitHub Pages finds it)
- `privacy-policy.html` — required by AdSense; fill in the `[date]` and `[your email]` placeholders
- `README.md` — this file
