<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/emailens/.github/main/docs/wordmark-dark.svg">
  <img src="https://raw.githubusercontent.com/emailens/.github/main/docs/wordmark-light.svg" alt="Emailens" width="360">
</picture>

<br />

### The rendering linter for email

**Write once. Know how it behaves across 21 email clients.**

[![npm engine](https://img.shields.io/npm/v/@emailens/engine?label=@emailens/engine&color=8a7544)](https://www.npmjs.com/package/@emailens/engine)
[![tests](https://img.shields.io/badge/tests-1288%20passing-brightgreen)]()
[![npm cli](https://img.shields.io/npm/v/@emailens/cli?label=@emailens/cli&color=blue)](https://www.npmjs.com/package/@emailens/cli)
[![npm mcp](https://img.shields.io/npm/v/@emailens/mcp?label=@emailens/mcp&color=blue)](https://www.npmjs.com/package/@emailens/mcp)
[![GitHub Action](https://img.shields.io/badge/GitHub-Action-2088FF)](https://github.com/emailens/action)
[![license](https://img.shields.io/badge/license-MIT-green)](./LICENSE)

<br />

[Web App](https://emailens.dev) · [Documentation](https://emailens.dev/docs) · [State of Email CSS Report](https://emailens.dev/email-css/report)

---

</div>

<p align="center">
  <b>Your email looks perfect in Apple Mail. Gmail strips half the CSS. Outlook renders it in Microsoft Word.</b><br/>
  Across <b>298 CSS and HTML features</b> tracked, only <b>6 are fully supported</b> across all 21 clients.<br/>
  Emailens catches the other 292 before your users do: in the engine, in your terminal, in CI, and in AI coding agents.
</p>

<div align="center">

![emailens terminal lint output](https://raw.githubusercontent.com/emailens/.github/main/docs/lint-demo.png)

</div>

<div align="center">

**Frameworks:** React Email &nbsp;·&nbsp; MJML &nbsp;·&nbsp; Maizzle &nbsp;·&nbsp; Tailwind CSS &nbsp;·&nbsp; Raw HTML  
**Clients:** Gmail &nbsp;·&nbsp; Outlook &nbsp;·&nbsp; Apple Mail &nbsp;·&nbsp; Yahoo Mail &nbsp;·&nbsp; Thunderbird &nbsp;·&nbsp; HEY &nbsp;·&nbsp; Superhuman &nbsp;·&nbsp; Samsung

</div>

---

## 🛠️ Open-source ecosystem

| Package | Status | Use it for | Quick start |
|---|---|---|---|
| [**`@emailens/engine`**](https://github.com/emailens/engine) | OSS | Core email compatibility and CSS scoring | `npm install @emailens/engine` |
| [**`@emailens/cli`**](https://github.com/emailens/cli) | OSS | Terminal linting and CI checks | `npx @emailens/cli lint email.html` |
| [**`@emailens/mcp`**](https://github.com/emailens/mcp) | OSS | Email QA in Claude Code, Cursor, and AI agents | `claude mcp add emailens -- npx -y @emailens/mcp` |
| [**`emailens/action`**](https://github.com/emailens/action) | OSS | Pull request quality gate in GitHub Actions | `uses: emailens/action@v1` |
| [**`emailens/vscode`**](https://github.com/emailens/vscode) | OSS | Editor linting and side-by-side Outlook preview | `code --install-extension ...` |

---

## ⚡ Start here: CLI

The easiest entry point is the CLI. It works locally, in CI, and in developer workflows without needing a hosted account.

```bash
npx @emailens/cli lint email.html
```

```bash
npx @emailens/cli analyze email.html
npx @emailens/cli preview email.html
```

---

## ☁️ Hosted SaaS

The open-source packages are the local developer toolchain. [emailens.dev](https://emailens.dev) is the hosted SaaS for teams that want:

- real browser screenshots across 21 clients
- shareable preview and audit links
- visual diffing between email revisions
- delivery checks and team workflows

The SaaS is an upgrade path for previewing and collaboration, not a replacement for the local CLI engine.

---

## 🧠 Why developers use Emailens

- Works offline with no account required
- Flags issues before an email ships
- Handles HTML, React Email, MJML, and Maizzle
- Enforces CI quality gates on pull requests
- Integrates with AI agents and coding workflows

---

Made with care for developers who hate broken inboxes.  
**[emailens.dev](https://emailens.dev)**

