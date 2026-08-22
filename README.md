### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 08 of 35** · branch `08-strings-runes-and-bytes`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 08 — Strings, Runes & Bytes

## 🎯 Learning goals
- Understand that a Go string is an immutable, read-only slice of bytes holding UTF-8.
- Know the difference between indexing a string (bytes) and ranging over it (runes).
- Convert between `string`, `[]byte` and `[]rune`, and know which conversions allocate.
- Use the `strings` package: `Split`, `Join`, `Contains`, `TrimSpace`, `Fields`, `Replace`, `Cut`.
- Convert to and from numbers with `strconv`, and handle the errors properly.
- Build strings efficiently with `strings.Builder` instead of `+=` in a loop.

## 📚 Resources
- [The Go Blog: Strings, bytes, runes and characters in Go](https://go.dev/blog/strings)
- [pkg.go.dev: strings](https://pkg.go.dev/strings)
- [Go by Example: String Functions](https://gobyexample.com/string-functions)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Take a string with emoji or accented characters and print `len(s)` vs `utf8.RuneCountInString(s)`.
- [ ] Print `s[0]` and the first value from `range s` for the same non-ASCII string, and explain the difference.
- [ ] Write a rune-correct string reverser and test it on "héllo 🌍".
- [ ] Benchmark-by-eye: build a 10k-word string with `+=` and with `strings.Builder`, and time both.
- [ ] Parse user input with `strconv.Atoi`/`ParseFloat` and handle the error path rather than ignoring it.

---

⬅️ **Prev:** [07 · Maps](https://github.com/DulsaraNethmin/go-notebook/tree/07-maps)  **Next:** [09 · Structs](https://github.com/DulsaraNethmin/go-notebook/tree/09-structs) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
