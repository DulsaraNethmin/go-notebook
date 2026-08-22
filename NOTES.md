# 03 — Control Flow

## 🎯 Learning goals
- Use `if`/`else if`/`else`, including the `if err := f(); err != nil` statement form.
- Master `for` — Go's only loop: three-clause, condition-only ("while"), infinite, and `range`.
- Use `switch` with no condition, with multiple values per case, and with initialisers.
- Understand that Go cases don't fall through by default, and when `fallthrough` is right.
- Break and continue out of nested loops with labels.
- Know why `goto` exists and why you will almost never reach for it.

## 📚 Resources
- [A Tour of Go: Flow control](https://go.dev/tour/flowcontrol/1)
- [Go by Example: For](https://gobyexample.com/for)
- [Go by Example: Switch](https://gobyexample.com/switch)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Write FizzBuzz using a `switch` with no condition instead of if/else chains.
- [ ] Write the same loop four ways: three-clause, condition-only, infinite with `break`, and `range` over an int.
- [ ] Use a labelled `break` to escape a nested loop as soon as you find a target in a 2-D grid.
- [ ] Write a `switch` that classifies a number as negative/zero/small/large using an initialiser statement.
- [ ] Use `fallthrough` once, then rewrite the same logic without it and note which reads better.
