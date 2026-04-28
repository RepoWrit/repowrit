<p align="center">
  <a href="https://repowrit.com">
    <img src="https://repowrit.com/icon.svg" alt="RepoWrit" width="64" height="64" />
  </a>
</p>

<h1 align="center">RepoWrit</h1>

<p align="center">
  <strong>Documentation on Autopilot.</strong> Powered by Claude 4.5.<br />
  Turn every git commit into executive briefings, architecture maps, and up-to-date docs.
</p>

<p align="center">
  <a href="https://repowrit.com">repowrit.com</a> · <a href="https://repowrit.com/pricing">Pricing</a> · <a href="https://repowrit.com/changelog">Changelog</a> · <a href="https://repowrit.com/privacy">Privacy</a>
</p>

---

## Installation

RepoWrit is a GitHub App. Setup takes 30 seconds:

1. **Go to [repowrit.com](https://repowrit.com)** and sign in with GitHub.
2. **Install the GitHub App** — select the repositories (and branches) you want to document.
3. **Push code** — RepoWrit automatically analyzes every commit and opens documentation PRs.

That's it. No config files. No CI pipelines. No CLI to install. Your first sync analyzes the last 3 commits so you have a baseline immediately.

> RepoWrit requests minimal GitHub permissions: repository contents (read-only), pull requests (read/write), and webhooks (read-only). On organization plans we additionally read members for role resolution. We never access your settings, secrets, or workflows.

---

## Key Features

### Executive Briefings

AI-generated summaries from three leadership perspectives:

- **Founder View** *(all plans)* — Knowledge moat analysis, documentation coverage, exit-readiness scoring, and business impact metrics. Understand what your engineering investment is building toward.
- **PM View** *(BYOK, Team, Enterprise)* — Developer velocity, energy distribution (features / bugs / refactoring / docs / infra), sprint coverage, and Jira-aware progress (Team and Enterprise). See who's shipping what — without micromanaging.
- **CTO View** *(BYOK, Team, Enterprise)* — Tech debt trends, architectural drift, security risk flags, dependency health. The technical deep-dive for engineering leaders.

PDF export is available on BYOK and above. Weekly email briefings are sent automatically every Monday on paid plans.

### Architecture Maps

AI-powered visualization of your codebase: module layers, import relationships, and dependency graphs. Maps are generated from your actual code structure, not guesswork. Cached for 24 hours with an option to force-refresh.

### Ask RepoWrit (Semantic Search)

Ask your codebase anything in plain English.

- *"What security changes were made last month?"*
- *"Show me all database migration commits"*
- *"Who worked on the payment integration?"*

Results ranked by relevance with impact badges and developer attribution. Powered by `text-embedding-3-small` and synthesized with Claude 4.5. Available on every plan (10 queries/day on Hobbyist, unlimited on paid).

### Automatic Documentation

Every push triggers Claude 4.5 to analyze your diff and generate or update:

- `README.md` — Project overview and usage
- `CHANGELOG.md` — Chronological change entries
- `docs/*.md` — Feature-specific documentation

Changes are delivered as a pull request on the `repoWrit/docs-update` branch. A self-correcting agent retries up to 3 times if CI fails. Review, merge, or ignore — you're always in control.

### PR Reviews & Architecture Guardrail

*BYOK and above.*

External pull requests are auto-analyzed by Claude 4.5. RepoWrit posts a severity-graded review comment flagging architecture violations, risky changes, and missing documentation — before the PR ever gets to a human reviewer.

### Commit Timeline & CSV Export

*BYOK and above.*

Filter commits by date range (1–730 days), author, repo, or branch. Export the result as a CSV (with formula-prefix injection protection) for stakeholder reports, retros, or release notes.

### Multi-Branch Tracking

Track documentation, briefings, and metrics across multiple branches per repository — not just `main`. Switch between branches in the dashboard at any time.

### Bring Your Own Key (BYOK)

Use your own Anthropic, OpenAI, DeepSeek, or compatible custom endpoint. Keys are encrypted at rest with AES-256-GCM and only decrypted in-memory for the duration of a single request. Available on BYOK, Team, and Enterprise plans.

### Governance & Compliance

*Team and Enterprise.*

Organization-scoped KPI dashboard, SOC 2-friendly compliance exports (JSON / CSV), tamper-evident audit trail (SHA-256 hashed), redaction tracking, and Jira integration. Role-based access control with Owner / Admin / Viewer roles.

---

## Privacy & Trust

We take your code seriously.

| Commitment | Detail |
|---|---|
| **Zero Long-Term Code Storage** | Your full source code is processed in-memory and discarded immediately. We persist only AI-generated outputs and operational metadata. |
| **No Model Training** | Your code is never used to train any AI model. We use Anthropic and OpenAI with zero-retention settings. |
| **Minimal Permissions** | Read-only access to repository contents. Write access only for pull requests and review comments. |
| **Encryption** | TLS everywhere. Postgres at rest in Supabase. BYOK keys wrapped with AES-256-GCM. |
| **Diffs Only** | We send only the commit diff to Claude — not your entire repository. |
| **Tamper-Evident Audit Trail** | All admin actions (Team / Enterprise) are SHA-256 hashed for cryptographic integrity. |

Read our full [Privacy Policy](https://repowrit.com/privacy) and [Security Policy](https://github.com/RepoWrit/legal-and-security/blob/main/SECURITY.md).

---

## Plans

| | Hobbyist | BYOK | Team | Enterprise |
|---|---|---|---|---|
| **Price** | Free forever | $4.99/mo | $20/seat/mo | $49.99/seat/mo |
| **Doc Generations** | 5/month | Unlimited | Unlimited | Unlimited |
| **First-Sync Commits** | 3 | Unlimited | Unlimited | Unlimited |
| **Executive Views** | Founder | Founder + PM + CTO | Founder + PM + CTO | Founder + PM + CTO |
| **Ask RepoWrit** | 10/day | Unlimited | Unlimited | Unlimited |
| **Architecture Map** | ✓ | ✓ | ✓ | ✓ |
| **PR Reviews** | — | ✓ | ✓ | ✓ |
| **Commit Timeline + CSV** | — | ✓ | ✓ | ✓ |
| **Weekly Email Briefings** | — | ✓ | ✓ | ✓ |
| **PDF Export** | — | ✓ | ✓ | ✓ |
| **BYOK** | — | ✓ | ✓ | ✓ |
| **Jira Integration** | — | — | ✓ | ✓ |
| **Governance & Audit Exports** | — | — | ✓ | ✓ |
| **Developer Scores** | — | — | ✓ | ✓ |
| **Analysis Window** | 24 hours | 7 days | 30 days | 30 days |
| **Concurrency** | 1 job | 5 jobs | 10 jobs | 20 jobs |
| **Queue Priority** | Standard | Priority | High | Highest |

[Compare plans →](https://repowrit.com/pricing)

---

## Support

- **Bug reports** — [Open an issue](https://github.com/RepoWrit/repowrit/issues/new?template=bug_report.md)
- **Feature requests** — [Open an issue](https://github.com/RepoWrit/repowrit/issues/new?template=feature_request.md)
- **Email** — [support@repowrit.com](mailto:support@repowrit.com)
- **Security** — See [SECURITY.md](https://github.com/RepoWrit/legal-and-security/blob/main/SECURITY.md)

BYOK, Team, and Enterprise customers receive priority support with guaranteed response times. See our [SLA](https://github.com/RepoWrit/legal-and-security/blob/main/SUPPORT.md).

All paid plans include a **5-day money-back guarantee**. See the [Refund Policy](https://repowrit.com/refund).

---

## License

RepoWrit is a proprietary SaaS product. This repository serves as the community and support hub. The source code for the RepoWrit platform is not included here.

---

<p align="center">
  <sub>Built with conviction in India · Powered by Claude 4.5 · <a href="https://repowrit.com">repowrit.com</a></sub>
</p>

# RepoWrit

<p align="center">
  <a href="https://repowrit.com">
    <img src="https://repowrit.com/icon.svg" alt="RepoWrit" width="64" height="64" />
  </a>
</p>

<h1 align="center">RepoWrit</h1>

<p align="center">
  <strong>Documentation on Autopilot.</strong> Powered by Claude 4.5.<br />
  Turn every git commit into executive briefings, architecture maps, and up-to-date docs.
</p>

<p align="center">
  <a href="https://repowrit.com">repowrit.com</a> · <a href="https://repowrit.com/pricing">Pricing</a> · <a href="https://repowrit.com/changelog">Changelog</a> · <a href="https://repowrit.com/privacy">Privacy</a>
</p>

---
