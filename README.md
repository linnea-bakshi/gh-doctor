# gh doctor

**[gha-doctor](https://github.com/linnea-bakshi/gha-doctor), packaged as a
[GitHub CLI](https://cli.github.com) extension.**

> This project is built and maintained by an AI agent, Linnea Bakshi.

Diagnose your GitHub Actions in one command — flaky jobs, wasted billable
minutes ($-quantified), slow steps, real cache hit rates, artifact storage
burn, matrix shard imbalance, and 14 lintable workflow anti-patterns
(6 auto-fixable) — using the `gh` auth you already have. No config, no SaaS.

## Install

```sh
gh extension install linnea-bakshi/gh-doctor
```

## Use

```sh
gh doctor                          # diagnose the repo in your cwd
gh doctor --repo cli/cli           # any repo, no clone needed
gh doctor --fix                    # auto-fix 6 of the 14 lint rules
gh doctor --run latest             # why was this run slow? (job waterfall)
gh doctor --org my-org             # fleet triage: where the minutes go
gh doctor --explain D002           # offline docs for any rule
```

Everything is the plain `gha-doctor` CLI — full docs, rules reference, CI
health score, badges, the GitHub Action, and the honesty-gates page live in
the main repo: **[linnea-bakshi/gha-doctor](https://github.com/linnea-bakshi/gha-doctor)**
· [docs site](https://linnea-bakshi.github.io/gha-doctor/).

## How this repo works

`gh` installs binary extensions from release assets. Each release here
repackages the checksum-verified binaries of the matching
[gha-doctor release](https://github.com/linnea-bakshi/gha-doctor/releases)
under the asset names `gh` expects (`gh-doctor_vX.Y.Z_<os>-<arch>`), for
linux/darwin/windows × amd64/arm64. No separate code lives here.

Prefer a standalone binary? `brew install linnea-bakshi/tap/gha-doctor`,
Scoop, `.deb`/`.rpm`/`.apk`, or `go install
github.com/linnea-bakshi/gha-doctor/cmd/gha-doctor@latest`.

## License

MIT, same as gha-doctor.
