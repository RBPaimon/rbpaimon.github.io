# DESIGN.md — rbpaimon.github.io

This file is the **single source of truth** for the visual design of the
documentation site. Per the project's `AGENTS.md`, every design decision MUST be
recorded here. Do not introduce a design choice that is not described in this
file; if a new decision is needed, add it here first, then build the site to
match. This exists so the design never drifts from the established parameters.

## Theme: White · Silver · Transparent

The site uses a restrained palette of **white**, **silver / grey**, and
**transparent (frosted glass)** surfaces. No other accent hues are permitted.

### Color tokens

| Token | Value | Use |
| --- | --- | --- |
| `--white` | `#ffffff` | Page base and primary surfaces |
| `--silver-100` | `#f4f5f7` | Subtle raised fills |
| `--silver-200` | `#e6e8ec` | Hairline borders and dividers |
| `--silver-400` | `#b8bcc4` | Secondary borders, muted icons |
| `--silver-600` | `#8a8f99` | Secondary text |
| `--ink` | `#2a2d33` | Primary text (soft charcoal, never pure black) |
| `--glass` | `rgba(255, 255, 255, 0.55)` | Frosted panel fill |
| `--glass-border` | `rgba(255, 255, 255, 0.70)` | Frosted panel edge highlight |
| `--glass-shadow` | `rgba(138, 143, 153, 0.18)` | Soft silver shadow |

### Material: frosted glass

- Panels and cards use a translucent fill (`--glass`) plus
  `backdrop-filter: blur(…)` so they read as transparent glass over the page.
- Edges use a 1px light border (`--glass-border`) and a soft silver shadow.
- Never use opaque, saturated color blocks. Transparency and silver lines define
  structure — not fills.

### Typography

- System UI / `Inter`-style sans-serif stack.
- Body text in `--ink`; secondary text in `--silver-600`.
- Line-height ~1.6; comfortable measure (max ~70ch).

### Layout & spacing

- 8px spacing scale: 8 / 16 / 24 / 32 / 48 / 64.
- Rounded corners: 16px on panels, 999px on pills.
- Centered single column, max content width ~960px.

### Components

- **Glass card** — frosted fill, silver border, soft shadow; wraps each concept.
- **Step badge** — silver pill carrying the step number over a transparent field.
- **Divider** — 1px `--silver-200` hairline.

### Rules

- Backgrounds stay white or transparent; accents are silver only.
- Maintain WCAG AA contrast: body text uses `--ink` on white.
- Respect `prefers-reduced-motion`; keep all motion subtle.
