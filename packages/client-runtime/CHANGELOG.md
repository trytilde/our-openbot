# @tryopenbot/client-runtime

## 0.2.0

### Minor Changes

- [#71](https://github.com/trytilde/openbot/pull/71) [`983eb35`](https://github.com/trytilde/openbot/commit/983eb352c39fee4fabfe45116b4ee9dcda4c5c28) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add optional local and Vercel-hosted ChatGPT subscription inference with Codex device-code authentication, provider-owned agent templates and deployment assets, and AI SDK 7 support.

- [#66](https://github.com/trytilde/openbot/pull/66) [`b9a66cb`](https://github.com/trytilde/openbot/commit/b9a66cba146cccfc971589b6149603f4085edb3e) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Make Cua Driver the Computer's programmatic GUI backend, expose its runtime catalog as direct local tools, and reconcile canonical and OpenBot computer-use skills for every agent.

- [#69](https://github.com/trytilde/openbot/pull/69) [`206e39f`](https://github.com/trytilde/openbot/commit/206e39f523fa2dd5421ab643d58f02ed9dedb8f3) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Run new-agent setup durably in the trusted development Computer and resume its progress after navigation or reload.

- [#47](https://github.com/trytilde/openbot/pull/47) [`0ee3944`](https://github.com/trytilde/openbot/commit/0ee39446580b8022ce26c414dd44cd6cdc07306a) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add a shared Zustand client runtime and grouped UI contracts, migrate web and Electron authentication and chat onto it, and add the first Expo mobile client with control-service selection, native authentication, sidebar, and conversation workflows.

- [#65](https://github.com/trytilde/openbot/pull/65) [`0a4c682`](https://github.com/trytilde/openbot/commit/0a4c682b49c7a72b08d34851d7e53d3cbf0f64d0) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Bots configure their own connectors from chat. The new `configure_connector`
  agent tool renders an in-chat account picker on web, desktop, and Expo;
  new-account credential setup posts to owner-authenticated `/api/connectors`
  routes so secrets never enter the transcript; brokered OAuth returns land on
  `/connectors/authorized` and hand back to the agent automatically. The agent
  reconciler now maps every Tilde control-plane function onto each agent's MCP
  server, namespaces Tilde skill names per agent, and agent templates ship the
  tool plus eight Tilde platform skills. Modal overlays are URL-routable via
  workspace search params.

- [#70](https://github.com/trytilde/openbot/pull/70) [`8fb0d80`](https://github.com/trytilde/openbot/commit/8fb0d809f1eef9cac06d569d0ed0a223de4f6dbf) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add the initial settings catalogue for browsing and assigning tools and skills to bots.

- [#63](https://github.com/trytilde/openbot/pull/63) [`608839d`](https://github.com/trytilde/openbot/commit/608839db733e8c5b023ca13087ffea0c8970cc83) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add shared queued-turn controls and native owner-client parity for onboarding, rich chat, attachments, and Computer takeover.

- [#59](https://github.com/trytilde/openbot/pull/59) [`4659f2b`](https://github.com/trytilde/openbot/commit/4659f2b5101bee5766557368d4877a45f0b2bc11) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Move onboarding state into `@tryopenbot/client-runtime`. Completion and the resulting agent description are persisted, survive reload, and decide whether a client shows first-run at all, so per ADR-0017 they are runtime state rather than renderer state. The runtime owns the contract, validation, and read/write, and the platform supplies key/value storage — `localStorage` on web, and the same interface accepts Expo SecureStore or the Electron bridge unchanged. `OnboardingResult` now has one definition, re-exported by `@tryopenbot/ui` so callers keep a single type.

- [#68](https://github.com/trytilde/openbot/pull/68) [`c2b115e`](https://github.com/trytilde/openbot/commit/c2b115ec173991e6403cbd10fa9d408705b4862a) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Replace the Computer's Openbox desktop with a focused XFCE session and permanent Files and browser launchers.

- [#58](https://github.com/trytilde/openbot/pull/58) [`1258ab6`](https://github.com/trytilde/openbot/commit/1258ab624e560ccebbc2ea658d1043b47917c13b) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Rebuild the workspace UI on vendored shadcn/ui, Beautiful UI, and AI Elements sources: semantic design tokens with light/dark class-based theming, the generated agent avatar engine, sidebar rows with an account menu and command palette actions, persisted client workspace switching with an automatic loopback development workspace, composer shortcuts and attachment thumbnails, queue-authoritative message submission and steering with deployment-enforced Tilde queue policies, causally ordered late replies, direct screenshot media rendering without tool-result JSON, segmented assistant transcript rendering with prose-only bubbles and merged tool runs, and a first-run onboarding flow. OpenBot-authored surfaces carry the `ob-` class prefix and OpenBot's own copy.

### Patch Changes

- [#72](https://github.com/trytilde/openbot/pull/72) [`ce97171`](https://github.com/trytilde/openbot/commit/ce97171a95681822b4355540fb4f8469fe4969f9) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Bound concurrent Tilde skill and tool reconciliation while preserving input order and deterministic errors.

- [#69](https://github.com/trytilde/openbot/pull/69) [`206e39f`](https://github.com/trytilde/openbot/commit/206e39f523fa2dd5421ab643d58f02ed9dedb8f3) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Keep agent activity, streamed messages, previews, and unread state updating while another chat is active.

- [#67](https://github.com/trytilde/openbot/pull/67) [`8097727`](https://github.com/trytilde/openbot/commit/80977279b1698672f86155fcaf3281b4cd77a701) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Keep the transcript loading skeleton, scroll-to-bottom control, and Electron drag regions stable across themes and workspace states.

- [`d163506`](https://github.com/trytilde/openbot/commit/d1635064bc407213821d0db2a81ed0fce4faff29) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Improve local diagnostics, preserve chat state while loading, and refine the workspace composer, steering queue, rich media, typography, sizing, and resize behaviour.

- [#64](https://github.com/trytilde/openbot/pull/64) [`c9e839d`](https://github.com/trytilde/openbot/commit/c9e839d33c664508ae13c25d48e76428ef09bcce) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Show every public top-level `openbot` command in the interactive launcher.
