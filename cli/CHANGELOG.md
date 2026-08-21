# openbot

## 0.2.0

### Minor Changes

- [`cd77f24`](https://github.com/trytilde/openbot/commit/cd77f24613ac272843fe68d7493d3ccefac2a35e) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add agent-centric chat workspaces with rich streamed messages and isolated live Computer desktops per agent.

- [`ff913c3`](https://github.com/trytilde/openbot/commit/ff913c375a8dd607cb45df6844981ea4446ae77c) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Move repository operations into the React Ink CLI and make it own local Hono startup.

- [#71](https://github.com/trytilde/openbot/pull/71) [`983eb35`](https://github.com/trytilde/openbot/commit/983eb352c39fee4fabfe45116b4ee9dcda4c5c28) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add optional local and Vercel-hosted ChatGPT subscription inference with Codex device-code authentication, provider-owned agent templates and deployment assets, and AI SDK 7 support.

- [#66](https://github.com/trytilde/openbot/pull/66) [`b9a66cb`](https://github.com/trytilde/openbot/commit/b9a66cba146cccfc971589b6149603f4085edb3e) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Make Cua Driver the Computer's programmatic GUI backend, expose its runtime catalog as direct local tools, and reconcile canonical and OpenBot computer-use skills for every agent.

- [#60](https://github.com/trytilde/openbot/pull/60) [`c906650`](https://github.com/trytilde/openbot/commit/c9066502f26eda728d1c2c67be9ace4e979ee775) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add `openbot desktop release` and a manually triggered desktop release workflow. Desktop artifacts publish to the shared updates bucket under a fork-guarded prefix with a `version.json` update manifest, and macOS builds are signed and notarized when credentials are present.

- [#48](https://github.com/trytilde/openbot/pull/48) [`2e56350`](https://github.com/trytilde/openbot/commit/2e56350137c8804597a8877d1c5b527221c97a51) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add the developer workflow to the `openbot` CLI for humans and sandboxed agents working on the codebase. Repository gates `e2e` and `desktop package` join `check`, `build`, and `test`; a `mobile` command group carries Expo runs with the Android and Node toolchain resolved, an idempotent headless emulator with loopback VNC, SDK setup, AVD creation, screenshots, logs, and doctor; `connect` and `remote` reach fork-configured mac and Linux dev hosts over ssh. Root scripts adopt a verb:target taxonomy (`dev:mobile:*`, `connect`, `dev:remote`, `doctor`).

- [#69](https://github.com/trytilde/openbot/pull/69) [`206e39f`](https://github.com/trytilde/openbot/commit/206e39f523fa2dd5421ab643d58f02ed9dedb8f3) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Run new-agent setup durably in the trusted development Computer and resume its progress after navigation or reload.

- [`d0aaada`](https://github.com/trytilde/openbot/commit/d0aaada9ff5c00faba2063410b0fd42855951bda) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add interactive encrypted configuration initialization and provider-defined onboarding questions.

  Build and deploy control and agent services as independent artifacts with native TypeScript checks, concurrent per-agent Vercel functions, and separate local services.

  Keep deployment entrypoints, platform configuration, and service templates as provider-owned assets that are materialized by build and deploy lifecycles.

  Provision the trusted development sandbox with the fork environment, encrypted secrets, a user-readable-only age identity, and automatic Bash-profile loading.

  Use one full primary agent at `configuration/agent/` and scaffold equally complete additional agents under `configuration/agent/subagents/<id>/`.

  Provision a named Vercel AI Gateway key during initialization and default authored agents to GPT-5.6 Sol with medium reasoning through AI SDK's built-in Gateway model routing.

  Carry `devMode` through every lifecycle hook. Development skips Vercel service deployment, keeps Tilde reconciliation and local endpoint tunneling active, delegates Vercel Sandbox to Microsandbox, and rebuilds and replaces the local Computer when image inputs change.

  Attribute lifecycle failures to their concrete provider implementation and domain, and print complete redacted CLI error stacks with cause chains by default.

- [#57](https://github.com/trytilde/openbot/pull/57) [`6a328b0`](https://github.com/trytilde/openbot/commit/6a328b0e62e55a3be382c18785e51194d6062914) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Replace the Hello World primary agent with the Factory agent and give it an end-to-end build/test/deploy loop. A new `@tryopenbot/git-provider` derives the fork repository from the checkout's origin remote, brokers a GitHub App credential through Tilde, and reconciles GitHub REST and git-over-HTTPS reverse-proxy profiles; the trusted development sandbox attaches its seeded source tree to the owner's fork through that proxy so the factory agent has an authenticated git client without holding a token. The factory agent's computer tools target the development sandbox, its skills cover creating, locally testing (Tilde local-runtime tunnel), and deploying agents, and the primary agent additionally receives the brokered GitHub toolkit on its MCP server. A background orchestrator (`openbot orchestrate`) owns the lifecycle: edits route every agent through the local-runtime tunnel with hot reload, and settled edits are verified, published to the openbot/sandbox-edits branch, and redeployed automatically. Every subagent can edit its own source in the development sandbox, and the web workspace's New Agent entry scaffolds, registers, and opens a chat with the agent itself.

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

- [`380fbc5`](https://github.com/trytilde/openbot/commit/380fbc56314485d94b1f8b51296fb854e2bb1550) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Represent shared Tilde and Vercel access as concrete platform implementations, centralize their common request and deployment helpers, initialize each once across its dependent providers, and allow init to revisit existing provider configuration with stored prompt defaults. Load fork-owned TypeScript configuration through the standalone CLI's TypeScript loader so generated `.js` specifiers resolve their `.ts` sources.

- [`2b0d90c`](https://github.com/trytilde/openbot/commit/2b0d90c5ebbc457a2cfe2badafa7ad30dd0cb0e4) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add team-scoped Tilde sign-in, browser sessions, and secure desktop token refresh for OpenBot installations.

- [`c75b77d`](https://github.com/trytilde/openbot/commit/c75b77d4c8f1940a5ce787a6e3c03e32b9abd659) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Collapse Tilde agent, skill, registry, MCP, and tool reconciliation into one `AgentProvider` lifecycle, and replace the owner-facing Chat Provider and ConnectRPC projection with the native Tilde REST/SSE bridge.

- [`d6f9091`](https://github.com/trytilde/openbot/commit/d6f90912c7e66b8df710b5aa0013fa764ce55851) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Consolidate provider contracts into their owning packages and add isolated agent workspaces plus a trusted, SOPS-capable development sandbox deployment.

- [#59](https://github.com/trytilde/openbot/pull/59) [`39ceb4b`](https://github.com/trytilde/openbot/commit/39ceb4b4947b60d024115aee0a1c7d9f2deb6010) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add `openbot desktop dev` and `openbot desktop package`, and make the Electron shell runnable on a display-less host. Desktop renders to its own virtual screen on display `:2` with loopback VNC on 5901, separate from the Android emulator's `:1` and 5900 so both run at once; `openbot connect` forwards both screens, and `openbot remote <host> desktop` and `desktop-package` run them on a configured host. Also builds unbuilt workspace dependencies before starting Expo, so a fresh clone no longer fails Metro bundling with `Unable to resolve "@tryopenbot/client-runtime"` when its `dist` is missing.

- [#60](https://github.com/trytilde/openbot/pull/60) [`6c81cb8`](https://github.com/trytilde/openbot/commit/6c81cb86ffa00a966cf13a17b7ebe41ab9e0542b) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Name the desktop identity for its publisher too: the Electron `appId` moves from `dev.openbot.desktop` to `ai.trytilde.openbot`, matching the mobile identifier, and resolves from the same `OPENBOT_APP_ID` a fork already sets for Expo. Done before the first signed release, after which the identifier is baked into every signed artifact.

- [`c7927b4`](https://github.com/trytilde/openbot/commit/c7927b43a71551b8a4d4428a7528ecf650b399e8) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add the complete reusable OpenBot workspace component system, exact light palette, motion curves, agent identity artwork, continuous chat composition, rich message content, activity surface, and Computer pane to `@tryopenbot/ui`.

- [`26d0e7a`](https://github.com/trytilde/openbot/commit/26d0e7abbd7c99decd17fbe961dc62943320720e) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add one fork-owned `configuration/` tree for directly authored Vercel AI SDK-compatible agent endpoints, agent-scoped skills and workspace seeds, and provider integrations, with an interactive terminal CLI for setup and operation. Concrete implementations are grouped under `Configuration({ providers: { ... } })`; repository resources use canonical file locations instead of configurable paths. OpenBot discovers committed agent modules without generating or publishing TypeScript at runtime.

- [#63](https://github.com/trytilde/openbot/pull/63) [`608839d`](https://github.com/trytilde/openbot/commit/608839db733e8c5b023ca13087ffea0c8970cc83) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add shared queued-turn controls and native owner-client parity for onboarding, rich chat, attachments, and Computer takeover.

- [`a1aecaf`](https://github.com/trytilde/openbot/commit/a1aecaf7f691a6f4fff4f79905b57171ab4ad506) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Separate chat APIs from agent provisioning, remove unused model-facing provider
  hooks, and keep authored agents independent through direct SDK integrations and
  non-provider runtime helpers.

- [#59](https://github.com/trytilde/openbot/pull/59) [`7f08497`](https://github.com/trytilde/openbot/commit/7f0849739fadcb51e858b984b8b843b8e85ae7e8) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add store publication for the official OpenBot app through EAS. `openbot mobile release build|submit|status|credentials` drives `eas-cli`, requires an explicit `--yes` before spending build minutes or changing a public listing, and refuses to use the official EAS project from any remote other than `trytilde/openbot`. `apps/mobile/app.json` becomes `app.config.ts` so a fork can point at its own EAS project, bundle identifier, and Expo owner through the environment rather than editing a tracked file. Recorded in ADR-0027.

- [`bd417b1`](https://github.com/trytilde/openbot/commit/bd417b1d7bb0327c031cc4c11a05dfc11f5cb917) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Publish all OpenBot workspace packages publicly with runnable JavaScript artifacts and declarations, and provide `openbot` as an installable standalone CLI.

  Refresh selected AWS profile credentials through AWS CLI before SOPS operations so IAM Identity Center sessions work during initialization and later secret access.

  Support AI agents and automation with non-interactive initialization through stable JSON answers on stdin and machine-readable JSON results.

  Migration:

  - Replace the internal package name `@tryopenbot/cli` with the public `openbot` package.
  - Invoke the installed CLI with `openbot <command>` or `npx openbot <command>`.

- [`c5df8df`](https://github.com/trytilde/openbot/commit/c5df8df5e0244d45c80deba036ce780c94cfc3b8) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Reconcile authored agents, skills, tools, services, and Computers through idempotent provider lifecycles in development and deployment.

- [`a865749`](https://github.com/trytilde/openbot/commit/a865749af593eabe061bb33d137338e17ed78216) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Refine the owner workspace into a continuous per-agent chat with the reference light palette, patterned agent avatars, message replies, file composition, and Tilde connector authorization cards.

- [`1e2084f`](https://github.com/trytilde/openbot/commit/1e2084f0ac32beea9aa9c8293ca092f17af563a0) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Standardize generated source, configuration, service, deployment, and provider assets on strict Handlebars templates.

- [#68](https://github.com/trytilde/openbot/pull/68) [`c2b115e`](https://github.com/trytilde/openbot/commit/c2b115ec173991e6403cbd10fa9d408705b4862a) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Replace the Computer's Openbox desktop with a focused XFCE session and permanent Files and browser launchers.

### Patch Changes

- [`d8c3d20`](https://github.com/trytilde/openbot/commit/d8c3d2011a8399db4979cab6a2da07c4d7709553) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Add one-command provider lifecycle deployment with separate control and agent
  services on Vercel or local systemd and launchd runtimes.

- [#59](https://github.com/trytilde/openbot/pull/59) [`3382853`](https://github.com/trytilde/openbot/commit/338285340d98eb23d37247bc9febfd45aa1b66d3) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Select the Android emulator system image by host CPU: `arm64-v8a` on Apple Silicon and `x86_64` elsewhere. `openbot mobile setup` and `openbot mobile avd` previously hardcoded `x86_64`, which has no hardware acceleration path on an Apple Silicon Mac and produces an unusable emulator.

- [#72](https://github.com/trytilde/openbot/pull/72) [`ce97171`](https://github.com/trytilde/openbot/commit/ce97171a95681822b4355540fb4f8469fe4969f9) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Bound concurrent Tilde skill and tool reconciliation while preserving input order and deterministic errors.

- [#59](https://github.com/trytilde/openbot/pull/59) [`3382853`](https://github.com/trytilde/openbot/commit/338285340d98eb23d37247bc9febfd45aa1b66d3) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Check the Xcode version in `openbot mobile doctor` on macOS, reading the minimum from the installed React Native's CocoaPods helpers so it cannot drift from what `pod install` enforces. React Native 0.86 requires Xcode 16.1; below that, an iOS build fails partway through `pod install` with `Please upgrade XCode` rather than at the toolchain check. Passthrough command failures — `mobile expo`, `mobile logs`, the repository gates — also stop printing the run-log crash notice, because the child process has already reported the error.

- [`f464185`](https://github.com/trytilde/openbot/commit/f4641858b43bcca8318495756f8e5bc17c8d79a4) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Connect the owner workspace to configured Chat Provider agents in local and deployed modes.

  Make Tilde initialization default to production, discover the global control-plane toolkit, and keep mixed age/KMS secret updates compatible with older SOPS and AWS SSO credentials.

  Provision the shared Tilde Vercel UI channel required by Mission Control idempotently.

- [#59](https://github.com/trytilde/openbot/pull/59) [`e148241`](https://github.com/trytilde/openbot/commit/e148241b7520b7cc56a395d9835741c91bcca5f8) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Report compiler search paths that break Xcode module builds in `openbot mobile doctor`. A global `CPPFLAGS` pointing at Homebrew LLVM makes clang find an incompatible C standard library, so an iOS build fails inside the SDK's own modulemap with `found_incompatible_headers__check_search_paths` and a cascade of `could not build module 'Foundation'` that names neither the variable nor the shell. Doctor now names them; it does not change them, because the developer's environment is theirs to own.

- [#69](https://github.com/trytilde/openbot/pull/69) [`206e39f`](https://github.com/trytilde/openbot/commit/206e39f523fa2dd5421ab643d58f02ed9dedb8f3) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Keep agent activity, streamed messages, previews, and unread state updating while another chat is active.

- [`20c5737`](https://github.com/trytilde/openbot/commit/20c5737cffa4f165f023b3fdd7f7a59aaa26316e) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Keep standalone `openbot dev` agent discovery rooted in the fork repository.

- [#59](https://github.com/trytilde/openbot/pull/59) [`b16c8e0`](https://github.com/trytilde/openbot/commit/b16c8e0360a8cf54680537af0591dc917f94d51d) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Report `openbot mobile doctor` failures as diagnostics rather than crashes. A missing tool no longer prints `OpenBot exited unsuccessfully` with a run-log path; the command keeps its non-zero exit code but owns its explanation. Doctor also gains a warning level, warns when the JDK major version is outside the Android Gradle Plugin's supported 17 and 21, names `openbot mobile setup` as the remedy on each failing Android tool check, and checks for CocoaPods on macOS.

- [#61](https://github.com/trytilde/openbot/pull/61) [`165bfa2`](https://github.com/trytilde/openbot/commit/165bfa2e2a50184f7899b1e466b3803ad1ed1acc) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Resolve the workspace root when the task runner starts the CLI inside a package, wait for the control service before dependent development traffic, and keep the computer image test independent of the fork's repository name.

- [`0c99101`](https://github.com/trytilde/openbot/commit/0c99101c84c07441e1bb1eb94a684b7bb56872b1) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Install initialized forks, resolve development packages from source, create Vercel image repositories automatically, and manage described secret and environment values through the CLI.

- [#45](https://github.com/trytilde/openbot/pull/45) [`b10e4ca`](https://github.com/trytilde/openbot/commit/b10e4ca458c43bb36783770c68d9ab77bb7c4db8) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Keep local browser authentication on the Vite origin and reconcile loopback OAuth callbacks during development.

- [#67](https://github.com/trytilde/openbot/pull/67) [`8097727`](https://github.com/trytilde/openbot/commit/80977279b1698672f86155fcaf3281b4cd77a701) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Keep the transcript loading skeleton, scroll-to-bottom control, and Electron drag regions stable across themes and workspace states.

- [`d163506`](https://github.com/trytilde/openbot/commit/d1635064bc407213821d0db2a81ed0fce4faff29) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Improve local diagnostics, preserve chat state while loading, and refine the workspace composer, steering queue, rich media, typography, sizing, and resize behaviour.

- [#59](https://github.com/trytilde/openbot/pull/59) [`d7f61de`](https://github.com/trytilde/openbot/commit/d7f61deee9b34c3dfa32698bf48d2542f04f33c3) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Detect an unbuilt workspace dependency by its runtime export condition rather than the first one listed. A package whose `exports` map starts with `types` and `development` pointing at TypeScript source looked built even when its `dist` was missing, so `openbot mobile expo` skipped the build and Metro failed with `While trying to resolve module @tryopenbot/client-runtime ... specifies a main module field that could not be resolved`.

- [#59](https://github.com/trytilde/openbot/pull/59) [`7aebeae`](https://github.com/trytilde/openbot/commit/7aebeae17fef54d252fcc3360cdd2eb18b5776ff) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Provision the NDK and CMake in `openbot mobile setup`, reading the NDK version React Native pins in its `gradle/libs.versions.toml` rather than restating it, and check the NDK in `openbot mobile doctor`. The Android Gradle Plugin downloads both partway through a build otherwise, and a mismatch surfaces as a failed `configureCMakeDebug` task that names neither the NDK nor the cause.

- [#59](https://github.com/trytilde/openbot/pull/59) [`a498e52`](https://github.com/trytilde/openbot/commit/a498e52b3d63d1b6b43ff26f1a27c33c544bba05) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Resolve the JDK in `openbot mobile doctor` the way Gradle does: `JAVA_HOME` first, `PATH` only as a fallback, with the source named in the output. On a machine with several JDKs installed — a linked Homebrew `openjdk` shadowing a keg-only `openjdk@21`, for instance — the previous check reported the compiler on `PATH` while Gradle built against a different one, so a correctly configured host could still be told its JDK was unsupported. Doctor now also notes when `JAVA_HOME` and `PATH` disagree.

- [#64](https://github.com/trytilde/openbot/pull/64) [`c9e839d`](https://github.com/trytilde/openbot/commit/c9e839d33c664508ae13c25d48e76428ef09bcce) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Show every public top-level `openbot` command in the interactive launcher.

- Updated dependencies [[`cd77f24`](https://github.com/trytilde/openbot/commit/cd77f24613ac272843fe68d7493d3ccefac2a35e), [`ff913c3`](https://github.com/trytilde/openbot/commit/ff913c375a8dd607cb45df6844981ea4446ae77c), [`983eb35`](https://github.com/trytilde/openbot/commit/983eb352c39fee4fabfe45116b4ee9dcda4c5c28), [`720d07c`](https://github.com/trytilde/openbot/commit/720d07caf0c1259a15839842644adb7d49684904), [`b9a66cb`](https://github.com/trytilde/openbot/commit/b9a66cba146cccfc971589b6149603f4085edb3e), [`9db1d92`](https://github.com/trytilde/openbot/commit/9db1d9293a184de2f040eed48f859439b2b2f7af), [`206e39f`](https://github.com/trytilde/openbot/commit/206e39f523fa2dd5421ab643d58f02ed9dedb8f3), [`d0aaada`](https://github.com/trytilde/openbot/commit/d0aaada9ff5c00faba2063410b0fd42855951bda), [`0ee3944`](https://github.com/trytilde/openbot/commit/0ee39446580b8022ce26c414dd44cd6cdc07306a), [`6a328b0`](https://github.com/trytilde/openbot/commit/6a328b0e62e55a3be382c18785e51194d6062914), [`0a4c682`](https://github.com/trytilde/openbot/commit/0a4c682b49c7a72b08d34851d7e53d3cbf0f64d0), [`8fb0d80`](https://github.com/trytilde/openbot/commit/8fb0d809f1eef9cac06d569d0ed0a223de4f6dbf), [`d8c3d20`](https://github.com/trytilde/openbot/commit/d8c3d2011a8399db4979cab6a2da07c4d7709553), [`380fbc5`](https://github.com/trytilde/openbot/commit/380fbc56314485d94b1f8b51296fb854e2bb1550), [`6a9f124`](https://github.com/trytilde/openbot/commit/6a9f124275f9e8230528a78e634d9413d981cf7c), [`2b0d90c`](https://github.com/trytilde/openbot/commit/2b0d90c5ebbc457a2cfe2badafa7ad30dd0cb0e4), [`987ac27`](https://github.com/trytilde/openbot/commit/987ac2713c7b1389e8c2cea45e7c84ce2de799f3), [`ce97171`](https://github.com/trytilde/openbot/commit/ce97171a95681822b4355540fb4f8469fe4969f9), [`c75b77d`](https://github.com/trytilde/openbot/commit/c75b77d4c8f1940a5ce787a6e3c03e32b9abd659), [`f464185`](https://github.com/trytilde/openbot/commit/f4641858b43bcca8318495756f8e5bc17c8d79a4), [`d6f9091`](https://github.com/trytilde/openbot/commit/d6f90912c7e66b8df710b5aa0013fa764ce55851), [`c7927b4`](https://github.com/trytilde/openbot/commit/c7927b43a71551b8a4d4428a7528ecf650b399e8), [`206e39f`](https://github.com/trytilde/openbot/commit/206e39f523fa2dd5421ab643d58f02ed9dedb8f3), [`20c5737`](https://github.com/trytilde/openbot/commit/20c5737cffa4f165f023b3fdd7f7a59aaa26316e), [`19a4a0e`](https://github.com/trytilde/openbot/commit/19a4a0e52b41f5afbdaddaed1029992ed2b4d961), [`165bfa2`](https://github.com/trytilde/openbot/commit/165bfa2e2a50184f7899b1e466b3803ad1ed1acc), [`0c99101`](https://github.com/trytilde/openbot/commit/0c99101c84c07441e1bb1eb94a684b7bb56872b1), [`b10e4ca`](https://github.com/trytilde/openbot/commit/b10e4ca458c43bb36783770c68d9ab77bb7c4db8), [`8097727`](https://github.com/trytilde/openbot/commit/80977279b1698672f86155fcaf3281b4cd77a701), [`d163506`](https://github.com/trytilde/openbot/commit/d1635064bc407213821d0db2a81ed0fce4faff29), [`26d0e7a`](https://github.com/trytilde/openbot/commit/26d0e7abbd7c99decd17fbe961dc62943320720e), [`608839d`](https://github.com/trytilde/openbot/commit/608839db733e8c5b023ca13087ffea0c8970cc83), [`a1aecaf`](https://github.com/trytilde/openbot/commit/a1aecaf7f691a6f4fff4f79905b57171ab4ad506), [`bd417b1`](https://github.com/trytilde/openbot/commit/bd417b1d7bb0327c031cc4c11a05dfc11f5cb917), [`c5df8df`](https://github.com/trytilde/openbot/commit/c5df8df5e0244d45c80deba036ce780c94cfc3b8), [`a865749`](https://github.com/trytilde/openbot/commit/a865749af593eabe061bb33d137338e17ed78216), [`2eee1d1`](https://github.com/trytilde/openbot/commit/2eee1d17e18aee13974456382a9a0556ca9c929c), [`0799a79`](https://github.com/trytilde/openbot/commit/0799a79fc8ef3cb2ba43235afa94bab5b3a3a5ef), [`c9e839d`](https://github.com/trytilde/openbot/commit/c9e839d33c664508ae13c25d48e76428ef09bcce), [`1e2084f`](https://github.com/trytilde/openbot/commit/1e2084f0ac32beea9aa9c8293ca092f17af563a0), [`c2b115e`](https://github.com/trytilde/openbot/commit/c2b115ec173991e6403cbd10fa9d408705b4862a), [`1258ab6`](https://github.com/trytilde/openbot/commit/1258ab624e560ccebbc2ea658d1043b47917c13b)]:
  - @tryopenbot/agent-provider@0.2.0
  - @tryopenbot/agent-service-provider@0.2.0
  - @tryopenbot/computer-service-provider@0.2.0
  - @tryopenbot/computer-tools@0.2.0
  - @tryopenbot/configuration@0.2.0
  - @tryopenbot/utilities@0.2.0
  - @tryopenbot/platform-integrations@0.2.0
  - @tryopenbot/control-service-provider@0.2.0
  - @tryopenbot/runtime-provider@0.2.0
  - @tryopenbot/control-service@0.2.0
  - @tryopenbot/auth-provider@0.2.0
  - @tryopenbot/git-provider@0.2.0
  - @tryopenbot/inference-provider@0.2.0
  - @tryopenbot/connector-tools@0.2.0
