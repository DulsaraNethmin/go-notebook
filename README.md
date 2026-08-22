### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 24 of 35** · branch `24-logging-and-slog`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 24 — Logging & slog

## 🎯 Learning goals
- Know what the old `log` package gives you and where it runs out (`log.Fatal`, `log.Printf`).
- Use `log/slog` for structured logging with key/value attributes instead of formatted strings.
- Choose a handler: `slog.NewTextHandler` for humans, `slog.NewJSONHandler` for machines.
- Set levels (Debug/Info/Warn/Error) via `slog.HandlerOptions` and control verbosity at runtime.
- Attach persistent context with `logger.With(...)` and group attributes.
- Understand why you log errors once, at the top, rather than at every layer.

## 📚 Resources
- [pkg.go.dev: log/slog](https://pkg.go.dev/log/slog)
- [The Go Blog: Structured Logging with slog](https://go.dev/blog/slog)
- [Go by Example: Logging](https://gobyexample.com/logging)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Log the same event with `log.Printf` and with `slog.Info` + attributes, and compare the output.
- [ ] Configure a JSON handler writing to stdout at `LevelDebug` and log one line at each level.
- [ ] Use `logger.With("request_id", id)` and confirm the field appears on every subsequent line.
- [ ] Set the default logger with `slog.SetDefault` and log from another package without passing it around.
- [ ] Log an error with `slog.Any("err", err)` and check how a wrapped error renders.

---

⬅️ **Prev:** [23 · Time & Scheduling](https://github.com/DulsaraNethmin/go-notebook/tree/23-time-and-scheduling)  **Next:** [25 · Testing](https://github.com/DulsaraNethmin/go-notebook/tree/25-testing) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
