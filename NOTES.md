# 17 — Channels

## 🎯 Learning goals
- Create channels with `make`, and understand unbuffered (synchronous handoff) vs buffered.
- Send and receive with `<-`, and know exactly which operations block and when.
- Close a channel, use the `v, ok := <-ch` form, and `range` over a channel until close.
- Use directional channel types (`chan<- T`, `<-chan T`) to encode intent in signatures.
- Know the ownership rule: the sender closes, never the receiver — and never close twice.
- Recognise the deadlock and "send on closed channel" panics from their messages.

## 📚 Resources
- [A Tour of Go: Channels](https://go.dev/tour/concurrency/2)
- [Go by Example: Channels](https://gobyexample.com/channels)
- [Effective Go: Channels](https://go.dev/doc/effective_go#channels)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Pass a result from a goroutine back to `main` over an unbuffered channel.
- [ ] Trigger `fatal error: all goroutines are asleep - deadlock!` on purpose and explain why it happened.
- [ ] Produce 10 values in a goroutine, close the channel, and consume them with `range` in main.
- [ ] Show the difference between a buffered channel of size 3 and an unbuffered one with the same sends.
- [ ] Write `producer(out chan<- int)` and `consumer(in <-chan int)` and confirm the compiler rejects a wrong-direction use.
