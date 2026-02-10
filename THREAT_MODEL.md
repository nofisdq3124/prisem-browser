# Threat Model – Prism Browser

This document describes the security and privacy assumptions of Prism Browser.

It exists to clearly define:
- What Prism protects against
- What it does not protect against
- What risks are intentionally accepted

This is not a marketing document.

---

## Scope

Prism Browser is a local desktop web browser.

- All browsing occurs on the user’s device
- No server-side rendering or proxying is used
- No Prism-controlled servers are involved in browsing

---

## Threats Considered

Prism aims to reduce exposure to:

- Cross-site tracking via ads and trackers
- Background network requests without user intent
- Accidental data persistence (history, logs, caches)
- Silent telemetry or analytics collection
- Hidden communication with third-party services

---

## Threats Not Addressed

Prism does **not** protect against:

- Network-level identification (IP address, ISP visibility)
- Malicious websites exploiting browser vulnerabilities
- Device compromise or malware on the host system
- Fingerprinting techniques inherent to the web platform
- Government, ISP, or employer surveillance
- Active attackers with control over the network

Users requiring protection from these threats should use tools designed for anonymity and network-level privacy.

---

## Assumptions

Prism assumes:

- The operating system is trusted
- The user’s device is not compromised
- The Firefox base is maintained with upstream security patches
- Users understand that browsing the web inherently reveals information

---

## Design Decisions

Based on this threat model, Prism:

- Disables telemetry entirely
- Avoids persistent storage by default
- Avoids background network activity
- Implements tracker and ad blocking at the network request level
- Documents all privacy-relevant behavior

---

## Tradeoffs

Some usability and compatibility tradeoffs are accepted:

- Some websites may not function correctly
- Features requiring persistent state may be limited
- Convenience features may be omitted

These tradeoffs are intentional.

---

## Review and Evolution

This threat model is a living document.

It should be updated as:
- New features are proposed
- Assumptions change
- Risks are discovered or better understood

