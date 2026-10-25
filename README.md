# Hermes Web UI build helper

This public repository contains the GitHub Actions workflow and the small
public build inputs needed to reproduce the Hermes web UI build from the public
upstream repository.

- It does not contain Hermes source code, credentials, environment files, or
  user data.
- It includes the exact public web public assets (font files and background
  image) under `web-public-extra/`; neither contains credentials or personal
  data.
- The workflow checks out `NousResearch/hermes-agent` at a requested tag/ref,
  runs the public web build, and uploads the resulting `web_dist` artifact.
- The workflow has no `secrets.*` references and uses a read-only
  `GITHUB_TOKEN`.
- Artifacts are retained for one day.
