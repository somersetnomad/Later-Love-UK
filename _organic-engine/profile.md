# Later Love UK: organic-engine-pages profile

## Site
- Repo: somersetnomad/Later-Love-UK (Jekyll on GitHub Pages, Axiom theme)
- Live URL: https://somersetnomad.github.io/Later-Love-UK/
- State: this folder (`_organic-engine/`, not served by Jekyll)

## Offer
- Affiliate: OurTime UK (over-50s dating, Match Group) through FlexOffers
- Affiliate link lives in `_config.yml` under `affiliate.ourtime.url`. It is EMPTY until FlexOffers approves the owner; while empty, `{% include affiliate-cta.html brand="ourtime" ... %}` renders nothing. Never paste a raw affiliate URL into a post; always use the include.
- Buyer action: try OurTime UK free, then subscribe
- Only OurTime has an affiliate link. eharmony and Match are covered honestly with no links of ours.

## Audience
- People over 50 in the UK looking for a relationship online, weighing up which site, what it costs, and whether it's safe

## Positioning
- Honest and safety-first. Real prices with check dates, renewal and cancellation details, member complaints reported as they are (OurTime's Trustpilot score is poor; say so), and safety guides with no affiliate links.
- Never fabricate testimonials, success stories, member numbers or experiences. Stock photos of people are captioned as models where they could be mistaken for members.

## Theme and post format
- Axiom theme ported to Jekyll (assets/axiom; site layer in assets/css/site.css and assets/js/site.js)
- Format per the axiom-post skill: answer box first, 2-6 H2 sections, H3 sub-parts, footnotes for asides/sources/technical detail (about one per 150-300 words), "Questions people ask" H2 with H3 questions plus matching `faq` front matter, a "Sources" H2. `description` is the one-sentence excerpt (<160 chars). 1-3 tags, primary first. `template: default`.
- Posts that carry the affiliate CTA set `affiliate: ourtime` in front matter; safety posts carry none.
- Hero image front matter: `image` (fm=jpg), `image_base`, `image_width`, `image_height`, `image_alt`, `image_credit`.

## Voice
- Plain, warm, direct, respectful of readers' experience. No patronising "seniors" language; say "over 50s" or "later life". No AI filler.

## Owner facts (only use what is listed here)
- Bala Danmeri writes the site from Somerset; also writes science fiction and metaphysical philosophy; trades as Noor Intelligence; contact info@baladanmeri.com
- [[NEEDED]] any personal or permitted second-hand experience of dating over 50

## Mode and schedule
- Launch: 5 guides published 29 Oct 2026
- AUTO weekly autopilot from Oct 2026: one post every Friday morning (scheduled task "Later Love UK weekly post"); process in RUNBOOK.md. Affiliate buttons stay hidden until the owner adds the FlexOffers link.
