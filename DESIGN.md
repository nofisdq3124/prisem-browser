# Prism Browser – Design Overview

This document describes the high-level design decisions for Prism Browser.

It defines:
- What Prism changes compared to upstream Firefox ESR
- What behavior is intentionally disabled
- What remains untouched
- What defaults are enforced versus configurable

This document guides implementation and review.

---

## Upstream Base

Prism Browser is based on **Firefox ESR**.

- Upstream security patches are tracked and applied
- Prism does not intentionally lag behind critical security updates
- Major architectural changes in Firefox are adopted cautiously

Prism is not a full fork; it is a curated, opinionated derivative.

---

## Core Design Principles

Prism Browser is designed to:

- Run entirely on the user’s local machine
- Avoid background activity without user intent
- Minimize persistent state
- Prefer explicit behavior over implicit convenience
- Remain auditable by contributors

---

## What Prism Changes

### Telemetry and Reporting

- All Firefox telemetry and data reporting is disabled
- No metrics, usage data, or diagnostics are collected or sent
- No opt-in or opt-out telemetry UI is provided

### Background Network Activity

- Background network requests are disabled where possible
- Services that periodically contact external servers without user action are removed or disabled
- Network access occurs only as a direct result of user interaction

### Persistence and Storage

By default, Prism:

- Does not persist browsing history
- Does not persist network logs
- Minimizes disk caches
- Avoids long-lived identifiers stored on disk

Temporary in-memory state may be used during a session.

### Network-Level Blocking

- Tracker and advertisement blocking is implemented at the network request level
- Blocking is applied consistently across all tabs and contexts
- Blocking behavior is transparent and documented

---

## What Prism Does Not Change

Prism intentionally retains:

- Firefox’s core rendering engine
- Web standards compliance
- Site compatibility where possible
- Firefox’s security model and sandboxing
- User-agent behavior unless explicitly documented

Prism does not attempt to “harden” Firefox beyond its stated goals.

---

## Defaults vs Configuration

Prism enforces strong defaults:

- Telemetry disabled
- No persistent history
- No background services

Users may be allowed to override some behaviors in the future, but:

- Defaults prioritize privacy and predictability
- Overrides must be explicit and documented
- Silent configuration changes are avoided

---

## Non-Goals (Design-Level)

Prism does not include:

- Account systems or cloud sync
- Built-in VPNs, proxies, or relays
- Identity obfuscation or anonymity features
- Fingerprinting resistance beyond basic reductions
- Feature parity with mainstream browsers

These exclusions are intentional and documented.

---

## Review and Evolution

This document evolves with the project.

Any change that affects:
- Network behavior
- Data persistence
- Privacy or security assumptions

must update this document and the threat model accordingly.
