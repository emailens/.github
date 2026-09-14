<div align="center">

# Emailens

### The rendering linter for email

**Write once. Know how it behaves across 21 email clients.**

[Web App](https://emailens.dev) · [Documentation](https://emailens.dev/docs) · [State of Email CSS](https://emailens.dev/email-css/report)

</div>

---

Only **6 of 298 CSS and HTML properties** are fully supported across all major email clients.  
Emailens catches the other 292 before your users do — in your editor, terminal, CI, and AI coding agent.

Supports **React Email**, **MJML**, **Maizzle**, and **raw HTML**.

---

## 🛠️ Open-Source Developer Ecosystem

| Tool | Focus | Quick Start | What it prevents |
|---|---|---|---|
| [**`mcp`**](https://github.com/emailens/mcp) | Claude Code, Cursor, AI agents | `claude mcp add emailens -- npx -y @emailens/mcp` | *Don't let AI ship broken email* |
| [**`vscode`**](https://github.com/emailens/vscode) | Live editor linter & preview | Install from VS Code Marketplace | *Don't write broken email* |
| [**`cli`**](https://github.com/emailens/cli) | Terminal linting & local testing | `npm install -g @emailens/cli` | *Don't build broken email* |
| [**`action`**](https://github.com/emailens/action) | GitHub Actions CI/CD gate | `uses: emailens/action@v1` | *Don't merge broken email* |
| [**`engine`**](https://github.com/emailens/engine) | Core compatibility engine | `npm install @emailens/engine` | *298 CSS/HTML rules & dark mode transforms* |

---

## 🤖 The AI Email Workflow (MCP)

AI coding agents are great at generating code, but notoriously bad at email compatibility (flexbox, CSS variables, missing VML fallbacks for Outlook, Gmail `<style>` stripping).

Emailens equips **Claude Code**, **Cursor**, and any MCP client with a full QA suite:
- **`analyze_email`** & **`audit_email`**: Compatibility scores, dark mode contrast, spam heuristics, Gmail clipping.
- **`fix_email`**: Framework-native fix instructions that AI agents can apply directly.
- **`diff_emails`**: Verify that code edits improve compatibility without regressions.

```bash
# Connect to Claude Code
claude mcp add emailens -- npx -y @emailens/mcp
```

---

## ☁️ Hosted QA SaaS ([emailens.dev](https://emailens.dev))

While the core linting and engine are 100% open source and offline-first, [emailens.dev](https://emailens.dev) provides hosted infrastructure for teams and production delivery:

- **Real Browser Screenshots:** Rendered captures across 21 real clients in light and dark mode.
- **Client Share Links:** Give teammates and clients reviewable preview URLs without requiring an account.
- **Visual Diff Engine:** Pixel-level regression comparisons between email revisions.
- **Pre-Send Quality Gate:** API & webhook gate blocking broken campaigns before sending.
- **Self-Healing AI Builder:** Describes and compiles emails, running a self-repair loop until they pass 90+ across all 21 clients.

---

<div align="center">

Made with care for developers who hate broken inboxes.  
[emailens.dev](https://emailens.dev)

</div>
