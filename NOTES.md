# 13 — Error Handling

## 🎯 Learning goals
- Internalise the `if err != nil` convention: errors are values, returned last, handled explicitly.
- Create errors with `errors.New` and `fmt.Errorf`, and add context without losing the original.
- Wrap with `%w` and unwrap with `errors.Is` (sentinel matching) and `errors.As` (type extraction).
- Define custom error types implementing the `error` interface, with an `Unwrap()` where useful.
- Know when to `panic`, how `recover` works inside a `defer`, and why libraries shouldn't panic.
- Write error messages the Go way: lowercase, no punctuation, no "failed to" pile-ups.

## 📚 Resources
- [The Go Blog: Working with Errors in Go 1.13](https://go.dev/blog/go1.13-errors)
- [Go by Example: Errors](https://gobyexample.com/errors)
- [pkg.go.dev: errors](https://pkg.go.dev/errors)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Define a sentinel `ErrNotFound`, wrap it two layers deep with `%w`, and match it with `errors.Is`.
- [ ] Write a `ValidationError` struct with a `Field` member and pull it back out with `errors.As`.
- [ ] Compare `%w` and `%v` in `fmt.Errorf` — show that only one keeps `errors.Is` working.
- [ ] Write a function that recovers from a panic and converts it into a returned error.
- [ ] Take some code that does `if err != nil { panic(err) }` and rewrite it to propagate the error properly.
