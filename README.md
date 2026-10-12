# Plotter for GitHub Copilot and Cursor

[Plotter](https://plotter.run) lets people mark up websites, web apps, images and
designs, share feedback and track changes together, in their browser or on iPhone
and iPad. This plugin connects your coding agent to your Plotter account so it can
work through that feedback. It's an [Agent Plugin](https://agent-plugins.org)
(1.0), so the same plugin works in GitHub Copilot (CLI, VS Code and the Copilot
app) and Cursor.

- **apply-feedback**: reads the open tasks for a site (each tied to the exact page
  element, with a picture of the mark), marks each one in progress, makes the
  change, and resolves it with a reply saying what changed. When a task is unclear
  it asks you, or asks the reviewer on the task's thread and leaves it open until
  they answer.
- **get-feedback**: builds a static site, hosts it privately on Plotter and returns
  a review link for your client.

## Install

**GitHub Copilot CLI**

```sh
copilot plugin install Plotter-Run/agent-plugins
```

**VS Code (Copilot)**: run **Chat: Install Plugin From Source** from the Command
Palette and enter `https://github.com/Plotter-Run/agent-plugins`.

**Cursor**: install **Plotter** from the Cursor Marketplace.

The first time the agent uses Plotter, it asks you to sign in: Plotter opens in
your browser, you sign in and pick the organization. There's no token to copy.
Revoke access any time in Plotter under **Settings › Integrations**.

## Use it

In your site's repository, ask:

- "Work through the Plotter feedback for https://example.com"
- "What did the client say about the pricing page?"
- "Build this and send it to Plotter for review"

## Without the plugin

Add the MCP server `https://app.plotter.run/v1/mcp` (streamable HTTP) in your
agent's MCP settings; it signs in with OAuth. For scripts and CI, send an
integration token from **Settings › Integrations** as
`Authorization: Bearer <token>`.

## Help

- Setup guide: https://plotter.run/help/connect-claude-code-or-codex
- Privacy: https://plotter.run/privacy
- Support: https://plotter.run/support
