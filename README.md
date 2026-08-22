### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 14 of 35** · branch `14-generics`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 14 — Generics

## 🎯 Learning goals
- Write generic functions with type parameters: `func Map[T, U any](s []T, f func(T) U) []U`.
- Use constraints: `any`, `comparable`, `cmp.Ordered`, and interface-based union constraints.
- Define your own constraint interfaces with type sets (`~int | ~float64`) and understand `~`.
- Declare generic types (a `Stack[T]`, a `Set[T]`) and their methods.
- Rely on type inference, and know when you must instantiate explicitly.
- Judge when generics are the right tool versus interfaces, and when they just add noise.

## 📚 Resources
- [Tutorial: Getting started with generics](https://go.dev/doc/tutorial/generics)
- [The Go Blog: When To Use Generics](https://go.dev/blog/when-generics)
- [Go by Example: Generics](https://gobyexample.com/generics)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Write generic `Map`, `Filter` and `Reduce` over slices.
- [ ] Write `Max[T cmp.Ordered](a, b T) T` and call it with ints, floats and strings.
- [ ] Implement a generic `Stack[T]` with `Push`, `Pop` and `Len`.
- [ ] Write a constraint using `~int | ~string` and use it with a defined type like `type ID int`.
- [ ] Take one generic function you wrote and rewrite it with an interface — note in your notes which you'd ship.

---

⬅️ **Prev:** [13 · Error Handling](https://github.com/DulsaraNethmin/go-notebook/tree/13-error-handling)  **Next:** [15 · io & Standard Interfaces](https://github.com/DulsaraNethmin/go-notebook/tree/15-io-and-standard-interfaces) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
