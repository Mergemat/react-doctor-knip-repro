# react-doctor-knip-repro

Minimal repro for `react-doctor` dead-code detection crashing with:

```text
TypeError: issues.files is not iterable
```

## Repro

```bash
bun install
bun run doctor
```

## Expected

`react-doctor` completes dead-code detection or skips it safely.

## Actual

`react-doctor` prints:

```text
✖ Dead code detection failed (non-fatal, skipping).
TypeError: issues.files is not iterable
```

This repro uses:

- React 19
- TypeScript
- Bun
- `react-doctor@0.0.37`
