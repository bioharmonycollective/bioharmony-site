# Bioharmony Collective website

Static site for bioharmonycollective.org. Three pages, no build step.

- `index.html`: Home
- `ministry.html`: The Ministry (beliefs, structure, stewards, legal standing)
- `membership.html`: Membership (offerings, the way in, request form, questions)
- `assets/`: `site.css`, `bhc-mark.png` (header mark and favicon), `bhc-logo.png` (full logo)

## Launch on GitHub Pages

1. Push these files to the root of the repository's `main` branch.
2. Enable Pages: `gh api -X POST repos/OWNER/REPO/pages -f "source[branch]=main" -f "source[path]=/"`
   (or Settings, Pages, deploy from branch `main`, folder `/`).
3. The site appears at `https://OWNER.github.io/REPO/`. All links are relative, so it works at that path and at a custom domain.
4. Custom domain: add a `CNAME` file containing the domain, then point DNS at GitHub Pages. Do this only after the checklist below is done, because it replaces the live Go High Level site.

## Before this replaces the live site

Search the HTML for `[` to find every placeholder.

- `index.html`: hero photo slot. Add the photo to `assets/` and replace the placeholder block with an `<img>`.
- `ministry.html`: link to the Statement of Faith, and check the four belief lines against it.
- `ministry.html`: no-inurement sentence, to be added after the written policy is adopted.
- `membership.html`: confirm energy exchange wording, then remove the note.
- `membership.html`: the request form does not submit anywhere yet. Replace it with the Go High Level form embed, or point the button at the Go High Level membership form.
- Every page carries `<meta name="robots" content="noindex">` so search engines skip the draft. Remove that line at launch.

## Language rules for any edit

Bioharmony Collective is a 508(c)(1)(a) Private Ministerial Association. Keep these in all copy.

- Say: Private Ministerial Association, spiritual ministry, members, tithes, donations, energy exchange, ministry offerings, within the private domain.
- Avoid: company, business, brand, store, customers, clients, users, products for sale, retail, nonprofit, 501(c)(3), financial opportunity.
- Origin Institute and Origin Temple are allied companions with their own governing documents. Do not present them as departments of Bioharmony Collective.
- Keep the private domain notice and the health notice in every footer.
- No em-dashes.
