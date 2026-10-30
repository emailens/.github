<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/emailens/.github/main/docs/wordmark-dark.svg">
  <img src="https://raw.githubusercontent.com/emailens/.github/main/docs/wordmark-light.svg" alt="Emailens" width="360">
</picture>

<br />

### The rendering linter for email

**Write once. Know how it behaves across 21 email clients.**

[![npm engine](https://badgen.net/npm/v/@emailens/engine?label=@emailens/engine&color=8a7544)](https://www.npmjs.com/package/@emailens/engine)
[![CI](https://github.com/emailens/engine/actions/workflows/ci.yml/badge.svg)](https://github.com/emailens/engine/actions/workflows/ci.yml)
[![npm cli](https://badgen.net/npm/v/@emailens/cli?label=@emailens/cli&color=blue)](https://www.npmjs.com/package/@emailens/cli)
[![npm mcp](https://badgen.net/npm/v/@emailens/mcp?label=@emailens/mcp&color=blue)](https://www.npmjs.com/package/@emailens/mcp)
[![GitHub Action](https://badgen.net/badge/GitHub/Action/2088FF)](https://github.com/emailens/action)
[![license](https://badgen.net/badge/license/MIT/green)](https://github.com/emailens/engine/blob/main/LICENSE)

<br />

[Web App](https://emailens.dev) · [Documentation](https://emailens.dev/docs) · [State of Email CSS Report](https://emailens.dev/email-css/report)

---

</div>

<p align="center">
  <b>Your email looks perfect in Apple Mail. Gmail strips half the CSS. Outlook renders it in Microsoft Word.</b><br/>
  Of the <b>300 CSS and HTML features</b> the engine tracks, only <b>6 work in all 21</b> email clients.<br/>
  Emailens catches the other 294 before your readers do: in your code, your terminal, your editor, CI and AI coding agents.
</p>

<div align="center">

![Real output of npx @emailens/cli lint on a welcome email: flex and gap in Outlook Classic, box-shadow in Gmail, a quoted font in Yahoo Mail, a short preheader](https://raw.githubusercontent.com/emailens/.github/main/docs/lint-demo.png)

</div>

<div align="center">

**Frameworks:** React Email &nbsp;·&nbsp; MJML &nbsp;·&nbsp; Maizzle &nbsp;·&nbsp; Tailwind CSS &nbsp;·&nbsp; Raw HTML  
**Clients:** Gmail &nbsp;·&nbsp; Outlook (Classic, New, 365, Mac, mobile) &nbsp;·&nbsp; Apple Mail &nbsp;·&nbsp; Yahoo Mail &nbsp;·&nbsp; Samsung Mail &nbsp;·&nbsp; Thunderbird &nbsp;·&nbsp; HEY &nbsp;·&nbsp; Proton &nbsp;·&nbsp; AOL &nbsp;·&nbsp; Fastmail &nbsp;·&nbsp; Superhuman

</div>

---

## 🛠️ Developer Ecosystem

| Package | Status | Use It For | Quick Start |
|---|---|---|---|
| [**`@emailens/engine`**](https://github.com/emailens/engine) | ![npm](https://badgen.net/npm/v/@emailens/engine?label=) | Core compatibility analysis & per-client CSS scoring (300 features, 21 clients) | `npm install @emailens/engine` |
| [**`@emailens/cli`**](https://github.com/emailens/cli) | ![npm](https://badgen.net/npm/v/@emailens/cli?label=) | Terminal linting with line:column findings & CI exit codes | `npx @emailens/cli lint email.html` |
| [**`@emailens/mcp`**](https://github.com/emailens/mcp) | ![npm](https://badgen.net/npm/v/@emailens/mcp?label=) | Email QA in Claude Code, Cursor, and AI agents | `claude mcp add emailens -- npx -y @emailens/mcp` |
| [**`emailens/action`**](https://github.com/emailens/action) | ![tag](https://badgen.net/github/tag/emailens/action?label=) | Pull request quality gate in GitHub Actions | `uses: emailens/action@v1` |
| [**`emailens/vscode`**](https://github.com/emailens/vscode) | *In development* | Editor linting, Outlook preview & Quick Fixes | *Not released yet* |

---

## ⚡ 1. The Core Engine (`@emailens/engine`)

The open-source core powers all Emailens tooling. It compiles React Email, MJML and Maizzle, transforms CSS per client, simulates dark mode, and checks 300 CSS and HTML features plus spam, accessibility, link and image quality.

```bash
npm install @emailens/engine
```

```typescript
import { auditEmail } from "@emailens/engine";

const report = auditEmail(htmlSource, { framework: "jsx" });

console.log(report.compatibility.scores["outlook-windows"]); // per-client score
console.log(report.spam);          // heuristic spam flags
console.log(report.accessibility); // WCAG contrast & alt checks
```

---

## 💻 2. Terminal Linting (`@emailens/cli`)

Lint locally, no account and no network, or fail a CI job on breaking markup:

```bash
# Lint one email: findings with line:column
npx @emailens/cli lint email.html

# Fail the build on warnings too
npx -y @emailens/cli lint 'emails/*.html' --fail-on-warning
```

---

## 🤖 3. AI Coding Workflow (`@emailens/mcp`)

AI models write great code, but routinely generate email HTML that fails in Outlook, strips styles in Gmail, and breaks dark mode.

Connect Emailens to **Claude Code** or **Cursor** so your agent can lint, audit, and self-repair emails directly:

```bash
claude mcp add emailens -- npx -y @emailens/mcp
```

Included tools: `preview_email`, `analyze_email`, `audit_email`, `fix_email`, `diff_emails`, `check_deliverability`, `list_clients`, plus hosted `capture_screenshots` and `share_preview` (emailens.dev API key).

---

## 🚀 4. GitHub Actions (`emailens/action`)

Block pull requests that introduce email regressions:

```yaml
- uses: emailens/action@v1
  with:
    pattern: "emails/**/*.html"
    threshold: "75"
```

With `mode: inbox` it checks the real email your app sends instead, and fails when it changes.

---

## ☁️ Hosted QA SaaS ([emailens.dev](https://emailens.dev))

The engine, the CLI, the VS Code extension and the MCP's local tools run offline. [emailens.dev](https://emailens.dev) adds what needs a server:

- **Per-client previews:** your email rendered as each of the 21 clients would show it, in light and dark mode.
- **Real-device checks:** screenshots from real installs, to confirm what a preview predicts.
- **Share links and visual diffs:** send a preview to a client or teammate without an account; compare two revisions.
- **AI Fix:** rewrites the parts a client breaks, keeping the design.
- **Deliverability:** SPF, DKIM and DMARC checks before you send.

---

<div align="center">

Made with care for developers who hate broken inboxes.  
**[emailens.dev](https://emailens.dev)**

</div>
