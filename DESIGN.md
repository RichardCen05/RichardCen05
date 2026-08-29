---
name: Richard Cen GitHub Profile
description: A recruiter-facing AI product evidence trail rendered as a calm product signal console.
colors:
  shadow-ink: "#020B08"
  forest-canvas: "#071F17"
  forest-raised: "#0A2A1E"
  pine: "#0E3B2A"
  learning-pine: "#123F2D"
  grid-line: "#174C37"
  orbit-line: "#1B6949"
  card-border: "#1F5A41"
  status-border: "#236447"
  route-muted: "#2B805C"
  emerald-signal: "#35D07F"
  text-muted: "#78A991"
  text-operational: "#78CFA2"
  text-loop-label: "#9CCBB4"
  mint-signal: "#A7F3D0"
  text-secondary: "#B4D8C5"
  text-primary-soft: "#C9E8D8"
  status-text: "#CFFBE3"
  off-white: "#F3FFF8"
  linkedin-badge: "#166534"
typography:
  interface-sans:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
  operational-mono:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
rounded:
  evidence-desktop: "16px"
  status-pill: "17px"
  loop-desktop: "20px"
  evidence-mobile: "20px"
  hero-desktop: "24px"
  hero-mobile: "28px"
  loop-mobile: "28px"
components:
  hero-desktop:
    backgroundColor: "{colors.forest-canvas}"
    textColor: "{colors.off-white}"
    rounded: "{rounded.hero-desktop}"
    width: "1200px"
    height: "420px"
  hero-mobile:
    backgroundColor: "{colors.forest-canvas}"
    textColor: "{colors.off-white}"
    rounded: "{rounded.hero-mobile}"
    width: "720px"
    height: "620px"
  product-loop-desktop:
    backgroundColor: "{colors.forest-canvas}"
    textColor: "{colors.off-white}"
    rounded: "{rounded.loop-desktop}"
    width: "1200px"
    height: "230px"
  product-loop-mobile:
    backgroundColor: "{colors.forest-canvas}"
    textColor: "{colors.off-white}"
    rounded: "{rounded.loop-mobile}"
    width: "720px"
    height: "720px"
---

# Design System: Richard Cen GitHub Profile

## Overview

**Creative North Star: "The Product Signal Console"**

The profile is an evidence trail from messy user workflow to measurable AI pilot. Deep forest surfaces, mint signals, thin operational linework, and compact data labels make it feel like a calm AI product operating system rather than a badge-first developer profile.

**Design thesis.** Lead with Richard's positioning and verifiable outcomes, then explain the product decisions behind them. Motion clarifies the discovery-to-pilot process; it is not ambient decoration.

### Information hierarchy

1. Responsive hero: name, AI Product Manager position, availability, one pilot result, and the discovery-to-pilot route.
2. LinkedIn and email actions, followed by a short first-person positioning statement.
3. Four quantified evidence points.
4. Three product briefs—Kulkita, Sentra, and Fiona—each organized as problem, product work, evidence, and what it proves.
5. Experience, the product operating loop, toolkit, selected recognition, GitHub activity, and a direct contact close.

## Colors

The palette is dark, low-glare forest green. Emerald and mint are signals, not general-purpose fill colors; warm off-white carries the strongest text.

| Token | Usage |
| --- | --- |
| `forest-canvas`, `forest-raised`, `pine`, `learning-pine` | Asset canvas, raised evidence surface, decorative mass, node fills, and the terminal learning state. |
| `grid-line`, `orbit-line`, `card-border`, `status-border`, `route-muted` | Low-contrast grid, orbital geometry, boundaries, and inactive route segments. |
| `emerald-signal`, `mint-signal` | Role accent, active path, node outlines, status dot, arrowhead, and final-state emphasis. |
| `off-white`, `text-primary-soft`, `text-secondary` | Display copy, primary supporting copy, and secondary explanatory copy. |
| `text-operational`, `text-loop-label`, `text-muted`, `status-text` | Mono labels, route labels, metadata, and availability text. |
| `shadow-ink` | Desktop evidence-card drop shadow only. |
| `linkedin-badge` | LinkedIn shield background; the email shield uses `pine`. |

**The Signal Rarity Rule.** Keep bright emerald and mint concentrated on state, route, and evidence cues so they retain meaning.

## Typography

SVG assets use the native interface sans stack for names, headings, evidence, and prose; the operational mono stack is reserved for system labels, stage names, locations, and compact evidence metadata. The Markdown body inherits GitHub's native typography, and no web font is loaded.

