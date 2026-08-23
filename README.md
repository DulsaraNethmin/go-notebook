### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 01 of 35** · branch `01-setup-and-hello-world`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 01 — Setup & Hello World

## 🎯 Learning goals
- Install the Go toolchain and understand what `GOROOT`, `GOPATH` and the module cache actually are.
- Write and run a first program: `package main`, `func main()`, `fmt.Println`.
- Know the difference between `go run`, `go build` and `go install`.
- Create a first module with `go mod init` and understand what `go.mod` records.
- Format code with `gofmt`/`go fmt` and accept that formatting is not up for debate in Go.
- Find your way around `go help`, `go doc` and pkg.go.dev.

## 📚 Resources
- [Download and install Go](https://go.dev/doc/install)
- [Tutorial: Get started with Go](https://go.dev/doc/tutorial/getting-started)
- [Go by Example: Hello World](https://gobyexample.com/hello-world)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ✅] Install Go, run `go version` and `go env`, and note where the module cache lives.
- [ ✅] Create a module `hello` with `go mod init` and write a Hello World that prints your name.
- [ ✅] Build a binary with `go build`, run it directly, then compare with `go run .` — note what artefact each leaves behind.
- [ ] Deliberately mis-format a file (bad indentation, extra blank lines), then fix it with `gofmt -w`.
- [ ] Use `go doc fmt.Println` from the terminal and read the docs without opening a browser.

---

**Next:** [02 · Variables, Constants & Types](https://github.com/DulsaraNethmin/go-notebook/tree/02-variables-constants-and-types) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
