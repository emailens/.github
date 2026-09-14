<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/emailens/.github/main/docs/wordmark-dark.svg">
  <img src="https://raw.githubusercontent.com/emailens/.github/main/docs/wordmark-light.svg" alt="Emailens" width="360">
</picture>

<br />

### The rendering linter for email

**Write once. Know how it behaves across 21 email clients.**

[![npm engine](https://img.shields.io/npm/v/@emailens/engine?label=@emailens/engine&color=8a7544)](https://www.npmjs.com/package/@emailens/engine)
[![npm mcp](https://img.shields.io/npm/v/@emailens/mcp?label=@emailens/mcp&color=blue)](https://www.npmjs.com/package/@emailens/mcp)
[![npm cli](https://img.shields.io/npm/v/@emailens/cli?label=@emailens/cli&color=blue)](https://www.npmjs.com/package/@emailens/cli)
[![VS Code](https://img.shields.io/badge/VS%20Code-Marketplace-007acc)](https://github.com/emailens/vscode)
[![GitHub Action](https://img.shields.io/badge/GitHub-Action-2088FF)](https://github.com/emailens/action)
[![license](https://img.shields.io/badge/license-MIT-green)](./LICENSE)

<br />

[Web App (Instant QA)](https://emailens.dev) · [Documentation](https://emailens.dev/docs) · [State of Email CSS Report](https://emailens.dev/email-css/report)

---

</div>

<p align="center">
  <b>Your email looks perfect in Apple Mail. Gmail strips half the CSS. Outlook renders it in Microsoft Word.</b><br/>
  Across <b>298 CSS and HTML features</b> tracked, only <b>6 are fully supported</b> across all 21 email clients.<br/>
  Emailens catches the other 292 before your users do — in your editor, terminal, CI/CD, and AI agent.
</p>

<div align="center">

![Emailens live preview in Outlook Classic](https://raw.githubusercontent.com/emailens/.github/main/docs/preview.png)

</div>

---

### Supported Everywhere You Build

```
  React Email  ·  MJML  ·  Maizzle  ·  Tailwind CSS  ·  HTML
```

```
  Gmail  ·  Outlook  ·  Apple Mail  ·  Yahoo Mail  ·  Thunderbird  ·  HEY  ·  Superhuman  ·  Samsung  ·  Proton
```

---

## 🛠️ Open-Source Developer Ecosystem

| Tool | Role | Quick Start | What It Catches |
|---|---|---|---|
| [**`mcp`**](https://github.com/emailens/mcp) | **AI Coding Assistants** (Claude Code, Cursor) | `claude mcp add emailens -- npx -y @emailens/mcp` | *Don't let AI ship broken email* |
| [**`vscode`**](https://github.com/emailens/vscode) | **Editor Extension** (Live lint & Outlook preview) | Install from VS Code Marketplace | *Don't write broken email* |
| [**`cli`**](https://github.com/emailens/cli) | **Terminal Linter** (Local testing & scripts) | `npm install -g @emailens/cli` | *Don't build broken email* |
| [**`action`**](https://github.com/emailens/action) | **GitHub Action** (Quality gate in pull requests) | `uses: emailens/action@v1` | *Don't merge broken email* |
| [**`engine`**](https://github.com/emailens/engine) | **Core Library** (298 CSS/HTML rules, dark mode) | `npm install @emailens/engine` | *Core compatibility scoring* |

---

## 🤖 The AI Email Workflow (MCP)

AI coding agents write great code, but routinely generate email markup that silently destroys Outlook, breaks Gmail on mobile, and ruins dark mode contrast.

Emailens equips **Claude Code**, **Cursor**, and any MCP client with a 9-tool email QA suite:
- **`analyze_email`** & **`audit_email`**: Compatibility scores (0-100), dark mode contrast, spam heuristics, 102KB Gmail clipping.
- **`fix_email`**: Framework-native fix instructions the AI applies directly (React Email, MJML, Maizzle, HTML).
- **`diff_emails`**: Verify that fixes improved scores without introducing regressions.

```bash
# Connect to Claude Code
claude mcp add emailens -- npx -y @emailens/mcp
```

---

## 💻 Local Terminal Linting (CLI)

Lint email templates directly in your terminal before committing:

```bash
# Run one-off analysis
npx @emailens/cli analyze email.html

# Lint files with CI-ready exit codes
npx @emailens/cli lint ./emails --threshold 80
```

<div align="center">

![emailens cli lint output](https://raw.githubusercontent.com/emailens/.github/main/docs/lint-demo.png)

</div>

---

## ☁️ Hosted QA SaaS ([emailens.dev](https://emailens.dev))

The core engine and developer tools run 100% offline and free. When your team needs production verification, [emailens.dev](https://emailens.dev) adds cloud infrastructure:

- **Real Browser Screenshots:** High-fidelity captures across 21 clients in light & dark mode.
- **Shareable Preview Links:** Share full rendering audits with teammates and clients (no login required to view).
- **Visual Regression Diffs:** Compare email revisions side-by-side to catch unexpected layout shifts.
- **Pre-Send Delivery Gate:** REST API and webhook blocking deliverability and spam issues before launch.
- **Self-Healing AI Builder:** Describes and compiles templates, automatically running self-repair loops until output passes 90+ on every client.

---

<div align="center">

Made with care for developers who hate broken inboxes.  
**[emailens.dev](https://emailens.dev)**

</div>
