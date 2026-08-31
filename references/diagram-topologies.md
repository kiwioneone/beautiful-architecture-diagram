# Diagram Topology Library

Choose topology from system semantics, not from visual novelty or a style reference. Consider more than one plausible topology before selecting.

## Selection Signals

- Who uses or integrates with the system? → System Context.
- What sits above or depends on what? → Layered Architecture.
- What owns or contains each subsystem? → Container / Component Map.
- What transforms or moves from source to destination? → Data Flow / Pipeline.
- What publishes, brokers, and consumes asynchronous events? → Event-Driven Architecture.
- What coordinates many peripheral capabilities? → Hub-and-Spoke.
- Where does each service run? → Deployment / Runtime.
- Which boundaries change trust or access? → Network / Trust Zones.
- Which independent actors exchange typed information? → Ecosystem / Multi-Agent Map.
- What repeatedly measures and changes the system? → Feedback Loop.

## T01 — System Context

Use for the system boundary, its users, external services, and high-level integrations. Put the system in one clear boundary and keep external actors outside. Label interaction intent or protocol only when known. Do not expose internal implementation detail that belongs in a component map.

## T02 — Layered Architecture

Use when vertical order represents abstraction, dependency, or foundation-to-application progression. Name what the ordering means. Group components within their true layer and show only cross-layer dependencies that affect understanding. Do not use layers for items that are merely chronological.

## T03 — Container / Component Map

Use for the internal structure of a bounded system. Containers show ownership or responsibility; component links show supported calls or data exchange. Keep one abstraction level per diagram. Do not mix cloud deployment nodes with logical components unless deployment is part of the message.

## T04 — Data Flow / Pipeline

Use for ordered ingestion, transformation, storage, analysis, and delivery. Place sources and destinations clearly and label significant transformations. Distinguish data movement from control signals when both appear. Do not imply a strict sequence where processing is actually asynchronous or parallel.

## T05 — Event-Driven Architecture

Use for producers, topics or queues, brokers, consumers, retries, and dead-letter paths. Separate publish from consume direction and label asynchronous channels. Show fan-out only where the source supports it. Do not turn the event bus into a decorative center node.

## T06 — Hub-and-Spoke

Use when a control plane, orchestrator, platform, or gateway coordinates several capabilities. Put the hub at the visual center and organize spokes by function or importance. Label the exchange type when relevant. Avoid a spider web: peripheral nodes connect to each other only when the source requires it.

## T07 — Deployment / Runtime

Use for mapping services to regions, clusters, nodes, runtimes, or devices. Nest logical services inside their actual compute or network boundaries. Separate runtime placement from logical dependency with distinct line semantics. Do not invent replicas, zones, or failover behavior.

## T08 — Network / Trust Zones

Use for ingress, egress, identity, policy enforcement, public/private networks, and sensitive data boundaries. Make trust transitions visually explicit and label allowed flow direction. Security claims must come from the source. Do not imply protection merely by drawing a colored container.

## T09 — Ecosystem / Multi-Agent Map

Use for several autonomous actors, agents, platforms, or organizations exchanging requests, data, control, or feedback. Group actors into semantic clusters, type the important links, and preserve clear ownership. Remove redundant edges before rendering.

## T10 — Feedback Loop

Use for iterative evaluation, learning, optimization, or operational control. Name the measured signal, decision, action, and returned observation. The closing arrow must represent a real causal feedback path, not a visual flourish.

## Mixed Architectures

Use one dominant topology and a small secondary pattern when necessary—for example, a layered system with one event bus. Do not combine multiple complete diagrams on the same canvas. If two abstraction levels are both essential, propose an overview first rather than compressing both into unreadable detail.
