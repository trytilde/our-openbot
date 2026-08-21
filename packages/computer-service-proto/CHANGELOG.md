# @tryopenbot/computer-service-proto

## 0.2.0

### Minor Changes

- [`cd77f24`](https://github.com/trytilde/openbot/commit/cd77f24613ac272843fe68d7493d3ccefac2a35e) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add agent-centric chat workspaces with rich streamed messages and isolated live Computer desktops per agent.

- [#71](https://github.com/trytilde/openbot/pull/71) [`983eb35`](https://github.com/trytilde/openbot/commit/983eb352c39fee4fabfe45116b4ee9dcda4c5c28) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add optional local and Vercel-hosted ChatGPT subscription inference with Codex device-code authentication, provider-owned agent templates and deployment assets, and AI SDK 7 support.

- [`720d07c`](https://github.com/trytilde/openbot/commit/720d07caf0c1259a15839842644adb7d49684904) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add the internal computer provider boundary, Microsandbox and Vercel implementations, a capability-protected computer service, and a shared multi-stage OCI image build and deployment lifecycle.

- [#66](https://github.com/trytilde/openbot/pull/66) [`b9a66cb`](https://github.com/trytilde/openbot/commit/b9a66cba146cccfc971589b6149603f4085edb3e) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Make Cua Driver the Computer's programmatic GUI backend, expose its runtime catalog as direct local tools, and reconcile canonical and OpenBot computer-use skills for every agent.

- [#69](https://github.com/trytilde/openbot/pull/69) [`206e39f`](https://github.com/trytilde/openbot/commit/206e39f523fa2dd5421ab643d58f02ed9dedb8f3) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Run new-agent setup durably in the trusted development Computer and resume its progress after navigation or reload.

- [`d0aaada`](https://github.com/trytilde/openbot/commit/d0aaada9ff5c00faba2063410b0fd42855951bda) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add interactive encrypted configuration initialization and provider-defined onboarding questions.

  Build and deploy control and agent services as independent artifacts with native TypeScript checks, concurrent per-agent Vercel functions, and separate local services.

  Keep deployment entrypoints, platform configuration, and service templates as provider-owned assets that are materialized by build and deploy lifecycles.

  Provision the trusted development sandbox with the fork environment, encrypted secrets, a user-readable-only age identity, and automatic Bash-profile loading.

  Use one full primary agent at `configuration/agent/` and scaffold equally complete additional agents under `configuration/agent/subagents/<id>/`.

  Provision a named Vercel AI Gateway key during initialization and default authored agents to GPT-5.6 Sol with medium reasoning through AI SDK's built-in Gateway model routing.

  Carry `devMode` through every lifecycle hook. Development skips Vercel service deployment, keeps Tilde reconciliation and local endpoint tunneling active, delegates Vercel Sandbox to Microsandbox, and rebuilds and replaces the local Computer when image inputs change.

  Attribute lifecycle failures to their concrete provider implementation and domain, and print complete redacted CLI error stacks with cause chains by default.

- [#70](https://github.com/trytilde/openbot/pull/70) [`8fb0d80`](https://github.com/trytilde/openbot/commit/8fb0d809f1eef9cac06d569d0ed0a223de4f6dbf) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add the initial settings catalogue for browsing and assigning tools and skills to bots.

- [`380fbc5`](https://github.com/trytilde/openbot/commit/380fbc56314485d94b1f8b51296fb854e2bb1550) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Represent shared Tilde and Vercel access as concrete platform implementations, centralize their common request and deployment helpers, initialize each once across its dependent providers, and allow init to revisit existing provider configuration with stored prompt defaults. Load fork-owned TypeScript configuration through the standalone CLI's TypeScript loader so generated `.js` specifiers resolve their `.ts` sources.

- [`2b0d90c`](https://github.com/trytilde/openbot/commit/2b0d90c5ebbc457a2cfe2badafa7ad30dd0cb0e4) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add team-scoped Tilde sign-in, browser sessions, and secure desktop token refresh for OpenBot installations.

- [`c75b77d`](https://github.com/trytilde/openbot/commit/c75b77d4c8f1940a5ce787a6e3c03e32b9abd659) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Collapse Tilde agent, skill, registry, MCP, and tool reconciliation into one `AgentProvider` lifecycle, and replace the owner-facing Chat Provider and ConnectRPC projection with the native Tilde REST/SSE bridge.

- [`d6f9091`](https://github.com/trytilde/openbot/commit/d6f90912c7e66b8df710b5aa0013fa764ce55851) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Consolidate provider contracts into their owning packages and add isolated agent workspaces plus a trusted, SOPS-capable development sandbox deployment.

- [`c7927b4`](https://github.com/trytilde/openbot/commit/c7927b43a71551b8a4d4428a7528ecf650b399e8) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add the complete reusable OpenBot workspace component system, exact light palette, motion curves, agent identity artwork, continuous chat composition, rich message content, activity surface, and Computer pane to `@tryopenbot/ui`.

- [`26d0e7a`](https://github.com/trytilde/openbot/commit/26d0e7abbd7c99decd17fbe961dc62943320720e) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add one fork-owned `configuration/` tree for directly authored Vercel AI SDK-compatible agent endpoints, agent-scoped skills and workspace seeds, and provider integrations, with an interactive terminal CLI for setup and operation. Concrete implementations are grouped under `Configuration({ providers: { ... } })`; repository resources use canonical file locations instead of configurable paths. OpenBot discovers committed agent modules without generating or publishing TypeScript at runtime.

- [#63](https://github.com/trytilde/openbot/pull/63) [`608839d`](https://github.com/trytilde/openbot/commit/608839db733e8c5b023ca13087ffea0c8970cc83) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add shared queued-turn controls and native owner-client parity for onboarding, rich chat, attachments, and Computer takeover.

- [`bd417b1`](https://github.com/trytilde/openbot/commit/bd417b1d7bb0327c031cc4c11a05dfc11f5cb917) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Publish all OpenBot workspace packages publicly with runnable JavaScript artifacts and declarations, and provide `openbot` as an installable standalone CLI.

  Refresh selected AWS profile credentials through AWS CLI before SOPS operations so IAM Identity Center sessions work during initialization and later secret access.

  Support AI agents and automation with non-interactive initialization through stable JSON answers on stdin and machine-readable JSON results.

  Migration:

  - Replace the internal package name `@tryopenbot/cli` with the public `openbot` package.
  - Invoke the installed CLI with `openbot <command>` or `npx openbot <command>`.

- [`c5df8df`](https://github.com/trytilde/openbot/commit/c5df8df5e0244d45c80deba036ce780c94cfc3b8) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Reconcile authored agents, skills, tools, services, and Computers through idempotent provider lifecycles in development and deployment.

- [`a865749`](https://github.com/trytilde/openbot/commit/a865749af593eabe061bb33d137338e17ed78216) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Refine the owner workspace into a continuous per-agent chat with the reference light palette, patterned agent avatars, message replies, file composition, and Tilde connector authorization cards.

- [#68](https://github.com/trytilde/openbot/pull/68) [`c2b115e`](https://github.com/trytilde/openbot/commit/c2b115ec173991e6403cbd10fa9d408705b4862a) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Replace the Computer's Openbox desktop with a focused XFCE session and permanent Files and browser launchers.

### Patch Changes

- [#72](https://github.com/trytilde/openbot/pull/72) [`ce97171`](https://github.com/trytilde/openbot/commit/ce97171a95681822b4355540fb4f8469fe4969f9) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Bound concurrent Tilde skill and tool reconciliation while preserving input order and deterministic errors.

- [#69](https://github.com/trytilde/openbot/pull/69) [`206e39f`](https://github.com/trytilde/openbot/commit/206e39f523fa2dd5421ab643d58f02ed9dedb8f3) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Keep agent activity, streamed messages, previews, and unread state updating while another chat is active.

- [`20c5737`](https://github.com/trytilde/openbot/commit/20c5737cffa4f165f023b3fdd7f7a59aaa26316e) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Keep standalone `openbot dev` agent discovery rooted in the fork repository.

- [`0c99101`](https://github.com/trytilde/openbot/commit/0c99101c84c07441e1bb1eb94a684b7bb56872b1) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Install initialized forks, resolve development packages from source, create Vercel image repositories automatically, and manage described secret and environment values through the CLI.

- [#45](https://github.com/trytilde/openbot/pull/45) [`b10e4ca`](https://github.com/trytilde/openbot/commit/b10e4ca458c43bb36783770c68d9ab77bb7c4db8) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Keep local browser authentication on the Vite origin and reconcile loopback OAuth callbacks during development.

- [#67](https://github.com/trytilde/openbot/pull/67) [`8097727`](https://github.com/trytilde/openbot/commit/80977279b1698672f86155fcaf3281b4cd77a701) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Keep the transcript loading skeleton, scroll-to-bottom control, and Electron drag regions stable across themes and workspace states.

- [`d163506`](https://github.com/trytilde/openbot/commit/d1635064bc407213821d0db2a81ed0fce4faff29) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Improve local diagnostics, preserve chat state while loading, and refine the workspace composer, steering queue, rich media, typography, sizing, and resize behaviour.

- [#64](https://github.com/trytilde/openbot/pull/64) [`c9e839d`](https://github.com/trytilde/openbot/commit/c9e839d33c664508ae13c25d48e76428ef09bcce) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Show every public top-level `openbot` command in the interactive launcher.
