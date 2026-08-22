### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 10 of 35** · branch `10-pointers`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 10 — Pointers

## 🎯 Learning goals
- Take an address with `&` and dereference with `*`, and read pointer types fluently.
- Understand that Go is always pass-by-value — pointers just make the copied value an address.
- Decide when to pass a pointer: mutation, large structs, or optionality.
- Know that `p.Field` auto-dereferences, so you rarely write `(*p).Field`.
- Understand `new(T)` vs `&T{}`, and the `nil` pointer and its panic.
- Understand escape analysis at a high level: why taking an address may move a value to the heap.

## 📚 Resources
- [A Tour of Go: Pointers](https://go.dev/tour/moretypes/1)
- [Go by Example: Pointers](https://gobyexample.com/pointers)
- [Go FAQ: Should I define methods on values or pointers?](https://go.dev/doc/faq#methods_on_values_or_pointers)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Write `zero(x *int)` that sets its target to 0, and prove a value-parameter version can't.
- [ ] Trigger a nil-pointer dereference panic on purpose and read the stack trace carefully.
- [ ] Use a `*string` field to represent "unset" vs "empty string" in a config struct.
- [ ] Show that `&T{}` and `new(T)` produce the same thing by printing both with `%+v` and `%T`.
- [ ] Run `go build -gcflags='-m' .` on a small file and find one value the compiler moved to the heap.

---

⬅️ **Prev:** [09 · Structs](https://github.com/DulsaraNethmin/go-notebook/tree/09-structs)  **Next:** [11 · Methods](https://github.com/DulsaraNethmin/go-notebook/tree/11-methods) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
