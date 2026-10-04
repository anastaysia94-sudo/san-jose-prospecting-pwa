# NEXT ACTIONS

Updated: 2026-10-04

## Smallest next execution block
1. Verify the current 450-prospect build, offline behavior, filters, evidence links, and preserved device progress; recover and commit missing source if the repository is still empty.
2. Run the relevant build/tests or workflow checks.
3. Record concrete proof: commit SHA, test/workflow result, deployment URL/status when applicable.
4. Update STATUS.md only after verification.

## Recovery follow-up (2026-10-04, PT)
1. Source recovered from the Drive zip (150 leads); confirm the Pages deploy at https://anastaysia94-sudo.github.io/san-jose-prospecting-pwa/ after merge.
2. On the phone that has the 450-lead version, use Settings > Export full backup, and commit the prospects data (no personal/secret data) if it should be canonical.
3. Close PR #2 (placeholder), which this restore supersedes.
4. The GitHub Actions Pages workflow is saved at `docs/pages-workflow.yml.txt` (it could not be pushed: the bot's token lacks `workflow` scope). Someone with `workflow` scope should add it as `.github/workflows/pages.yml` and switch Pages back to "GitHub Actions". Until then the site is published from the `gh-pages` branch (a copy of `dist/`), which must be refreshed by hand when `dist/` changes.
