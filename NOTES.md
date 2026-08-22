# 02 — Variables, Constants & Types

## 🎯 Learning goals
- Declare values with `var`, short declaration `:=`, and grouped `var (...)` blocks — and know where each is legal.
- Understand zero values and why Go has no "uninitialised" variables.
- Use the basic types: `int`/`int64`/`uint`, `float64`, `bool`, `string`, `byte`, `rune`.
- Work with `const`, typed vs untyped constants, and `iota` for enum-like sets.
- Convert between types explicitly (`int64(x)`, `float64(n)`) and know why Go refuses implicit conversion.
- Understand scope and shadowing, and why an unused variable is a compile error.

## 📚 Resources
- [A Tour of Go: Basics](https://go.dev/tour/basics/1)
- [Go by Example: Variables](https://gobyexample.com/variables)
- [The Go Blog: Constants](https://go.dev/blog/constants)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Declare one variable of every basic type without initialising it and print all the zero values.
- [ ] Write an `iota`-based enum for weekdays, plus a `String()`-free helper that maps values to names.
- [ ] Trigger the "declared and not used" compile error on purpose, then fix it with `_`.
- [ ] Show integer division truncation (`7/2`) vs float division, and convert between them explicitly.
- [ ] Shadow a variable inside an `if` block, print both, and explain in your notes which one wins where.
