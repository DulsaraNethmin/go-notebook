# 16 — Goroutines

## 🎯 Learning goals
- Start a goroutine with `go f()` and understand it's a few KB of stack, not an OS thread.
- Understand the scheduler at a working level: G/M/P, `GOMAXPROCS`, preemption.
- Wait for goroutines with `sync.WaitGroup` — `Add` before `go`, `Done` in a `defer`.
- Understand that `main` returning kills every goroutine, no matter what they're doing.
- Recognise data races, and find them with `go run -race` / `go test -race`.
- Know that goroutines leak if nobody ever signals them to stop.

## 📚 Resources
- [A Tour of Go: Goroutines](https://go.dev/tour/concurrency/1)
- [Go by Example: WaitGroups](https://gobyexample.com/waitgroups)
- [The Go Blog: Introducing the Go Race Detector](https://go.dev/blog/race-detector)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Launch 5 goroutines that print their index, run it several times, and note the ordering changes.
- [ ] Show the "main exits first" problem, then fix it properly with a `WaitGroup`.
- [ ] Write a deliberate data race (unsynchronised `counter++` in 100 goroutines) and catch it with `-race`.
- [ ] Fix that race with a mutex, then re-run under `-race` to confirm it's clean.
- [ ] Spawn a goroutine blocked forever on a channel and observe the leak with `runtime.NumGoroutine()`.
