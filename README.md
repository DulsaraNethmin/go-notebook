### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 12 of 35** · branch `12-interfaces`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 12 — Interfaces

## 🎯 Learning goals
- Understand implicit satisfaction: no `implements` keyword, structural typing at compile time.
- Design small interfaces ("accept interfaces, return structs") and know why one-method interfaces win.
- Use type assertions (`v, ok := x.(T)`) and type switches safely.
- Understand `any`, and the empty interface's cost in readability.
- Understand the (type, value) pair inside an interface — and the nil-interface-holding-nil-pointer trap.
- Embed interfaces to compose bigger ones, and assert satisfaction at compile time with `var _ I = (*T)(nil)`.

## 📚 Resources
- [A Tour of Go: Interfaces](https://go.dev/tour/methods/9)
- [Effective Go: Interfaces](https://go.dev/doc/effective_go#interfaces)
- [The Go Blog: The Laws of Reflection (interface internals)](https://go.dev/blog/laws-of-reflection)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Define a `Shape` interface with `Area()`, implement it for `Circle` and `Rect`, and total a `[]Shape`.
- [ ] Write a function taking `any` and using a type switch to describe what it received.
- [ ] Reproduce the nil-interface trap: return a nil `*MyError` as an `error` and show `err != nil`.
- [ ] Add `var _ Shape = (*Circle)(nil)` and break the implementation to see the compile-time check fire.
- [ ] Refactor a function that took a concrete `*os.File` to take an `io.Writer` instead, and test it with a buffer.

---

⬅️ **Prev:** [11 · Methods](https://github.com/DulsaraNethmin/go-notebook/tree/11-methods)  **Next:** [13 · Error Handling](https://github.com/DulsaraNethmin/go-notebook/tree/13-error-handling) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
