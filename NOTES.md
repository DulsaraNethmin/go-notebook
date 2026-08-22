# 11 — Methods

## 🎯 Learning goals
- Attach methods to your own named types with a receiver, including non-struct types.
- Choose between value and pointer receivers, and keep that choice consistent per type.
- Understand method sets: why `*T` has both, and why `T` only has value-receiver methods.
- Know when Go auto-takes an address (`v.PtrMethod()`) and when it can't (unaddressable values).
- Use method values and method expressions as first-class functions.
- Implement `String() string` and see `fmt` pick it up automatically.

## 📚 Resources
- [A Tour of Go: Methods](https://go.dev/tour/methods/1)
- [Go by Example: Methods](https://gobyexample.com/methods)
- [Effective Go: Pointers vs. Values](https://go.dev/doc/effective_go#pointers_vs_values)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Write a `Counter` type with `Inc()` on a pointer receiver and show a value receiver silently fails to increment.
- [ ] Define `type Celsius float64` with a `String()` method and print it with `fmt.Println`.
- [ ] Store a value of type `T` in a map and try calling a pointer-receiver method on it — read the compile error.
- [ ] Pass a method value (`c.Inc`) as a `func()` argument to another function.
- [ ] Write out, in your notes, the rule for which method set satisfies an interface — in your own words.
