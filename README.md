### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 07 of 35** · branch `07-maps`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 07 — Maps

## 🎯 Learning goals
- Create maps with literals and `make`, and know why the zero value `nil` map panics on write.
- Do the four operations: insert, read, `delete`, and length.
- Use the comma-ok idiom (`v, ok := m[k]`) to distinguish "missing" from "zero value".
- Understand that iteration order is deliberately randomised, and how to iterate in sorted order.
- Know which types are valid map keys (comparable) and which are not (slices, maps, funcs).
- Model a set with `map[T]struct{}`, and use the `maps` package helpers.

## 📚 Resources
- [The Go Blog: Go maps in action](https://go.dev/blog/maps)
- [Go by Example: Maps](https://gobyexample.com/maps)
- [pkg.go.dev: maps](https://pkg.go.dev/maps)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Write a word-frequency counter for a paragraph of text using `map[string]int`.
- [ ] Print that map's keys in sorted order using `slices.Sorted(maps.Keys(m))`.
- [ ] Show the difference between a missing key and a key set to zero using the comma-ok idiom.
- [ ] Declare a `nil` map, read from it successfully, then write to it and read the panic message.
- [ ] Implement set union and intersection using `map[string]struct{}`.

---

⬅️ **Prev:** [06 · Arrays & Slices](https://github.com/DulsaraNethmin/go-notebook/tree/06-arrays-and-slices)  **Next:** [08 · Strings, Runes & Bytes](https://github.com/DulsaraNethmin/go-notebook/tree/08-strings-runes-and-bytes) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
