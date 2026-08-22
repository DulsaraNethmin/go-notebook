# 18 — select & Concurrency Patterns

## 🎯 Learning goals
- Use `select` to wait on multiple channel operations, and understand its random choice among ready cases.
- Add timeouts with `time.After` and non-blocking sends/receives with `default`.
- Build a pipeline of stages connected by channels, each stage closing its own output.
- Implement fan-out (many workers on one input) and fan-in (merge many outputs into one).
- Build a worker pool with a jobs channel and a results channel.
- Use the done-channel / quit-channel idiom to shut everything down cleanly.

## 📚 Resources
- [The Go Blog: Go Concurrency Patterns — Pipelines and cancellation](https://go.dev/blog/pipelines)
- [Go by Example: Select](https://gobyexample.com/select)
- [Go by Example: Worker Pools](https://gobyexample.com/worker-pools)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Use `select` with `time.After` to give a slow operation a 100ms deadline.
- [ ] Write a non-blocking receive with `default` and show it doesn't wait on an empty channel.
- [ ] Build a 3-stage pipeline: generate → square → filter-even, each stage its own goroutine.
- [ ] Build a worker pool of 3 workers processing 10 jobs, collecting results in order-independent fashion.
- [ ] Write a `merge(chans ...<-chan int) <-chan int` fan-in that closes the output exactly once.
