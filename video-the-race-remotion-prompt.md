# THE RACE: Remotion Build Prompt

Copy this entire file into Claude Code as the prompt.

---

## What to build

A 30-second video using Remotion (React-based programmatic video). The video is called "THE RACE." It tells the story of two companies launching the same data product: one builds scraping infrastructure from scratch, the other uses a managed API. Split-screen format. The left side descends into chaos. The right side stays calm. The contrast does the selling.

## Tech specs

- Remotion 4.x, React 18, TypeScript
- 30fps, 30 seconds = 900 frames
- 1920x1080 (16:9)
- Register three compositions in Root.tsx:
  - `TheRace` (1920x1080, 900 frames) - main video
  - `TheRaceVertical` (1080x1920, 900 frames) - vertical cut, stacked instead of side-by-side
  - `TheRaceLinkedIn` (1920x1080, 450 frames) - 15-second cut using only shots 5-8

## Design system

Colors:
- Background: `#091B36`
- Left side accent (danger/fail): `#FF4444`
- Right side accent (Bright Data blue): `#3D7FFC`
- Success green: `#22C55E`
- Text primary: `#FFFFFF`
- Text secondary: `#94A3B8`
- Subtle borders/backgrounds: use the accent colors at 10-20% opacity

Typography:
- Headlines/labels: Inter (bold/black weight), geometric sans fallback. All caps for labels, letter-spacing 2-4px.
- Code/data: JetBrains Mono or Fira Code, monospace fallback
- Numbers: Large (48-72px), tight letter-spacing (-2px), heavy weight

Visual style: Clean, dark, tech-corporate. Think Stripe or Linear product videos. No 3D. No illustrations of people. Everything is abstract: terminals, dashboards, code blocks, charts, notification badges, progress bars, world map dot grids. The left side uses red tints. The right side uses blue tints.

## Architecture

Use `<Sequence>` components for each shot. Use `interpolate()` for linear animations and `spring()` for snappy entrances. Keep each scene as its own component. Extract shared UI (terminal blocks, counters, slack messages, badges, gauges) into a components file.

Use `useCurrentFrame()` within each scene to drive local animation progress (0-1 normalized where possible).

## Shot-by-shot specification

All timings in frames at 30fps.

### Shot 1: OPENING (frames 0-29, 1 second)
Black screen. Text fades in centered: "Same market. Same idea." White, 56px, Inter Black. Fade in over 15 frames using `interpolate(frame, [0, 15], [0, 1])`. Hold.

### Shot 2: SPLIT REVEAL (frames 30-59, 1 second)
Hard vertical divider line (2px, `#94A3B844`) animates from center outward. Left half gets subtle red background tint (`#FF444408`). Right half gets subtle blue tint (`#3D7FFC08`).

Labels appear with a `spring()` animation:
- Left: "BUILD IT YOURSELF" in `#FF4444`, 18px, letter-spacing 4px, centered at top of left half
- Right: "ONE API CALL" in `#3D7FFC`, same style, centered at top of right half

### Shot 3: WEEK 1 (frames 60-119, 2 seconds)

**Left side:** A terminal window (dark background, colored dots top-left). Code lines type in progressively, simulating a Scrapy project setup:
```
$ scrapy startproject data_pipeline
$ vim scrapy.cfg
$ kubectl apply -f proxy-cluster.yaml
  configuring 12 proxy nodes...
  setting up IP rotation...
  deploying anti-detect middleware...
  ERROR: connection pool exhausted
```
Use a typing effect: reveal characters one by one based on frame progress. Include a blinking cursor. Clock overlay bottom-right: "WEEK 1" in red, monospace, small border.

**Right side:** A clean, minimal code editor showing 3 lines:
```
const res = await fetch('api.brightdata.com/v1/scrape', {
  method: 'POST', body: JSON.stringify({ url, format: 'json' })
});
```
At ~frame 80, a JSON response block appears below with a green left border, showing clean structured data. Smooth fade-in. Clock overlay: "DAY 1" in blue.

### Shot 4: WEEK 4 (frames 120-179, 2 seconds)

