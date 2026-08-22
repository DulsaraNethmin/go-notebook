# 06 — Arrays & Slices

## 🎯 Learning goals
- Understand arrays as fixed-size value types, and why they're rare in idiomatic Go.
- Understand the slice header: pointer, length, capacity — and what `len` vs `cap` really report.
- Use `append` and know exactly when it reallocates the backing array and when it doesn't.
- Slice with `s[a:b]` and `s[a:b:c]`, and understand aliasing of the shared backing array.
- Copy safely with `copy`, and know how to delete/insert elements idiomatically.
- Use the modern `slices` package (`slices.Sort`, `slices.Contains`, `slices.Clone`).

## 📚 Resources
- [The Go Blog: Go Slices — usage and internals](https://go.dev/blog/slices-intro)
- [Go by Example: Slices](https://gobyexample.com/slices)
- [pkg.go.dev: slices](https://pkg.go.dev/slices)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Append to a slice in a loop and print `len`/`cap` each time — record the growth pattern you observe.
- [ ] Demonstrate the aliasing trap: slice a slice, mutate the sub-slice, and show the original changed too.
- [ ] Fix that same trap two ways: with `copy` into a fresh slice and with a full slice expression `s[a:b:c]`.
- [ ] Write `remove(s []int, i int) []int` that deletes an element without leaking the old tail value.
- [ ] Pass an array and a slice to a function that mutates them, and explain why only one change is visible.
