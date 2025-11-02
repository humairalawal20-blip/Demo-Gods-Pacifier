## Summary
Implements two self-contained contracts to stabilize demos by toggling mock responses and suggesting bounded latency values.

## Changes
- offline-mock-swapper: owner-gated mode switch, real/mock registries, metrics, response fetch.
- latency-illusionist: owner-gated latency plans, deterministic suggestions, usage counters.
- Documentation: README on main; PR details here.

## How to test
- clarinet check
- Call init-owner once per contract to set admin.
- Seed endpoints: set-real, set-mock, set-mode, then get-response.
- Plan latency: set-plan, then suggest with any seed.

## Notes
- No traits, no cross-contract calls.
- Deterministic math only; no timers or external state.

## Checklist
- [x] Contracts compile (clarinet check)
- [x] No cross-contract calls or trait usage
- [x] README present on main; contracts on development
- [x] PR body formatted with markdown
