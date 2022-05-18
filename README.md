# GitHub Actions - Deployments

> Test several options for deploying via GitHub Actions

This repository contains several test Actions for deploying via GitHub Actions (see [caveats](#caveats)).

## Actions

| Name                       | Type                | Description                                                                           |
| -------------------------- | ------------------- | ------------------------------------------------------------------------------------- |
| `code_quality`             | `pull_request:main` | Linting/tests on every PR into `main`                                                 |
| `deploy_production`\*      | `release`           | Code quality, with optional staging/production deployments, when publishing a release |
| `deploy_staging`\*         | `merge:main`        | Code quality, with optional staging deployment, on merges into `main`                 |
| `deploy_manual_production` | `manual`            | Manual deployment to staging                                                          |
| `deploy_manual_staging`    | `manual`            | Manual deployment to production                                                       |

_`*` indicates that Environments are used to require deployment approvals_

## Caveats

> **NOTE:** GitHub Environments are required to enable pausing deployments until reviewed; however, this option is only available in public repositories _or_ Enterprise plans!
