# 15 — io & Standard Interfaces

## 🎯 Learning goals
- Understand `io.Reader` and `io.Writer` as the universal plumbing of the Go standard library.
- Implement your own `Reader`/`Writer` and honour the `Read` contract (n, err, `io.EOF`).
- Use the composition helpers: `io.Copy`, `io.TeeReader`, `io.MultiWriter`, `io.LimitReader`.
- Use `strings.NewReader`, `bytes.Buffer` and `io.Discard` to make code trivially testable.
- Implement `fmt.Stringer`, `sort.Interface`, and `io.Closer` where they fit.
- Know the standard interface-naming convention (`-er` suffix) and why interfaces stay tiny.

## 📚 Resources
- [pkg.go.dev: io](https://pkg.go.dev/io)
- [Effective Go: Interfaces and methods](https://go.dev/doc/effective_go#interface_methods)
- [Go by Example: Reading Files](https://gobyexample.com/reading-files)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Copy from `strings.NewReader` to `os.Stdout` with `io.Copy` in a single line.
- [ ] Write an `UpperWriter` implementing `io.Writer` that upper-cases everything before forwarding it.
- [ ] Use `io.MultiWriter` to write the same output to a file and to stdout at once.
- [ ] Implement `sort.Interface` for a `ByAge []Person` type, then rewrite it with `slices.SortFunc`.
- [ ] Refactor a function that took a filename to take an `io.Reader`, and unit-test it with a `bytes.Buffer`.
