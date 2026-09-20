# Marketing Skills — synchronized reference

**[Open the marketing skills on the `main` branch](https://github.com/Elevation-Business-OS/marketingskills/tree/main)**

This fork follows [Corey Haines's Marketing Skills](https://github.com/coreyhaines31/marketingskills). The original skills retain their MIT license and attribution. `main` is the source branch; clone it explicitly:

```sh
git clone --branch main https://github.com/Elevation-Business-OS/marketingskills.git
```

The default `codex/automation` branch contains only our independent sync workflow and its latest successful check. Keeping the scheduler here lets `main` match upstream without local workflow commits. No upstream installer, script or workflow is run by the sync.

- Weekly check: Mondays, 07:17 Europe/Dublin; GitHub may delay scheduled starts.
- [Run history and manual Run workflow button](https://github.com/Elevation-Business-OS/marketingskills/actions/workflows/sync-upstream.yml).
- [Latest successful check](.sync/last-success.json).
- A divergent `main` causes a failed run; it is never force-reset.
- Existing reference material remains usable if a check is late or fails.

GitHub hosts the job. It does not require a local computer, Codex session or AI API key. It uses the short-lived repository-scoped `GITHUB_TOKEN`; no personal access token is stored. A small success record is committed to `codex/automation` each run, including when upstream is unchanged. This maintains an audit trail and repository activity during quiet upstream periods. Failure visibility uses GitHub Actions run status and the account's existing notification preferences.
