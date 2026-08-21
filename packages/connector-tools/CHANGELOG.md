# @tryopenbot/connector-tools

## 0.2.0

### Minor Changes

- [#65](https://github.com/trytilde/openbot/pull/65) [`0a4c682`](https://github.com/trytilde/openbot/commit/0a4c682b49c7a72b08d34851d7e53d3cbf0f64d0) Thanks [@danielblignaut](https://github.com/danielblignaut)! - Bots configure their own connectors from chat. The new `configure_connector`
  agent tool renders an in-chat account picker on web, desktop, and Expo;
  new-account credential setup posts to owner-authenticated `/api/connectors`
  routes so secrets never enter the transcript; brokered OAuth returns land on
  `/connectors/authorized` and hand back to the agent automatically. The agent
  reconciler now maps every Tilde control-plane function onto each agent's MCP
  server, namespaces Tilde skill names per agent, and agent templates ship the
  tool plus eight Tilde platform skills. Modal overlays are URL-routable via
  workspace search params.
