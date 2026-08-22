### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 20 of 35** · branch `20-context`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 20 — Context

## 🎯 Learning goals
- Understand what `context.Context` is for: cancellation, deadlines, and request-scoped values.
- Create contexts with `Background`, `TODO`, `WithCancel`, `WithTimeout`, `WithDeadline`.
- Always `defer cancel()` — and understand the leak you get when you don't.
- React to cancellation with `<-ctx.Done()` and `ctx.Err()` in `select` loops.
- Follow the conventions: first parameter, named `ctx`, never stored in a struct.
- Use `context.WithValue` sparingly and only for request-scoped data, never for optional args.

## 📚 Resources
- [The Go Blog: Go Concurrency Patterns — Context](https://go.dev/blog/context)
- [pkg.go.dev: context](https://pkg.go.dev/context)
- [Go by Example: Context](https://gobyexample.com/context)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Write a worker that loops until `ctx.Done()` fires, and cancel it from `main` after 1 second.
- [ ] Give an HTTP request a 500ms timeout with `context.WithTimeout` and observe the failure when it's exceeded.
- [ ] Distinguish `context.Canceled` from `context.DeadlineExceeded` using `errors.Is` on `ctx.Err()`.
- [ ] Thread a request ID through two function calls with `context.WithValue` and a private key type.
- [ ] Chain a child context under a parent and prove cancelling the parent cancels the child.

---

⬅️ **Prev:** [19 · sync & atomic](https://github.com/DulsaraNethmin/go-notebook/tree/19-sync-and-atomic)  **Next:** [21 · File I/O & os](https://github.com/DulsaraNethmin/go-notebook/tree/21-file-io-and-os) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