**Left side:** The terminal is now overwhelmed. More scrolling lines, faster:
```
deploy-proxy-v3.yaml
docker-compose.override.yml
.env.scraper.staging
rotate-ips.sh
```
Below the terminal, show a simplified Jira/task board graphic: a row of small rectangles, most red/yellow, with a counter "47 open tickets" in red. Clock: "WEEK 4".

**Right side:** A simple line chart climbing from bottom-left to upper-right (draw using SVG path with `strokeDashoffset` animation). Below it: "12 paying customers" in blue, 24px. Below that, a small code block labeled "Building: AI enrichment pipeline" in green text, suggesting the team is working on product, not infra. Clock: "WEEK 4" in blue.

### Shot 5: THE BREAK (frames 180-269, 3 seconds)

This is the emotional peak of the left side. Maximum contrast.

**Left side:** Background shifts to deeper red tint (`#FF444415`). Large "403 FORBIDDEN" text flashes in (spring animation, 64px, red, centered). Below it, Slack-style messages stack in rapidly, one every ~10 frames, sliding in from the right:
1. "scraper down across all feeds" (urgent styling: red left border, red text)
2. "LinkedIn returning 429 on every request"
3. "Cloudflare updated challenge page"
4. "CEO asking for status update"
5. "ALL PIPELINES HALTED"

Each message has a left border (3px red), dark background, and slides in with a spring animation. Stack them vertically, newest at bottom.

**Right side:** Deliberately calm. A simple dashboard mockup: a flat green horizontal line labeled "99.7% UPTIME" in green. Below: a counter "30 customers" in blue. A subtle revenue ticker that smoothly increments. Everything static and peaceful. The contrast with the left side is the entire point.

### Shot 6: THE BLEED (frames 270-359, 3 seconds)

**Left side:** Two large counters, stacked:
- "$218K" in red, 56px, with label "SPENT" below in gray
- "$0" in red, 56px, with label "REVENUE" below in gray

Below them, a scrolling list of IP addresses being banned (monospace, red, small text, scrolling upward continuously). Text like:
```
BANNED 192.168.x.x (LinkedIn)
BANNED 10.0.x.x (Amazon)
BLOCKED proxy-node-7 (Cloudflare)
```

**Right side:** Two large counters, stacked:
- "$180K" in blue, 56px, with label "REVENUE" below
- "50" in blue, 56px, with label "CUSTOMERS" below

Below them, a simple wireframe sketch mockup (just rectangles suggesting a UI), with a label "Shipping: v2.3 feature release" in green. The right side is building product. The left is still fighting fires.

### Shot 7: THE GAP (frames 360-449, 3 seconds)

**Left side:**
- Text "3 ENGINEERS" in red, 36px, bold
- Below: "FULL-TIME MAINTENANCE" in gray, 18px, uppercase
- Cost counter: "$618K/yr" in red, 48px
- An uptime gauge/progress bar at 85%, color red, wobbling slightly (use a sine wave on the width: `85 + Math.sin(frame * 0.3) * 2`%)
- Small notification badges accumulating in corner: "12 complaints" with red badge

**Right side:**
- Text "3 ENGINEERS" in blue, 36px, bold
- Below: "SHIPPING PRODUCT" in green, 18px, uppercase
- Cost counter: "$12K/yr" in blue, 48px
- Uptime gauge at 99.99%, solid green, perfectly flat
- Generic enterprise silhouette logos fading in (use simple rounded rectangles in blue at 20% opacity as placeholder company logos, 6-8 of them in a grid)

### Shot 8: COMPARISON TABLE (frames 450-539, 3 seconds)

Split screen collapses: both sides slide toward center and fade out. Background returns to solid `#091B36`.

A comparison table animates in, one row at a time. Each row enters with a `spring()` from below, 15 frames apart:

| Metric | Build (red, left-aligned) | API (blue, right-aligned) |
|---|---|---|
| TIME TO MARKET | 6 months | 2 weeks |
| ANNUAL COST | $618K | $12K |
| UPTIME | 85% | 99.99% |
| ENGINEERS ON INFRA | 3 | 0 |

Layout: Three columns. Center column is the metric label (gray, uppercase, 14px, letter-spacing 2px). Left column is red values (28px, bold). Right column is blue values (28px, bold). Each row has a subtle bottom border (`#94A3B822`). The table is centered on screen.

