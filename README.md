# ClipTown desktop tray build matrix

This independent compatibility repository compiles the exact tray-hardened
`cliptown/cliptown-flutter` revision on Linux, macOS, and Windows. Each lane also
runs the deterministic lifecycle-controller tests before building the native
debug application.

The matrix proves cross-platform compilation and lifecycle policy. Native tray
interaction and centered restore are exercised separately by
`cliptown-test/desktop-tray-lifecycle-e2e` on macOS.

This harness does not read clipboard contents, listen for keystrokes, or persist
blobs. Validate its immutable source metadata with
`node scripts/validate-plan.mjs`.
