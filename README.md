# Review Workflows

Reusable advisory review workflows for arc-web repositories.

## Workflows

- `.github/workflows/pr-agent.yml`: runs PR-Agent/Qodo for AI PR review and slash-command responses.
- `.github/workflows/semgrep.yml`: runs Semgrep CE with `semgrep scan --config auto`.

## Required secret

Set `OPENAI_KEY` as an organization or repository Actions secret before enabling PR-Agent callers.

## Rollout policy

These workflows are advisory in v1. Semgrep uses `continue-on-error: true`; PR-Agent comments on pull requests but does not block merges.

Sources:

- https://qodo-merge-docs.qodo.ai/installation/github/
- https://semgrep.dev/docs/semgrep-ci/sample-ci-configs
