# 32 — Reflection, unsafe & cgo

## 🎯 Learning goals
- Understand the laws of reflection: interface ↔ `reflect.Value`/`reflect.Type`, and what "settable" means.
- Inspect structs at runtime: iterate fields, read types, and read struct tags via `Field.Tag.Get`.
- Modify values through reflection, and know why you need `reflect.ValueOf(&x).Elem()`.
- Know reflection's real costs: no compile-time safety, poor performance, unreadable code.
- Understand what `unsafe.Pointer` and `unsafe.Sizeof` do, and the rules you must not break.
- Call C from Go with cgo, and understand why "cgo is not Go" (build cost, cross-compilation, GC boundary).

## 📚 Resources
- [The Go Blog: The Laws of Reflection](https://go.dev/blog/laws-of-reflection)
- [pkg.go.dev: reflect](https://pkg.go.dev/reflect)
- [cgo documentation](https://pkg.go.dev/cmd/cgo)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Write a function that prints every field name, type and value of any struct passed as `any`.
- [ ] Read a custom struct tag (e.g. `validate:"required"`) and build a tiny validator on top of it.
- [ ] Set a struct field through reflection, and reproduce the panic you get without a pointer.
- [ ] Print `unsafe.Sizeof` for a few structs and reorder fields to shrink one through better alignment.
- [ ] Write a minimal cgo program calling a C function, then time `go build` with and without cgo.
