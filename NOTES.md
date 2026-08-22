# 09 — Structs

## 🎯 Learning goals
- Define struct types and create values with field-name literals (and why positional literals are fragile).
- Understand that structs are value types: assignment and passing copy the whole struct.
- Use anonymous structs and nested structs where a named type would be overkill.
- Use embedding to promote fields and methods — Go's composition instead of inheritance.
- Read and write struct tags, and know that they're just metadata read via reflection.
- Know when a struct is comparable with `==` and when it isn't.

## 📚 Resources
- [A Tour of Go: Structs](https://go.dev/tour/moretypes/2)
- [Go by Example: Structs](https://gobyexample.com/structs)
- [Effective Go: Embedding](https://go.dev/doc/effective_go#embedding)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Define a `Person` struct, pass it to a function that mutates a field, and show the caller is unaffected.
- [ ] Embed an `Address` struct in `Person` and access a promoted field directly as `p.City`.
- [ ] Add `json:"..."` tags to a struct and marshal it — confirm the output key names changed.
- [ ] Compare two structs with `==`, then add a slice field and watch it stop compiling.
- [ ] Build a small slice of anonymous structs as table-test data for some function you wrote earlier.
