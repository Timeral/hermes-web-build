# Hermes Web UI build helper

This public repository contains only the GitHub Actions workflow used to build
the Hermes web UI from the public upstream repository.

- It does not contain Hermes source code, credentials, environment files, or
  user data.
- The workflow checks out `NousResearch/hermes-agent` at a requested tag/ref,
  runs the public web build, and uploads the resulting `web_dist` artifact.
- The workflow has no `secrets.*` references and uses a read-only
  `GITHUB_TOKEN`.
- Artifacts are retained for one day.
