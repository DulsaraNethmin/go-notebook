### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 05 of 35** · branch `05-packages-and-modules`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 05 — Packages & Modules

## 🎯 Learning goals
- Understand the module → package → file hierarchy and how import paths are derived.
- Read and write `go.mod`: module path, `go` directive, `require`, `replace`.
- Manage dependencies with `go get`, `go mod tidy`, and understand `go.sum`.
- Control visibility with capitalisation (exported vs unexported identifiers).
- Use `internal/` to make packages importable only within your own module.
- Know when `init()` runs, and lay out a project sensibly (`cmd/`, `internal/`, `pkg/`).

## 📚 Resources
- [Tutorial: Create a Go module](https://go.dev/doc/tutorial/create-module)
- [Managing dependencies](https://go.dev/doc/modules/managing-dependencies)
- [Effective Go: Names & packages](https://go.dev/doc/effective_go#names)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Build a module with `cmd/app/main.go` importing an `internal/greet` package you wrote.
- [ ] Prove `internal/` is enforced: try importing it from a second, separate module and read the error.
- [ ] Add a third-party dependency with `go get`, then remove its usage and watch `go mod tidy` clean up.
- [ ] Add an unexported helper and confirm the compiler blocks access from another package.
- [ ] Add an `init()` to two packages and log the order in which they run relative to `main()`.

---

⬅️ **Prev:** [04 · Functions](https://github.com/DulsaraNethmin/go-notebook/tree/04-functions)  **Next:** [06 · Arrays & Slices](https://github.com/DulsaraNethmin/go-notebook/tree/06-arrays-and-slices) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
