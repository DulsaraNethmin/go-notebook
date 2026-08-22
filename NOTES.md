# 34 — Build, embed & Tooling

## 🎯 Learning goals
- Use build constraints (`//go:build`) to compile different code per OS, arch, or custom tag.
- Cross-compile with `GOOS`/`GOARCH`, and know what `CGO_ENABLED=0` buys you.
- Embed files and directories into the binary with `//go:embed` and `embed.FS`.
- Inject version info at build time with `-ldflags "-X main.version=..."`, and trim binaries with `-s -w`.
- Generate code with `//go:generate` and understand when generation beats reflection.
- Keep the codebase honest with `go vet`, `staticcheck`/`golangci-lint`, and `go mod verify`.

## 📚 Resources
- [pkg.go.dev: embed](https://pkg.go.dev/embed)
- [Go command documentation — build constraints](https://pkg.go.dev/cmd/go#hdr-Build_constraints)
- [The Go Blog: Generating code](https://go.dev/blog/generate)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Embed an HTML template and a static folder with `//go:embed` and serve them from an HTTP handler.
- [ ] Write two files with `//go:build linux` and `//go:build darwin` and confirm only one compiles.
- [ ] Cross-compile a Linux/amd64 binary from your Mac with `GOOS=linux GOARCH=amd64 go build`.
- [ ] Inject a version string with `-ldflags -X` and print it from a `-version` flag.
- [ ] Run `go vet ./...` and `golangci-lint run` on an earlier topic's code and fix everything they report.