The desktop hero uses a 66px/750 name, 27px/650 role, 20px positioning line, and 14–18px operational labels. The mobile hero increases key text for the 720px artboard: 68px/750 name, 38px/680 role, 30px positioning line, and 22–25px labels. Product-loop type ranges from 15–25px on desktop and 24–38px on mobile.

**The Two-Voice Rule.** Use sans type for the human narrative and mono type for product-system metadata; do not introduce a third typeface.

## Layout

The README is a single vertical GitHub document with centered visual assets and contact actions. Long-form evidence remains native Markdown for scanning, selection, search, and theme compatibility.

The `<picture>` elements switch at `(max-width: 1200px)`: viewports at or below 1200px receive the mobile SVGs; wider viewports receive the desktop SVGs. Desktop uses a 1200×420 horizontal hero and a 1200×230 horizontal five-stage loop. Mobile uses a 720×620 stacked hero and a 720×720 vertical loop. Both render at `width="100%"` within GitHub's content column.

Desktop hero composition is asymmetric: identity at left, evidence card at right, and a five-stop route across the lower third. Mobile stacks identity, one evidence card, and a simplified three-stop route. The loop preserves all five stages but changes from horizontal to vertical.

## Elevation & Depth

The system is flat by default and creates depth through tonal layering, thin outlines, clipped circles, and sparse geometry. Only the desktop hero evidence card uses a shadow: 0px horizontal offset, 8px vertical offset, 12px standard deviation, `shadow-ink` at 55% opacity. Mobile and both loop assets use no shadows.

## Shapes

Large SVG canvases use gently rounded clipping: 24px on the desktop hero, 28px on mobile assets, and 20px on the desktop loop. Evidence cards use 16px desktop and 20px mobile corners; the availability capsule uses a 17px radius. Nodes are circular, paths are round-capped, and borders remain thin (normally 1–2px desktop, 2–5px mobile for legibility).

## Components

- **Hero signal board:** responsive desktop/mobile SVG pair containing identity, availability, positioning, pilot evidence, and route visualization.
- **Evidence card:** raised tonal panel inside the hero; desktop carries two evidence lines, while mobile prioritizes the 35% pilot result.
- **Signal route:** five stages on desktop, three summary stages on mobile, with a single animated signal dot.
- **Product operating loop:** static five-stage desktop/mobile SVG pair; horizontal on desktop and vertical on mobile.
- **Contact actions:** externally rendered Shields.io badges for LinkedIn and email, plus a native-text contact close.
- **Evidence content blocks:** native Markdown sections, lists, bold metrics, and blockquotes; project briefs consistently end with “What it proves.”
- **GitHub activity:** externally rendered profile-details image linked to Richard's GitHub profile.

### External dependencies

The profile depends on GitHub Markdown/HTML rendering, repository-hosted SVG assets, Shields.io for contact badges, and `github-profile-summary-cards.vercel.app` for the activity image. LinkedIn and `mailto:` are the only contact destinations. There is no JavaScript, CSS bundle, web-font service, or private project asset.

### Motion

Only the hero signal dot moves. It travels once for 4 seconds, freezes at the end, and uses spline easing (`0.22 1 0.36 1`); it never loops. Under `prefers-reduced-motion: reduce`, the moving dot is hidden. The route, labels, and all core meaning remain visible, and the product-loop assets stay static.

## Do's and Don'ts

### Do

- **Do** keep every claim attributable to supplied evidence; distinguish user-reported pilot results from internal evaluations and public awards.
- **Do** preserve SVG `<title>`, `<desc>`, `role="img"`, and README `alt` text. Keep the same meaning available in surrounding Markdown.
- **Do** verify SVG XML, both responsive renderings, external URLs, GitHub light/dark readability, and reduced-motion behavior after asset changes.
- **Do** update desktop and mobile asset pairs together and preserve the 1200px `<picture>` breakpoint unless intentionally revising the responsive system.
- **Do** keep Fiona's client details private and label n8n and Zapier as working knowledge.

### Don't

- **Don't** add phone numbers, private Fiona links, invented metrics, customers, integrations, or technical depth.
- **Don't** replace evidence with skill percentages, motivational quotes, long badge rows, or unqualified projections.
- **Don't** add looping, flashing, or meaning-critical animation.
- **Don't** introduce external fonts or runtime code; reliability inside GitHub is part of the design.
