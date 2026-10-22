# go-bignum.github.io

The go-bignum landing page (Hugo), served at <https://go-bignum.github.io/>.
The documentation is at <https://go-bignum.github.io/docs/> (repository
[go-bignum/docs](https://github.com/go-bignum/docs)).

The layout is the go-* family template: `layouts/index.html` and the shared
design (stylesheet, theme toggle, fork ribbon, icons), imported as the Hugo
module `github.com/go-fleettools/landingkit` pinned in `go.mod`. `[params.brand]`
in `hugo.toml` is read from the logo's gradient:

```sh
go run github.com/go-fleettools/landingkit/cmd/landingkit brand static/img/logo.svg
hugo server
```

`bigfloat`, the one library of the organization, is shown as released v0.1.0, with a performance
line linking its `docs/perf.md` (every function at or below mpmath's time).

| Workflow | What |
| --- | --- |
| `hugo.yml` | builds on pull requests; builds and deploys to Pages on `main` |
| `ci.yml` | the site builds and names every repository; `go mod tidy` keeps the landingkit requirement |
| `links.yml` | every link and image of the built site resolves |

BSD-3-Clause.
