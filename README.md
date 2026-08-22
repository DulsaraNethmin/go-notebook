### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 33 of 35** · branch `33-profiling-and-optimization`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 33 — Profiling & Optimization

## 🎯 Learning goals
- Adopt the workflow: benchmark → profile → change one thing → re-benchmark → compare.
- Collect CPU, memory, block and mutex profiles via `go test -cpuprofile/-memprofile` and `net/http/pprof`.
- Read profiles with `go tool pprof`: `top`, `list`, `web`, and flat vs cumulative time.
- Use escape analysis (`-gcflags='-m'`) to understand and reduce heap allocations.
- Reduce allocations concretely: pre-size slices and maps, reuse buffers, consider `sync.Pool`.
- Find concurrency bugs with `-race` and understand GC behaviour with `GODEBUG=gctrace=1`.

## 📚 Resources
- [The Go Blog: Profiling Go Programs](https://go.dev/blog/pprof)
- [Diagnostics](https://go.dev/doc/diagnostics)
- [A Guide to the Go Garbage Collector](https://go.dev/doc/gc-guide)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Write a deliberately slow function, benchmark it, and capture a CPU profile with `-cpuprofile`.
- [ ] Use `go tool pprof` `top` and `list` to find the exact line burning the time.
- [ ] Capture a memory profile and cut allocations by pre-sizing a slice; prove it with `-benchmem`.
- [ ] Expose `net/http/pprof` on a running server and pull a live 30s CPU profile.
- [ ] Compare two benchmark runs with `benchstat` and only claim a win when it's statistically real.

---

⬅️ **Prev:** [32 · Reflection, unsafe & cgo](https://github.com/DulsaraNethmin/go-notebook/tree/32-reflection-unsafe-and-cgo)  **Next:** [34 · Build, embed & Tooling](https://github.com/DulsaraNethmin/go-notebook/tree/34-build-embed-and-tooling) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
