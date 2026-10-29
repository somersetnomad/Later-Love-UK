# Later Love UK weekly run

The scheduled task follows this file. `profile.md` holds site facts, positioning, voice and owner facts; if they disagree, profile.md wins on facts and this file wins on process. If the `organic-engine-pages` or `axiom-post` skills are installed, load them too; this file takes priority.

## Mode
AUTO: publish directly to `main` when every quality-gate item passes. If anything fails or needs the owner, push a branch `organic-engine/<slug>` instead, publish nothing live, and say what's needed in the summary. One new post per run, never more than one per week.

## Affiliate rule
- The only affiliate is OurTime UK. Use `{% include affiliate-cta.html brand="ourtime" kicker="..." lead="..." button="..." %}` (see existing posts) and set `affiliate: ourtime` in front matter. Never paste a raw affiliate URL. The include stays hidden until the owner sets `affiliate.ourtime.url` in `_config.yml`; never edit that value yourself.
- Safety posts (scams, first dates, privacy, wellbeing) carry NO affiliate include.
- Other dating sites are covered honestly with no links of ours, and a disclosure line where OurTime appears alongside them.

## Steps
1. Attach `somersetnomad/Later-Love-UK` with push access (add_repo), clone it, read every file in `_organic-engine/`.
2. **Refresh first:** if a published post has a broken link, an outdated price/rule/date, or a clear weakness, fix one at most, update its `last_modified_at`, and log it. Prices older than ~3 months should be re-checked.
3. **Pick the topic:** highest-priority `queued` item in `queue.csv` that doesn't need owner facts missing from profile.md. Buyer-intent topics first (deciding on or paying for a dating site), with a safety guide roughly one week in four. If fewer than 6 usable items remain, research demand (UK over-50s dating searches, forums, competitor gaps) and add more.
4. **Research and brief** with web search. Search before stating any current price, plan, rule or statistic. Cite primary sources (the dating sites' own help pages, Report Fraud, police, gov.uk, Get Safe Online, Ofcom). Report member complaints honestly.
5. **Write** in the profile's voice. Never invent experiences, testimonials, success stories or member numbers. Format: answer box first, 2-6 H2 sections, H3 sub-parts, footnotes for asides/sources/detail, "Questions people ask" H2 with H3 questions plus matching `faq` front matter, "Sources" H2. `description` <160 chars, title <=60 chars, 1-3 tags, `template: default`.
6. **Images:** one hero (landscape) plus optional in-body. Find on Unsplash with WebSearch, WebFetch each photo page for photographer, `@username`, images.unsplash.com URL and licence line. Free Unsplash License only (skip Unsplash+ / plus.unsplash.com), not already in `images.csv`, no public figures, no visible brand logos. Download a small copy (curl images.unsplash.com works) and look at it before using. Photos of people are captioned "Models, not members" where they could be mistaken for users. Credit with `utm_source=later_love_uk&utm_medium=referral`. Hero front matter: `image` (fm=jpg), `image_base`, `image_width`, `image_height`, `image_alt`, `image_credit`. Log in `images.csv`.
7. **Quality gate:** answer-first opening; information gain; every factual claim sourced; every outbound link and image URL resolves (WebFetch or curl); affiliate rule obeyed; links to and from at least one existing post (edit an older post to link in); no AI filler; no patronising language.
8. **Publish:** save `_posts/YYYY-MM-DD-<slug>.md`, commit to `main` with `organic-engine: publish <slug>`, push. Wait for the "pages build and deployment" run for the commit (public API: `repos/somersetnomad/Later-Love-UK/actions/runs?branch=main&per_page=1`) and confirm `success`. If it fails, fix and push again; if it still fails, revert and report. RubyGems is blocked in the sandbox, so don't try to build locally.
9. **Log:** update `queue.csv`, `changelog.md`, `tracking.csv` (spot checks labelled `spot_check` / `ai_spot_check`; never claim rankings you didn't observe).

## Hard rules
No fabricated facts, reviews, testimonials or statistics. No link schemes. No structural changes (deleting pages, redirects, robots rules, theme files under `assets/axiom/`, `_config.yml` affiliate values) without asking.

## Summary to the owner (SendUserMessage)
What went live (title and link) and whether it carries the OurTime button, anything refreshed, tracking notes with source, anything waiting on Bala (e.g. FlexOffers link), and the next two topics.
