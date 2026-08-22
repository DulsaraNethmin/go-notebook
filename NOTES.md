# 19 — sync & atomic

## 🎯 Learning goals
- Protect shared state with `sync.Mutex`, and unlock with `defer` so early returns can't strand the lock.
- Use `sync.RWMutex` when reads massively outnumber writes, and know its cost.
- Run one-time initialisation with `sync.Once`.
- Use `sync/atomic` types (`atomic.Int64`, `atomic.Value`) for simple counters and flags.
- Use `golang.org/x/sync/errgroup` to run concurrent tasks that can fail.
- Know when to reach for a mutex and when a channel is the better answer.

## 📚 Resources
- [pkg.go.dev: sync](https://pkg.go.dev/sync)
- [Go by Example: Mutexes](https://gobyexample.com/mutexes)
- [pkg.go.dev: errgroup](https://pkg.go.dev/golang.org/x/sync/errgroup)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Build a `SafeCounter` struct embedding a mutex, hammer it from 100 goroutines, verify under `-race`.
- [ ] Rewrite that counter with `atomic.Int64` and compare the code and the speed.
- [ ] Copy a struct containing a `sync.Mutex` by value and let `go vet` tell you off.
- [ ] Use `sync.Once` to lazily initialise an expensive singleton called from many goroutines.
- [ ] Fetch 3 URLs concurrently with `errgroup` and make sure one failure cancels the rest.
