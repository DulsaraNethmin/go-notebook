# 26 — Benchmarking & Fuzzing

## 🎯 Learning goals
- Write `BenchmarkXxx(b *testing.B)` and run it with `go test -bench=. -benchmem`.
- Read benchmark output: ns/op, B/op, allocs/op — and know which one usually matters.
- Use `b.Loop()` (or the classic `b.N` loop) correctly, and `b.ResetTimer` for setup you don't want measured.
- Avoid the compiler optimising your benchmark away by assigning to a package-level sink.
- Write fuzz tests with `FuzzXxx(f *testing.F)`, seed a corpus, and let the fuzzer find crashers.
- Compare before/after runs with `benchstat` rather than eyeballing single numbers.

## 📚 Resources
- [pkg.go.dev: testing — Benchmarks](https://pkg.go.dev/testing#hdr-Benchmarks)
- [Go Fuzzing documentation](https://go.dev/doc/fuzz/)
- [Tutorial: Getting started with fuzzing](https://go.dev/doc/tutorial/fuzz)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Benchmark string concatenation with `+=` vs `strings.Builder` and record the ns/op and allocs/op.
- [ ] Benchmark `append` with and without a pre-sized `make([]T, 0, n)` and quantify the difference.
- [ ] Use `b.ResetTimer()` after an expensive setup step and show the number change.
- [ ] Write a fuzz test for your rune-reverser from topic 08 and let it run for 30 seconds.
- [ ] Fix whatever the fuzzer finds, and confirm the failing input got saved into `testdata/fuzz/`.
