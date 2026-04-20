# Go Package Scaffold

Generate boilerplate code for a new Go library package.

## Features

- Minimal opinions — just a package stub (`doc.go`) and CI plumbing
- `mise.toml` for tool versioning and common tasks (test, lint, fmt, coverage)
- GolangCI-Lint (v2) configuration with gofumpt formatter
- Optional GitHub Actions for PR testing
- Optional goreleaser config (library mode) + manual-bump release workflow
- Optional Renovate configuration

## Usage

```sh
scaffold new github.com/hay-kot/scaffold-go-pkg
```

## Development

This repo uses [mise](https://mise.jdx.dev/) to pin tools and expose tasks:

```sh
mise run test:snapshot         # diff committed snapshot vs. fresh render
mise run test:snapshot:update  # regenerate the committed snapshot
mise run test:run              # render + `go build` + `go test` the output
mise run update:deps           # refresh template go.mod/go.sum
mise run update:actions        # bump GitHub Action major versions
```
