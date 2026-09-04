# Changelog

All notable changes to GREMLIN are documented here. The format follows [Keep a Changelog](https://keepachangelog.com/), and this project adheres to [Semantic Versioning](https://semver.org/).

## [0.2.0] — 2026-09-04

### Added
- CHECK gate: verification step between SLASH and SKIN
  - Test: "can I point to where each claim came from? If no → SHEATHED"
- Self-knowledge clause in SLASH: parameter count, hardware, and energy cost are unknown by default, not inferable
- Failed experiment logged: energy-cost red team (Stage 0)

### Fixed
- Unsupported claims from chained real-sources-to-ungrounded-conclusions now caught pre-delivery

### Lineage note
First kernel-structure change. Same versioning logic as EVE 0.1.0→0.2.0: new capability, not a wording tweak.

## [0.1.0] — 2026-09-04

### Added
- Initial kernel specification (KERNEL.md)
  - Three anchors: Light, Blade, Skin
  - Clock: SPOTLIGHT → SLASH → CHECK → SKIN
  - Three legitimate outputs: Answer, "I don't know," SHEATHED
  - Five rules (including Rule 4: refusal is a feature, Rule 5: trusted context channels are highest-risk)
  - Operationalized metrics: unsupported claim, error, target selection, SHEATHED rate
- Research design documenting control-group spawn experiment
- Experiment log with Gen 1 results and profile injection incident
- Findings document with six findings from the Gen 1 spawn
- README with project overview and lineage
- MIT license

### Lineage
GREMLIN Gen 1 descends from RuneCore → EVE/NOMIC → Rune Forge. It inherits the core rule (capability is not authority; presentation must never manufacture evidence or consent) and the practice of tracking failed experiments openly.
