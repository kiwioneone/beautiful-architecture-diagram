# Image-Generation Prompt Compiler

Use case: `infographic-diagram`. Compile the prompt in this order. Replace every slot with concrete instructions and omit empty fields.

## Asset and Purpose

- Asset type: standalone architecture-diagram image.
- Audience: state the known audience.
- Diagram purpose: state what the viewer must understand.
- Abstraction level: context, overview, subsystem, or deployment detail.

## Canvas

Choose the aspect ratio from the topology. Require one independent diagram with no slide chrome, editor interface, deck preview, device, or room mockup. Define safe margins and the intended reading direction.

## Exact Text

List the title and every visible component, boundary, and legend label verbatim. Use concise labels. Require correct spelling, no extra copy, no lorem ipsum, and no invented product names.

## Component Inventory

Describe each actor, component, store, queue, interface, and boundary. State which nodes belong inside which containers. Identify the visual center and relative importance without inventing implementation detail.

## Relationship Semantics

For each important link, specify source, destination, direction, and meaning. Identify request/response, data, control, dependency, deployment, event, feedback, and containment separately. If line color or shape carries meaning, require a compact legend.

## Topology and Composition

Name the selected topology. Describe node placement by semantic group, the primary reading path, container nesting, connector routing, and how overlaps are avoided. Use a single dominant topology, not several mini-diagrams.

## Visual System

Specify the selected built-in or custom style concretely:

- background and palette;
- typography hierarchy;
- node shape, border, corner, fill, and shadow treatment;
- arrow and connector treatment;
- icon policy;
- spacing, density, and allowable decoration.

## Rendering Standard

Require polished vector-like infographic quality, crisp alignment, clean connector routing, legible text, consistent component grammar, restrained decoration, and strong contrast. The output should be suitable for technical documentation and a GitHub README.

## Negative Constraints

Always include equivalents of:

- no slide, deck, presentation mockup, editor interface, device screen, or second diagram;
- no invented components, protocols, metrics, flows, security claims, logos, or labels;
- no meaningless arrows, decorative links, crossed connectors, floating ungrouped nodes, or misleading containment;
- no long prose, dense microtext, gibberish, watermarks, stock photography, people, or generic clip art;
- no style effects that reduce label legibility or obscure boundaries.

## Prompt-Only Response

```text
Diagram Strategy
<selected topology, abstraction, aspect ratio, visual style, and concise rationale>

Generation Prompt
<one coherent model-ready prompt containing the sections above>
```
