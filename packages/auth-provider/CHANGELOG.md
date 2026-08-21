# @tryopenbot/auth-provider

## 0.2.0

### Minor Changes

- [#71](https://github.com/trytilde/openbot/pull/71) [`983eb35`](https://github.com/trytilde/openbot/commit/983eb352c39fee4fabfe45116b4ee9dcda4c5c28) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add optional local and Vercel-hosted ChatGPT subscription inference with Codex device-code authentication, provider-owned agent templates and deployment assets, and AI SDK 7 support.

- [#66](https://github.com/trytilde/openbot/pull/66) [`b9a66cb`](https://github.com/trytilde/openbot/commit/b9a66cba146cccfc971589b6149603f4085edb3e) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Make Cua Driver the Computer's programmatic GUI backend, expose its runtime catalog as direct local tools, and reconcile canonical and OpenBot computer-use skills for every agent.

- [#69](https://github.com/trytilde/openbot/pull/69) [`206e39f`](https://github.com/trytilde/openbot/commit/206e39f523fa2dd5421ab643d58f02ed9dedb8f3) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Run new-agent setup durably in the trusted development Computer and resume its progress after navigation or reload.

- [#47](https://github.com/trytilde/openbot/pull/47) [`0ee3944`](https://github.com/trytilde/openbot/commit/0ee39446580b8022ce26c414dd44cd6cdc07306a) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add a shared Zustand client runtime and grouped UI contracts, migrate web and Electron authentication and chat onto it, and add the first Expo mobile client with control-service selection, native authentication, sidebar, and conversation workflows.

- [#70](https://github.com/trytilde/openbot/pull/70) [`8fb0d80`](https://github.com/trytilde/openbot/commit/8fb0d809f1eef9cac06d569d0ed0a223de4f6dbf) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add the initial settings catalogue for browsing and assigning tools and skills to bots.

- [`2b0d90c`](https://github.com/trytilde/openbot/commit/2b0d90c5ebbc457a2cfe2badafa7ad30dd0cb0e4) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add team-scoped Tilde sign-in, browser sessions, and secure desktop token refresh for OpenBot installations.

- [#63](https://github.com/trytilde/openbot/pull/63) [`608839d`](https://github.com/trytilde/openbot/commit/608839db733e8c5b023ca13087ffea0c8970cc83) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add shared queued-turn controls and native owner-client parity for onboarding, rich chat, attachments, and Computer takeover.

- [#68](https://github.com/trytilde/openbot/pull/68) [`c2b115e`](https://github.com/trytilde/openbot/commit/c2b115ec173991e6403cbd10fa9d408705b4862a) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Replace the Computer's Openbox desktop with a focused XFCE session and permanent Files and browser launchers.

### Patch Changes

- [#72](https://github.com/trytilde/openbot/pull/72) [`ce97171`](https://github.com/trytilde/openbot/commit/ce97171a95681822b4355540fb4f8469fe4969f9) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Bound concurrent Tilde skill and tool reconciliation while preserving input order and deterministic errors.

- [#69](https://github.com/trytilde/openbot/pull/69) [`206e39f`](https://github.com/trytilde/openbot/commit/206e39f523fa2dd5421ab643d58f02ed9dedb8f3) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Keep agent activity, streamed messages, previews, and unread state updating while another chat is active.

- [#45](https://github.com/trytilde/openbot/pull/45) [`b10e4ca`](https://github.com/trytilde/openbot/commit/b10e4ca458c43bb36783770c68d9ab77bb7c4db8) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Keep local browser authentication on the Vite origin and reconcile loopback OAuth callbacks during development.

- [#67](https://github.com/trytilde/openbot/pull/67) [`8097727`](https://github.com/trytilde/openbot/commit/80977279b1698672f86155fcaf3281b4cd77a701) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Keep the transcript loading skeleton, scroll-to-bottom control, and Electron drag regions stable across themes and workspace states.

- [`d163506`](https://github.com/trytilde/openbot/commit/d1635064bc407213821d0db2a81ed0fce4faff29) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Improve local diagnostics, preserve chat state while loading, and refine the workspace composer, steering queue, rich media, typography, sizing, and resize behaviour.

- [#64](https://github.com/trytilde/openbot/pull/64) [`c9e839d`](https://github.com/trytilde/openbot/commit/c9e839d33c664508ae13c25d48e76428ef09bcce) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Show every public top-level `openbot` command in the interactive launcher.

- Updated dependencies [[`cd77f24`](https://github.com/trytilde/openbot/commit/cd77f24613ac272843fe68d7493d3ccefac2a35e), [`983eb35`](https://github.com/trytilde/openbot/commit/983eb352c39fee4fabfe45116b4ee9dcda4c5c28), [`b9a66cb`](https://github.com/trytilde/openbot/commit/b9a66cba146cccfc971589b6149603f4085edb3e), [`206e39f`](https://github.com/trytilde/openbot/commit/206e39f523fa2dd5421ab643d58f02ed9dedb8f3), [`d0aaada`](https://github.com/trytilde/openbot/commit/d0aaada9ff5c00faba2063410b0fd42855951bda), [`6a328b0`](https://github.com/trytilde/openbot/commit/6a328b0e62e55a3be382c18785e51194d6062914), [`8fb0d80`](https://github.com/trytilde/openbot/commit/8fb0d809f1eef9cac06d569d0ed0a223de4f6dbf), [`d8c3d20`](https://github.com/trytilde/openbot/commit/d8c3d2011a8399db4979cab6a2da07c4d7709553), [`380fbc5`](https://github.com/trytilde/openbot/commit/380fbc56314485d94b1f8b51296fb854e2bb1550), [`2b0d90c`](https://github.com/trytilde/openbot/commit/2b0d90c5ebbc457a2cfe2badafa7ad30dd0cb0e4), [`ce97171`](https://github.com/trytilde/openbot/commit/ce97171a95681822b4355540fb4f8469fe4969f9), [`c75b77d`](https://github.com/trytilde/openbot/commit/c75b77d4c8f1940a5ce787a6e3c03e32b9abd659), [`f464185`](https://github.com/trytilde/openbot/commit/f4641858b43bcca8318495756f8e5bc17c8d79a4), [`d6f9091`](https://github.com/trytilde/openbot/commit/d6f90912c7e66b8df710b5aa0013fa764ce55851), [`c7927b4`](https://github.com/trytilde/openbot/commit/c7927b43a71551b8a4d4428a7528ecf650b399e8), [`206e39f`](https://github.com/trytilde/openbot/commit/206e39f523fa2dd5421ab643d58f02ed9dedb8f3), [`20c5737`](https://github.com/trytilde/openbot/commit/20c5737cffa4f165f023b3fdd7f7a59aaa26316e), [`0c99101`](https://github.com/trytilde/openbot/commit/0c99101c84c07441e1bb1eb94a684b7bb56872b1), [`b10e4ca`](https://github.com/trytilde/openbot/commit/b10e4ca458c43bb36783770c68d9ab77bb7c4db8), [`8097727`](https://github.com/trytilde/openbot/commit/80977279b1698672f86155fcaf3281b4cd77a701), [`d163506`](https://github.com/trytilde/openbot/commit/d1635064bc407213821d0db2a81ed0fce4faff29), [`608839d`](https://github.com/trytilde/openbot/commit/608839db733e8c5b023ca13087ffea0c8970cc83), [`bd417b1`](https://github.com/trytilde/openbot/commit/bd417b1d7bb0327c031cc4c11a05dfc11f5cb917), [`c5df8df`](https://github.com/trytilde/openbot/commit/c5df8df5e0244d45c80deba036ce780c94cfc3b8), [`a865749`](https://github.com/trytilde/openbot/commit/a865749af593eabe061bb33d137338e17ed78216), [`c9e839d`](https://github.com/trytilde/openbot/commit/c9e839d33c664508ae13c25d48e76428ef09bcce), [`c2b115e`](https://github.com/trytilde/openbot/commit/c2b115ec173991e6403cbd10fa9d408705b4862a)]:
  - @tryopenbot/platform-integrations@0.2.0
  - @tryopenbot/runtime-provider@0.2.0
