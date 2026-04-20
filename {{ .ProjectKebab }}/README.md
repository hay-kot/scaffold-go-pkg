{{- $slug := trimPrefix "github.com/" .Scaffold.gomod -}}
# {{ .Project }}

{{ .Scaffold.description }}

[![Go Reference](https://pkg.go.dev/badge/{{ .Scaffold.gomod }}.svg)](https://pkg.go.dev/{{ .Scaffold.gomod }})
{{- if .Computed.feature_gh_actions }}
[![CI](https://github.com/{{ $slug }}/actions/workflows/pr.yml/badge.svg)](https://github.com/{{ $slug }}/actions/workflows/pr.yml)
{{- end }}
[![License](https://img.shields.io/github/license/{{ $slug }})](./LICENSE)

## Install

```bash
go get {{ .Scaffold.gomod }}
```

## Usage

TODO
