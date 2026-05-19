# CLAUDE.md — Mohan Sashank Portfolio

## Project Overview
This is Mohan Sashank's freelance video editing portfolio website. It is a single-page conversion funnel targeting potential clients who have found him via social media.

## Editor Config
- **Name / Brand**: Mohan Sashank
- **Niche**: Multi-niche (military/war content, motivational, short-form). Visual style leans minimal.
- **Style / Vibe**: Sleek & minimal + modern & techy. Dark SaaS aesthetic.
- **Reference sites**: https://www.stinsonedits.com/ (directional inspiration only)

## Brand Colours
- **Dominant (60%)**: `#0A0A0F` — near-black with subtle blue undertone. Used as page background.
- **Secondary (30%)**: `#E2E8F0` — cool off-white. Used for all text and structural elements.
- **Accent (10%)**: `#6366F1` — indigo. Used exclusively for CTAs, highlights, view counts, and numbers.

## Funnel Type
- **Type**: DM funnel
- **CTA text**: DM Me
- **CTA link**: https://x.com/sashank_mohan

## Structure Choices
- **Navigation**: Nav bar (sticky, blurred backdrop)
- **Hero video**: Showreel — URL placeholder (to be added)
- **Case study style**: Minimal (no video titles — thumbnail, client name, view count only)
- **Social proof strip**: Scrolling carousel (auto-scrolling, pauses on hover)
- **About Me section**: None
- **Retention/Analytics section**: None

## Videos
| # | Type | Client | YouTube URL | View Count |
|---|------|--------|-------------|------------|
| 1 | Long Form | TBD | TBD | — |
| 2 | Long Form | TBD | TBD | — |
| 3 | Long Form | TBD | TBD | — |
| 4 | Short Form | TBD | TBD | 30M |
| 5 | Short Form | TBD | TBD | 18M |
| 6 | Short Form | TBD | TBD | 4.3M |
| 7 | Short Form | TBD | TBD | 86K |
| 8 | Short Form | TBD | TBD | — |

**To add a video:** In the HTML, find the matching card and replace the `<div class="thumb-ph">` placeholder block with:
```html
<iframe
  src="https://www.youtube.com/embed/VIDEO_ID?rel=0&modestbranding=1"
  loading="lazy" allowfullscreen title="Video"
></iframe>
```
Then update `v-client` (client name) and `v-views` (view count) in the `v-meta` div below it.

**To add the showreel:** In the hero section, replace the `<div class="reel-ph">` block with:
```html
<iframe
  src="https://www.youtube.com/embed/YOUR_VIDEO_ID?autoplay=1&mute=1&rel=0&modestbranding=1"
  loading="lazy" allowfullscreen allow="autoplay; encrypted-media"
></iframe>
```

## Testimonials
| Client | Quote | Date |
|--------|-------|------|
| Brett Ottolenghi | "I will be hiring Mohan for many more videos. He has done a great job editing my videos to my specifications. He sticks with the project until it is finished. Always communicates quickly." | January 2022 |
| Timothy Sykes | "Great job, pleasure to work with!" | Verified client |
| Andrew | "Excellent job. Great communication. A pleasure to work with." | July 2021 |

## Numerical Results
- 30M views — single short-form video
- 18M views — single short-form video
- 4.3M views — single short-form video
- 86K views — single video

## Social Proof Strip Creators
| Creator | Handle | Subscribers |
|---------|--------|-------------|
| Insane Curiosity | @InsaneCuriosity | 634K |
| Timothy Sykes | @TimothySykesTrader | 477K |
| Ayehxncho Vault | @ayehxncho_vault | 72.2K |
| The Sauna Heater | @thesaunaheater | 21.8K |
| Next Curiosity (Brett Ottolenghi) | @NextCuriosity | 1.09K |

## Social Links
- X (Twitter): https://x.com/sashank_mohan (also the CTA link)

## Assets
No image assets currently — all creator avatars use CSS-generated initials. Replace with actual images when available by adding an `<img>` tag inside the `.c-av` div for each creator in the carousel.

---

## Design Rules (Do Not Break)

1. **60/30/10**: Only use `#0A0A0F`, `#E2E8F0`, and `#6366F1`. No new colours introduced.
2. **Hierarchy**: Every video card follows Hook (thumbnail) → Client name → View count.
3. **Above-the-Fold CTA**: The "DM Me" button must always be visible without scrolling. The hero CTA is above the showreel.
4. **CTA Repetition**: "DM Me" appears in the nav, hero, after long-form, after short-form, after testimonials, and in the footer. Same text and link every time.
5. **Hick's Law**: 8 videos total (3 long form + 5 short form). If adding a new video, remove the weakest to stay at 8.
6. **Social Proof Priority**: Work first, testimonials second, numbers as bonus. No placeholder sections.
7. **Anti-Cloning**: Maintain this editor's unique layout. Do not restructure to match other portfolios.
8. **Trust over hype**: Keep copy minimal and grounded. No exaggeration.
9. **Single HTML file**: One file, inline CSS and JS. Keep it that way.
10. **Responsive**: All edits must look good on mobile and desktop.

## Common Edit Patterns

- **"Add a video URL"**: Find the matching card in the HTML. Replace the `<div class="thumb-ph">` with an `<iframe>` embed. Update `v-client` and `v-views` text. Update the Videos table above.
- **"Add the showreel"**: Find the `<div class="reel-ph">` in the hero section. Replace with an `<iframe>` autoplay embed. See embed code in the Videos section above.
- **"Add a testimonial"**: Add a new `.t-card` block in the testimonials section. Keep to 3 testimonials ideally — if adding a 4th, switch the grid to `repeat(2,1fr)` for better layout.
- **"Change CTA text or link"**: Update ALL instances (nav, hero, after long-form, after short-form, after testimonials, footer). There are 6 total. Update the Funnel Type section above.
- **"Change colours"**: Update the CSS `:root` variables at the top of the `<style>` block. Check contrast ratios remain readable.
- **"Update view counts"**: Find the `v-views` span in the matching card and update the text. Update the Videos table above.
- **"Add creator to strip"**: Add a new `.c-chip` block in BOTH Set 1 and Set 2 of the carousel. Update the Social Proof Strip table above.

After any edit, update this CLAUDE.md to stay in sync with the live site.
