# Worked Topology Examples

Use these examples to reason about topology and abstraction. Do not copy their system facts into unrelated diagrams.

## System Context — SaaS Analytics Platform

**Input:** A web application used by analysts, integrated with an identity provider, payment service, warehouse, and notification service.

**Diagnosis:** The user wants the system's external environment, not internal services.

**Candidates:** System Context, Container Map, Ecosystem Map.

**Selection:** System Context. Put Analysts and Admins plus the four external systems outside one Analytics Platform boundary. Label only verified interaction intent. Internal microservices are omitted because they would mix abstraction levels.

## Layered Architecture — AI Application Stack

**Input:** Applications depend on orchestration, which depends on models and retrieval, which depend on data and compute.

**Diagnosis:** The primary relation is abstraction and dependency from application to foundation.

**Candidates:** Layered Architecture, Pipeline, Container Map.

**Selection:** Layered Architecture. Horizontal layers preserve dependency semantics. A pipeline would incorrectly imply that requests execute once through every layer in a fixed order.

## Event-Driven — Order Processing

**Input:** Checkout publishes an order event; inventory, payment, fulfillment, and notifications consume related events through a broker, with retry and dead-letter handling.

**Diagnosis:** Asynchronous publish/consume behavior and fan-out are central.

**Candidates:** Event-Driven Architecture, Data Flow, Hub-and-Spoke.

**Selection:** Event-Driven Architecture. Producers, broker/topics, consumers, retry path, and dead-letter queue get distinct semantics. The broker is infrastructure, not an orchestrating business brain.

## Deployment — Multi-Region API

**Input:** A global load balancer routes to regional Kubernetes clusters containing API and worker services; both access a managed database with region-specific replicas.

**Diagnosis:** Runtime placement, region boundaries, and deployed services are the message.

**Candidates:** Deployment / Runtime, Container Map, Network / Trust Zones.

**Selection:** Deployment / Runtime. Nest services in clusters and clusters in regions. Use separate link treatment for request traffic and replication only if the source confirms both. Do not invent availability zones or failover rules.

## Trust Zones — Enterprise Agent Gateway

**Input:** Public clients reach an authenticated gateway; an internal orchestrator can call approved tools and a protected data store under policy enforcement and audit logging.

**Diagnosis:** Trust transitions and allowed access paths matter more than service inventory.

**Candidates:** Network / Trust Zones, Hub-and-Spoke, System Context.

**Selection:** Network / Trust Zones. Show public, controlled ingress, internal execution, and protected data boundaries. Policy enforcement and audit are labeled only where the source places them; color does not imply guarantees on its own.

## What These Examples Teach

- Choose the diagram that answers the viewer's actual question.
- Keep one abstraction level unless a small secondary pattern is necessary.
- Reject a visually attractive topology when it changes the relationship semantics.
- Never turn absent technical details into architecture facts.
