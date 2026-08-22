# 22 — JSON & Encoding

## 🎯 Learning goals
- Marshal and unmarshal with `json.Marshal` / `json.Unmarshal`, and stream with `Encoder`/`Decoder`.
- Control the wire format with struct tags: renaming, `omitempty`, `-`, and `string`.
- Understand why only exported fields are encoded.
- Decode unknown shapes into `map[string]any` and navigate them with type assertions.
- Implement `json.Marshaler` / `json.Unmarshaler` for custom types like durations or enums.
- Handle nested structs, slices, pointers-for-optional, and `json.RawMessage` for deferred decoding.

## 📚 Resources
- [The Go Blog: JSON and Go](https://go.dev/blog/json)
- [pkg.go.dev: encoding/json](https://pkg.go.dev/encoding/json)
- [Go by Example: JSON](https://gobyexample.com/json)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Round-trip a nested struct through JSON and diff the result against the original.
- [ ] Lower-case a struct field and watch it vanish from the JSON output — then explain why.
- [ ] Use `omitempty` and a pointer field to tell "absent" apart from "zero".
- [ ] Implement `MarshalJSON`/`UnmarshalJSON` on a `type Status int` so it serialises as a string.
- [ ] Decode an arbitrary JSON blob into `map[string]any` and safely extract a nested value.
