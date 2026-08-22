### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 23 of 35** · branch `23-time-and-scheduling`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 23 — Time & Scheduling

## 🎯 Learning goals
- Work with `time.Time`, `time.Duration`, and the arithmetic between them (`Add`, `Sub`, `Since`).
- Master the reference-time layout (`2006-01-02 15:04:05`) for `Format` and `Parse`.
- Handle time zones and `time.Location`, and default to UTC for anything stored or transmitted.
- Use `time.Sleep`, `time.After`, `time.NewTimer` and `time.NewTicker` — and stop tickers.
- Compare instants correctly (`Before`/`After`/`Equal`, never `==`) and use monotonic time for durations.
- Make time-dependent code testable by injecting a clock instead of calling `time.Now()` directly.

## 📚 Resources
- [pkg.go.dev: time](https://pkg.go.dev/time)
- [Go by Example: Time Formatting / Parsing](https://gobyexample.com/time-formatting-parsing)
- [Go by Example: Tickers](https://gobyexample.com/tickers)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Format `time.Now()` five different ways, including RFC3339, using the reference layout.
- [ ] Parse "2026-08-22T10:30:00Z" and add 90 minutes to it.
- [ ] Run a ticker every 200ms, stop it after 5 ticks with `defer ticker.Stop()`.
- [ ] Measure a function's runtime with `time.Since(start)` and print it as a `Duration`.
- [ ] Refactor a function that calls `time.Now()` internally to accept a `now func() time.Time` and test it.

---

⬅️ **Prev:** [22 · JSON & Encoding](https://github.com/DulsaraNethmin/go-notebook/tree/22-json-and-encoding)  **Next:** [24 · Logging & slog](https://github.com/DulsaraNethmin/go-notebook/tree/24-logging-and-slog) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
