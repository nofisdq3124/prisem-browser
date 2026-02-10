# Prism Browser

Prism Browser is a privacy-first, minimal web browser based on Firefox.

It is designed for real users who want transparency, local control, and predictable behavior—without exaggerated claims about anonymity or “total security.”

Prism runs entirely on the user’s machine. It does not proxy traffic, collect telemetry, or perform background network activity without explicit user action.

---

## Project Goals

Prism Browser aims to:

- Respect user privacy by default
- Minimize background activity and hidden behavior
- Provide clear and honest documentation
- Remain understandable and auditable by contributors
- Favor simplicity over feature bloat

Specifically:

- No telemetry or analytics
- No persistent browsing history or logs by default
- No background network requests without user interaction
- Built-in tracker and ad blocking at the network level
- Open source and publicly downloadable
- Licensed under the Apache License 2.0

---

## Non-Goals

Prism Browser does **not** aim to:

- Replace Tor or other anonymity networks
- Guarantee anonymity or untraceability
- Obscure user identity at the network level
- Match full feature parity with Chrome or Firefox
- Market itself with security or privacy hype

If you need strong anonymity guarantees, Prism is not the right tool.

---

## Philosophy

Privacy is not magic.
Security is not absolute.
Software should be honest about its limits.

Prism Browser focuses on:
- Reducing unnecessary data exposure
- Avoiding silent or implicit behavior
- Making tradeoffs explicit and documented

---

## Project Status

This project is in an early design phase.

Initial work focuses on:
- Threat modeling
- Architecture decisions
- Documentation
- Establishing clear boundaries and guarantees

Code will come later.

---

## Contributing

Contributions are welcome, especially in the areas of:

- Threat modeling
- Documentation
- Design discussions
- Privacy and security review

Please read `THREAT_MODEL.md` before proposing changes that affect security or privacy behavior.

---

## License

Prism Browser is licensed under the Apache License 2.0.
See the `LICENSE` file for details.
