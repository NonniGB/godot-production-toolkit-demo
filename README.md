# Godot Production Toolkit Demo

A tiny Godot 4 fixture that shows how to run [Godot Production Toolkit](https://github.com/NonniGB/godot-production-toolkit) in GitHub Actions.

The project intentionally contains a few release-readiness warnings so the workflow produces useful JSON, Markdown, and HTML reports. It is not a game template; it is a small CI fixture for trying the tooling quickly.

## What The Workflow Runs

- Asset import checks for pixel-art settings.
- Android export preset checks.
- Input map coverage checks.
- Static mobile performance checks.

Reports are uploaded as a GitHub Actions artifact named `godot-doctor-reports`.

## Local Run

```powershell
godot-project-doctor run godot-project-doctor.toml --format markdown --output reports\summary.md
godot-project-doctor summarize reports\godot-project-doctor --format html --output reports\summary.html
```