# tytsxai-stack org defaults

This repository provides organization-level defaults for `tytsxai-stack`:

- **`workflow-templates/`** — When you create a new repo and click "Actions → Set up a workflow", these templates appear as starting points. They're pre-configured to use the **self-hosted runner on hp-ubuntu** (`runs-on: [self-hosted, linux]`).

## How CI runs in this org

All CI in `tytsxai-stack` runs on a single self-hosted runner registered to the org level (one runner serves every repo). New private repos created in this org should use `runs-on: [self-hosted, linux]` rather than `ubuntu-latest`.

If you push a workflow with `runs-on: ubuntu-latest`, the job will fail to start (no GitHub-hosted runner is provisioned for this org).
