# hassioaddon

## Roles

Ask-first repository (public, and tracks an `upstream` remote). Workers never
commit or push; they leave the working tree changed and write a report for the
maintainer to review and push. Never rewrite history — it would break the
upstream-tracking relationship.

## What this is

A Home Assistant add-on repository (forked from `bytenoodle/hassioaddon`),
installable in HA Supervisor via the repository URL in README.md. It bundles
three add-ons: Homepage (start page), Spoolman (filament inventory web UI), and
Bambulab-ams-spoolman (syncs a Bambu AMS with Spoolman).

## Key facts

- Each add-on lives in its own top-level directory (`homepage/`, `spoolman/`,
  `Bambulab-ams-spoolman/`) with its own config/Dockerfile.
- No CI workflows are configured in this repo (`.github/workflows/` does not
  exist) — changes are validated manually.
- `repository.yaml` still lists the pre-fork maintainer/URL — known, not yet
  updated; leave it unless asked.

## Guardrails

- Fork updates from `upstream` should be merged, not rebased, to keep history
  intact for both remotes.
