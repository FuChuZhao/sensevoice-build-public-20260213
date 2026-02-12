# SenseVoice Build Repo (Public)

Public repository that only contains workflow definitions.

## Security model

- `on: workflow_dispatch` only
- minimal permissions (`contents: read`)
- source code is cloned from private SOURCE_REPO via read-only deploy key
- artifacts uploaded with `retention-days: 1`

## Required setup

Repository variable:

- `SOURCE_REPO` (format: `owner/private-source-repo`)

Repository secret:

- `SOURCE_REPO_SSH_KEY` (private key for read-only deploy key configured in SOURCE_REPO)

## Workflow inputs

- `source_ref`
- `artifact_name`
- `runner`
- `preset_name`
- `repeat`
- `max_wavs`
- `scenario_label`
- `ui_app`

