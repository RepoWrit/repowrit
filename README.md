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
2. **Install the GitHub App** — select the repositories you want to document.
3. **Push code** — RepoWrit automatically analyzes every commit and opens documentation PRs.

That's it. No config files. No CI pipelines. No CLI to install.

> RepoWrit requests minimal GitHub permissions: repository contents (read-only) and pull requests (read/write). We never access your settings, secrets, or workflows.

---

## Key Features

### Executive Briefings

AI-generated summaries from three leadership perspectives:

- **Founder View** *(Hobby, Builder, Scale)* — Exit-readiness scoring, knowledge moat analysis, business impact metrics. Understand what your engineering investment is building toward.
- **PM View** *(Builder, Scale)* — Developer velocity, effort distribution, sprint coverage. See who's shipping what — without micromanaging.
- **CTO View** *(Scale)* — Tech debt trends, risk flags, architecture drift, dependency health. The technical deep-dive for engineering leaders.

Scale plan ($44.99/mo) unlocks all three views, PDF export, and a 7-day rolling analysis window.

### Architecture Maps

*Scale plan exclusive.*

AI-powered visualization of your codebase: module layers, import relationships, and dependency graphs. Maps are generated from your actual code structure, not guesswork. Cached for 24 hours with option to force-refresh.

### Semantic Search

Ask your codebase anything in plain English.

- *"What security changes were made last month?"*
- *"Show me all database migration commits"*
- *"Who worked on the payment integration?"*

Results ranked by relevance with impact badges and developer attribution. Available on all plans.

### Automatic Documentation

Every push triggers Claude 4.5 to analyze your diff and generate or update:

- `README.md` — Project overview and usage
- `CHANGELOG.md` — Chronological change entries
- `docs/*.md` — Feature-specific documentation

Changes are delivered as a pull request on the `repoWrit/docs-update` branch. Review, merge, or ignore — you're always in control.

---

## Privacy & Trust

We take your code seriously.

| Commitment | Detail |
|---|---|
| **Zero Data Retention** | Your source code is processed in-memory by Claude 4.5 and discarded immediately. Nothing is stored. |
| **No Model Training** | Your code is never used to train any AI model. We use the Anthropic API with zero-retention settings. |
| **Minimal Permissions** | Read-only access to repository contents. Write access only for pull requests. |
| **Encryption** | TLS everywhere. Hosted on Vercel and Supabase with SOC 2-compliant infrastructure. |
| **Diffs Only** | We send only the commit diff to Claude — not your entire repository. |

Read our full [Privacy Policy](https://repowrit.com/privacy) and [Security Policy](https://github.com/RepoWrit/legal-and-security/blob/main/SECURITY.md).

---

## Plans

| | Hobby | Builder | Scale |
|---|---|---|---|
| **Price** | Free forever | $14.99/mo | $44.99/mo |
| **Doc Generations** | 5/month | Unlimited | Unlimited |
| **Executive Views** | Founder | Founder + PM | Founder + PM + CTO |
| **Architecture Maps** | — | — | ✓ |
| **PDF Export** | — | — | ✓ |
| **Analysis Window** | 24 hours | 48 hours | 7 days |
| **Concurrency** | 1 job | 3 jobs | 10 jobs |
| **Queue Priority** | Standard | Priority | Highest |

[Compare plans →](https://repowrit.com/pricing)

---

## Support

- **Bug reports** — [Open an issue](https://github.com/RepoWrit/repowrit/issues/new?template=bug_report.md)
- **Feature requests** — [Open an issue](https://github.com/RepoWrit/repowrit/issues/new?template=feature_request.md)
- **Email** — [support@repowrit.com](mailto:support@repowrit.com)
- **Security** — See [SECURITY.md](https://github.com/RepoWrit/legal-and-security/blob/main/SECURITY.md)

Builder and Scale customers receive priority support with guaranteed response times. See our [SLA](https://github.com/RepoWrit/legal-and-security/blob/main/SUPPORT.md).

---

## License

RepoWrit is a proprietary SaaS product. This repository serves as the community and support hub. The source code for the RepoWrit platform is not included here.

---

<p align="center">
  <sub>Built with conviction in India · Powered by Claude 4.5 · <a href="https://repowrit.com">repowrit.com</a></sub>
</p>
