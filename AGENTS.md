# PPL Node — Development Guidance

## General principles

- Prefer simple, readable, standards-based solutions.
- Keep the system modular and easy to test.
- Avoid unnecessary dependencies.
- Treat privacy and offline operation as core requirements.
- Document important technical decisions.
- Do not assume Internet access is available.
- Keep user-facing interactions simple and approachable.

## Development workflow

- Make small, understandable changes.
- Test hardware assumptions before building on them.
- Record significant decisions in `docs/decisions.md`.
- Keep experiments separate from production firmware.