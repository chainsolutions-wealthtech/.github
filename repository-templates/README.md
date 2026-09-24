# Repository Templates Source

This directory stores governed repository blueprints owned by the organization.

Each child directory mirrors the root of a target repository. The source blueprint is versioned here before being materialized as an actual GitHub Template Repository.

## Governed Repository Template

`governed-repository-template/` is the generic governance core extracted from proven patterns without copying project-specific state.

It contains:
- mandatory reading order;
- machine-readable governance profile;
- persistent project memory;
- Loop Engineering;
- zero-regression rules;
- project-state placeholders;
- ADR / architecture baseline;
- initialization and validation scripts;
- governance CI;
- issue / pull-request templates.

Project-specific regulatory, financial, infrastructure or application state is explicitly excluded.
