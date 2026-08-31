# Built-in Style Library

Style is a presentation layer applied after topology selection. It may change color, typography, node treatment, spacing, and decoration, but never component meaning, containment, or link semantics.

## S01 — Editorial Tech

- Character: premium technical report, editorial grid, warm minimalism.
- Palette: warm ivory `#F3EFE6`, deep ink green `#153F3B`, muted orange `#EB7A2D`, warm gray `#D8D2C6`.
- Typography: condensed or tight grotesk title; modern sans-serif labels.
- Nodes: medium-radius cards, fine warm borders, soft natural shadows.
- Links: thin ink-green lines; orange only for a pivotal flow or node.
- Decoration: sparse crosshairs, guide lines, page index, engineering marks.
- Best for: technical strategy, AI systems, consulting reports, thoughtful open-source projects.

## S02 — Dark Blueprint

- Character: infrastructure blueprint, precise, technical, nocturnal.
- Palette: midnight navy `#071525`, deep panel blue `#0B2035`, cyan `#28D7FF`, cool white `#D7F4FF`.
- Typography: compact geometric sans serif; uppercase micro-labels.
- Nodes: dark panels with cyan hairline borders and faint inner glow.
- Links: cyan lines with clear arrowheads; optional typed-line legend.
- Decoration: low-contrast technical grid and coordinate marks.
- Best for: DevTools, cloud infrastructure, networking, runtime and deployment diagrams.

## S03 — Swiss Signal

- Character: strict international typographic style with strong editorial impact.
- Palette: off-white `#FAFAF7`, near-black `#101010`, signal red `#E02222`.
- Typography: bold grotesk headline, disciplined sans-serif labels, numeric indexing.
- Nodes: square corners, black structure, minimal fill.
- Links: black primary lines; red only for the critical path or state.
- Decoration: grid alignment, section rules, small numeric codes.
- Best for: strong GitHub hero examples, frameworks, standards, architecture principles.

## S04 — Product Minimal

- Character: refined SaaS product system, calm and approachable.
- Palette: white, silver gray `#F1F4F6`, graphite `#172029`, soft green `#45A58F`.
- Typography: modern product sans serif with generous spacing.
- Nodes: light cards, subtle borders, natural elevation, moderate radius.
- Links: graphite or green hairlines with restrained arrows.
- Decoration: almost none; hierarchy comes from spacing and scale.
- Best for: product platforms, developer experience, business systems, documentation.

## S05 — Neo Brutalist

- Character: bold open-source energy, direct, playful, deliberately structural.
- Palette: warm cream `#F3F0E7`, black `#111111`, electric yellow `#FFE600`, coral `#FF5C35`, mint `#88E0D0`.
- Typography: heavy condensed sans serif and monospace micro-labels.
- Nodes: square corners, two-pixel black borders, crisp offset shadows.
- Links: heavy black lines; color identifies only real categories.
- Decoration: large numeric markers and simple geometric blocks.
- Best for: creative developer tools, experimental frameworks, memorable repository showcases.

## S06 — Executive Dark

- Character: premium leadership brief, quiet confidence, restrained luxury.
- Palette: charcoal `#151716`, graphite `#242724`, champagne `#CBA86D`, parchment `#F4E9D3`.
- Typography: refined serif or high-contrast title paired with clean sans-serif labels.
- Nodes: dark panels, fine gold-tinted borders, controlled deep shadows.
- Links: thin champagne lines with minimal arrowheads.
- Decoration: sparse rules and subtle radial lighting; no ornamental clutter.
- Best for: leadership, investment, governance, enterprise strategy, high-end launches.

## S07 — Soft Data Canvas

- Character: friendly data product, light, modern, explanatory.
- Palette: mist white `#FBFAFF`, soft violet `#7B6DE6`, pale blue `#EEF8FF`, apricot `#FFF3EC`, deep slate `#252B45`.
- Typography: rounded or neutral product sans serif.
- Nodes: light cards with soft category tints and low-contrast borders.
- Links: violet/slate lines with clean directional arrows.
- Decoration: a few blurred color fields behind the diagram, never behind labels.
- Best for: analytics, SaaS, education, approachable AI products, data workflows.

## Recommendation Rules

Choose three styles that differ materially. Base the recommendation on:

- audience: engineers, product users, executives, researchers, or a broad GitHub audience;
- subject: infrastructure, application system, security, data, governance, or experimental tooling;
- density: dense diagrams favor precise restrained systems; sparse diagrams can carry stronger personality;
- display background and intended use;
- supplied brand or reference constraints.

Useful defaults:

- Infrastructure or network: Dark Blueprint, Editorial Tech, Product Minimal.
- Executive or governance: Executive Dark, Editorial Tech, Swiss Signal.
- Open-source launch: Swiss Signal, Neo Brutalist, Dark Blueprint.
- Product or data platform: Product Minimal, Soft Data Canvas, Editorial Tech.
- When uncertain: Editorial Tech, Dark Blueprint, Product Minimal.

Never recommend three light editorial styles or three dark technical styles together. Explain each option in one sentence and wait unless the user asked for automatic selection.
