# 25 — Testing

## 🎯 Learning goals
- Write `_test.go` files with `TestXxx(t *testing.T)` and run them with `go test ./...`.
- Know the difference between `t.Error`/`t.Errorf` (continue) and `t.Fatal`/`t.Fatalf` (stop).
- Write table-driven tests with subtests via `t.Run`, and use `t.Parallel` where safe.
- Use `t.Helper()`, `t.Cleanup()`, and `t.TempDir()` to keep tests clean.
- Test with fakes: pass in interfaces (`io.Reader`, a repo interface) instead of real dependencies.
- Measure coverage with `-cover` and `-coverprofile`, and know when to stop chasing the number.

## 📚 Resources
- [Tutorial: Add a test](https://go.dev/doc/tutorial/add-a-test)
- [pkg.go.dev: testing](https://pkg.go.dev/testing)
- [Go by Example: Testing and Benchmarking](https://gobyexample.com/testing-and-benchmarking)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Write a table-driven test with `t.Run` subtests for a function from an earlier topic.
- [ ] Add a failing case on purpose and read `go test -v` output until you can parse it at a glance.
- [ ] Use `t.TempDir()` to test a function that writes files, with no manual cleanup.
- [ ] Test an HTTP-calling function against `httptest.NewServer` instead of the real network.
- [ ] Run `go test -coverprofile=c.out ./... && go tool cover -html=c.out` and find one untested branch.