Frame timing:
- Row 1 enters at frame 460
- Row 2 at frame 475
- Row 3 at frame 490
- Row 4 at frame 505
- All visible together from 520-539

### Shot 9-10: KILL SHOT (frames 540-659, 4 seconds)

Black screen. Two lines of text, typed out sequentially.

Line 1 (frames 540-600): "The question isn't whether to build a data product."
- White, 42px, Inter Bold, centered
- Typing effect: one character every 1-2 frames
- Include a blinking cursor at the end

Pause (frames 600-615): cursor blinks. Silence.

Line 2 (frames 615-659): "It's where you burn your engineering hours."
- Same style, appears below line 1
- Typing effect, same speed
- "burn" in `#FF4444` (red), rest in white. This is the only colored word.

### Shot 11: MONTAGE (frames 660-779, 4 seconds)

Fast cuts, each stat gets exactly 30 frames (1 second). Full black background between each. Each stat enters with a hard cut (no transition).

**Cut 1 (660-689): "400M+ residential IPs"**
World map made of dots. Use a grid of small circles (4px) placed roughly in continent shapes. Dots light up progressively from left to right (blue glow + full opacity vs dim gray). The text "400M+" appears large (64px, blue, bold) at center-bottom.

**Cut 2 (690-719): "195 countries"**
Same world map, all dots fully lit in blue with glow (`box-shadow: 0 0 8px #3D7FFC`). Text: "195 COUNTRIES" in white, 48px, centered.

**Cut 3 (720-749): "99.7% success rate"**
Large "99.7%" in green, 80px, centered. Below: "success rate on the hardest sites" in gray, 18px. Green checkmark icons (simple SVG) cascade in from top, 5-6 of them, staggered with spring animations.

**Cut 4 (750-779): Certifications**
Five certification badges in a horizontal row, each appearing with a spring scale animation staggered by 5 frames:
- SOC 2
- ISO 27001
- GDPR
- CCPA
- CSA STAR

Each badge: border 2px `#22C55E`, rounded corners, padding, green text, uppercase, dark background. Center the row.

### Shot 12: CTA (frames 780-899, 4 seconds)

Clean frame. Centered vertically:

1. Bright Data logo: just render as text "bright data" in white, 28px, bold, with a small blue square (12x12) to the left as a simplified logo mark. Use `spring()` to scale from 0 to 1.

2. Below (fade in at frame 810): "The collection layer for data products." in `#94A3B8`, 20px.

3. Below (fade in at frame 840): "brightdata.com/data-products" in white, 24px, bold.

Hold. At frame 870, everything fades to black over 30 frames using `interpolate(frame, [870, 899], [1, 0])`.

## Additional implementation notes

- Every animation should use `spring({ fps: 30, config: { damping: 15 } })` for entrances unless the brief says "fade" (then use linear `interpolate`).
- For typing effects, calculate chars visible as `Math.floor(interpolate(frame, [startFrame, endFrame], [0, text.length]))`. Show a blinking cursor: `opacity: Math.sin(frame * 0.5) > 0 ? 1 : 0`.
- For the scrolling IP ban list (shot 6), use `translateY` animated over frames to create continuous upward scroll.
- For the growth chart SVG (shot 4), use a path element with `strokeDasharray` equal to total length and `strokeDashoffset` interpolated from full length to 0.
- The world map dots: generate deterministic positions using a seeded pseudo-random function (e.g., `((i * 9301 + 49297) % 233280) / 233280`). Place ~120 dots in rough continent shapes by defining bounding boxes for NA, SA, Europe, Africa, Asia, Oceania and generating random points within each.
- Keep all component files in `src/`. No deep nesting. A flat `components.tsx` for shared UI, individual scene files or a single `scenes.tsx` file, and `Root.tsx` for composition registration.
- Use `@remotion/cli` for rendering. Add scripts to package.json: `"start": "remotion studio"`, `"build": "remotion render TheRace out/the-race.mp4"`.
- No external assets required. Everything is rendered in React/CSS/SVG.
- Google Fonts: import Inter and JetBrains Mono via `@remotion/google-fonts` or load from Google Fonts CDN in a `<style>` tag.
