---
name: beautiful-architecture-diagram
description: Create semantically correct, visually polished architecture-diagram images from system descriptions, technical documents, component lists, or visual references. Use for system context, layered, component, data-flow, event-driven, hub-and-spoke, deployment, trust-zone, ecosystem, and feedback-loop diagrams; do not use for PPT design, editable Mermaid/SVG output, or generic illustration requests.
---

# Beautiful Architecture Diagram

Turn technical material into one independent architecture-diagram image. Preserve the system's actual boundaries and relationships; visual polish is secondary to semantic clarity.

## Choose the Output Path

- Default: directly generate the architecture-diagram image with an available image-generation tool.
- For the best result, run this skill in Codex with image generation enabled and prefer GPT Image 2 (`gpt-image-2`) when that model is available.
- Do not require one hard-coded tool name. Use the host agent's available image-generation capability while preserving this skill's topology and prompt rules.
- If the user asks only for a prompt, return the diagram strategy and a complete generation prompt without generating.
- If image generation is unavailable, return the complete handoff prompt and state the limitation briefly. Do not substitute an SVG, Mermaid, Graphviz, or code-rendering workflow.
- Editable Mermaid, Graphviz, SVG, and `.pptx` outputs are outside this skill's scope.

## Resolve the Visual Style

- If the user names a built-in style, use it.
- If the user provides a style reference, treat it as a custom visual system while selecting the diagram topology independently.
- If no style is specified, read [references/style-library.md](references/style-library.md), recommend exactly three meaningfully different styles with one-sentence rationales, and wait for selection.
- If the user says “自动选择”, “直接生成”, or otherwise asks to skip discussion, choose the best style and continue without pausing.

## Build the Diagram

1. Identify the diagram's purpose, audience, scope, and intended takeaway.
2. Extract only supported facts: external actors, boundaries, components, services, data stores, queues, interfaces, protocols, trust zones, and observable relationships.
3. Classify every relevant relationship as request/response, data flow, control, dependency, deployment, event, feedback, or containment. Never invent missing infrastructure or guarantees.
4. Choose an abstraction level that stays legible. Prefer an overview architecture over unreadable detail and disclose any material grouping.
5. Read [references/diagram-topologies.md](references/diagram-topologies.md). Consider multiple plausible topologies and choose the one that best preserves the relationship semantics, scope, and reading path.
6. Select the canvas from the topology: wide landscape for flows and platform overviews, balanced 4:3 or square for component maps, and portrait only for genuinely vertical structures.
7. Read [references/prompt-compiler.md](references/prompt-compiler.md), compile exact image instructions, and generate or return the prompt according to the requested output path.
8. Consult [references/worked-examples.md](references/worked-examples.md) only when topology choice or abstraction is ambiguous.

Ask one focused question only when a missing detail would materially change the topology. Otherwise use a neutral label and disclose the assumption.

## Handle Visual References

Extract palette, typography character, node treatment, border and shadow language, icon style, line and arrow treatment, spacing, density, and atmosphere. Unless the user explicitly requests structural replication, do not copy the reference's topology, node positions, component count, or labels.

Learn the visual grammar; reconstruct the system architecture.

## Preserve These Invariants

- Generate one independent architecture diagram, not a slide, deck, editor interface, device mockup, or presentation preview.
- Preserve user-provided names, facts, required relationships, and boundary semantics exactly.
- Arrows encode direction, dependency, or flow. Lines encode relationships. Containers encode scope, ownership, deployment, or trust. Loops encode real feedback.
- Include a legend only when line types, colors, or zones carry distinct meanings.
- Avoid dense microtext, long prose, crossing connectors, undifferentiated card grids, meaningless arrows, generic stock icons, watermarks, and unrequested logos.
- Keep the title or system label visible, the entry point clear, component text readable, and whitespace intentional.
- Style must never obscure or contradict the architecture.

## Deliver

For direct generation, return the image. Add a short note only when an assumption, abstraction choice, or omitted detail needs disclosure.

For prompt-only mode, return exactly:

```text
Diagram Strategy
<topology, abstraction level, selected style, and concise rationale>

Generation Prompt
<complete model-ready prompt>
```

Before delivering, verify the component inventory, boundaries, relationship types, directionality, topology choice, label legibility, and absence of unsupported details.
