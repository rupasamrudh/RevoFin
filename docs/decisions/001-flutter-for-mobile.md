
# Decision 001: Use Flutter for the Mobile App

- Status: Accepted
- Date: 2026-10-19
- Sprint: 0

## Context

RevoFin is a solo-build project with limited development hours. Android is the first target platform, with iOS planned later. The app needs smooth vertical video scrolling, and the codebase should remain manageable for one engineer.

## Options considered

1. **Flutter:** Pros — shared codebase for Android and iOS, consistent UI, and a single primary language. Cons — video playback and scrolling performance must be validated on real devices.
2. **React Native:** Pros — cross-platform development and a JavaScript/TypeScript ecosystem. Cons — requires learning and maintaining the React Native approach and its associated tooling.
3. **Native Android:** Pros — direct access to Android APIs and platform-specific optimization. Cons — a separate iOS implementation would be needed later.

## Decision

Use Flutter with Dart for the mobile application, targeting Android first while keeping the architecture suitable for a future iOS release.

## Consequences

Cross-platform development becomes easier to manage as a solo engineer, but smooth video playback and scrolling cannot be assumed. In Sprint 4, test feed performance on a real, mid-range Android device, targeting 60 fps and a first video frame in under 1.5 seconds on 4G. If performance fails, profile the feed, optimize video loading and rendering, and reconsider the relevant implementation choices before expanding scope.
