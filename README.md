<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/emailens/.github/main/docs/wordmark-dark.svg">
  <img src="https://raw.githubusercontent.com/emailens/.github/main/docs/wordmark-light.svg" alt="Emailens" width="360">
</picture>

<br />

### The rendering linter for email

**Write once. Know how it behaves across 21 email clients.**

[![npm engine](https://img.shields.io/npm/v/@emailens/engine?label=@emailens/engine&color=8a7544)](https://www.npmjs.com/package/@emailens/engine)
[![tests](https://img.shields.io/badge/tests-1108%20passing-brightgreen)]()
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
  Across <b>298 CSS and HTML features</b> tracked, only <b>6 are fully supported</b> across all 21 email clients.<br/>
  Emailens catches the other 292 before your users do: in the engine, in your terminal, in CI, and in AI coding agents.
</p>

<div align="center">

![emailens terminal lint output](https://raw.githubusercontent.com/emailens/.github/main/docs/lint-demo.png)

</div>

<div align="center">

**Frameworks:** React Email &nbsp;·&nbsp; MJML &nbsp;·&nbsp; Maizzle &nbsp;·&nbsp; Tailwind CSS &nbsp;·&nbsp; Raw HTML  
**Clients:** Gmail &nbsp;·&nbsp; Outlook &nbsp;·&nbsp; Apple Mail &nbsp;·&nbsp; Yahoo Mail &nbsp;·&nbsp; Thunderbird &nbsp;·&nbsp; HEY &nbsp;·&nbsp; Superhuman &nbsp;·&nbsp; Samsung &nbsp;·&nbsp; Proton

</div>

---

## 🛠️ Developer Ecosystem

| Package | Status | Use It For | Quick Start |
|---|---|---|---|
| [**`@emailens/engine`**](https://github.com/emailens/engine) | `v0.12.3` (npm) | Core email compatibility & CSS scoring (298 features, 21 clients) | `npm install @emailens/engine` |
| [**`@emailens/cli`**](https://github.com/emailens/cli) | `v0.6.0` (npm) | Terminal linting & automated CI/CD exit codes | `npx @emailens/cli lint email.html` |
| [**`@emailens/mcp`**](https://github.com/emailens/mcp) | `v0.8.0` (npm) | Email QA in Claude Code, Cursor, and AI agents | `claude mcp add emailens -- npx -y @emailens/mcp` |
| [**`emailens/action`**](https://github.com/emailens/action) | `v1` (Action) | Pull request quality gate in GitHub Actions | `uses: emailens/action@v1` |
| [**`emailens/vscode`**](https://github.com/emailens/vscode) | *In Development* | Editor linting & side-by-side Outlook preview | *Coming soon to Marketplace* |

---

## ⚡ 1. The Core Engine (`@emailens/engine`)

The open-source core powers all Emailens tooling. It parses HTML, simulates client quirks, transforms CSS per client, and evaluates 298 rules with 1,108 automated tests.

```bash
npm install @emailens/engine
```

```typescript
import { auditEmail } from "@emailens/engine";

const report = await auditEmail(htmlSource, {
  clients: ["gmail-web", "outlook-windows", "apple-mail"],
});

console.log(report.overallCompatibility); // 0-100 worst-client score
console.log(report.compatibility);        // per-client scores & issues
console.log(report.spam);                 // heuristic spam flags
console.log(report.accessibility);        // WCAG contrast & alt checks
```

---

## 💻 2. Terminal Linting (`@emailens/cli`)

Analyze files locally or fail CI pipelines on breaking markup:

```bash
# Analyze a single email
npx @emailens/cli analyze email.html

# Lint an entire template directory with a minimum score threshold
npx @emailens/cli lint ./emails --threshold 80
```

---

## 🤖 3. AI Coding Workflow (`@emailens/mcp`)

AI models write great code, but routinely generate email HTML that fails in Outlook, strips styles in Gmail, and breaks dark mode.

Connect Emailens to **Claude Code** or **Cursor** so your agent can lint, audit, and self-repair emails directly:

```bash
claude mcp add emailens -- npx -y @emailens/mcp
```

Included tools: `preview_email`, `analyze_email`, `audit_email`, `fix_email`, `diff_emails`, `check_deliverability`, `list_clients`.

---

## 🚀 4. GitHub Actions (`emailens/action`)

Block pull requests that introduce email regressions:

```yaml
- uses: emailens/action@v1
  with:
    pattern: "emails/**/*.html"
    threshold: "75"
```

---

## ☁️ Hosted QA SaaS ([emailens.dev](https://emailens.dev))

While the core tools run 100% offline, [emailens.dev](https://emailens.dev) provides hosted infrastructure for teams:

- **Real Browser Screenshots:** High-fidelity captures across 21 real clients in light and dark mode.
- **Client Share Links:** Share preview audits with stakeholders without requiring an account.
- **Visual Diff Engine:** Pixel-level regression comparisons between email revisions.
- **Pre-Send Delivery Gate:** REST API and webhook blocking deliverability and spam issues before launch.
- **Self-Healing AI Builder:** Describes and compiles templates, automatically running self-repair loops until output passes 90+ on every client.

---

<div align="center">

Made with care for developers who hate broken inboxes.  
**[emailens.dev](https://emailens.dev)**

</div>
