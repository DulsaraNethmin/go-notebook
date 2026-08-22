### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 04 of 35** · branch `04-functions`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 04 — Functions

## 🎯 Learning goals
- Declare functions with multiple return values and use the `(T, error)` convention.
- Understand named return values and when they help vs when they hide bugs.
- Write variadic functions and expand a slice into them with `slice...`.
- Treat functions as values: parameters, returns, and function types.
- Build closures that capture variables, and understand what "capture" actually means.
- Use `defer` for cleanup, know its LIFO order, and know when arguments are evaluated.

## 📚 Resources
- [A Tour of Go: More types & functions](https://go.dev/tour/moretypes/24)
- [Go by Example: Closures](https://gobyexample.com/closures)
- [The Go Blog: Defer, Panic, and Recover](https://go.dev/blog/defer-panic-and-recover)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Write `divide(a, b float64) (float64, error)` that returns an error on division by zero.
- [ ] Write a variadic `sum(nums ...int) int` and call it both with literal args and with `nums...`.
- [ ] Build a counter closure factory: `makeCounter() func() int` where each counter is independent.
- [ ] Stack three `defer`s in one function and predict the output order before running it.
- [ ] Show that `defer fmt.Println(x)` captures `x` at defer time, but `defer func(){ fmt.Println(x) }()` does not.

---

⬅️ **Prev:** [03 · Control Flow](https://github.com/DulsaraNethmin/go-notebook/tree/03-control-flow)  **Next:** [05 · Packages & Modules](https://github.com/DulsaraNethmin/go-notebook/tree/05-packages-and-modules) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
