# 21 — File I/O & os

## 🎯 Learning goals
- Read and write whole files with `os.ReadFile` / `os.WriteFile`, and know their size limits in practice.
- Open files with `os.Open` / `os.Create` / `os.OpenFile`, and always `defer f.Close()`.
- Stream large files line by line with `bufio.Scanner`, and handle its buffer limit.
- Build portable paths with `path/filepath`, and walk trees with `filepath.WalkDir`.
- Use `os.Args`, `os.Getenv`/`os.LookupEnv`, `os.Exit`, and the standard streams.
- Understand file permissions, `os.Stat`, and `errors.Is(err, os.ErrNotExist)`.

## 📚 Resources
- [pkg.go.dev: os](https://pkg.go.dev/os)
- [Go by Example: Reading Files](https://gobyexample.com/reading-files)
- [pkg.go.dev: bufio](https://pkg.go.dev/bufio)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Write a `wc`-style tool that counts lines, words and bytes in a file given as `os.Args[1]`.
- [ ] Append to a log file with `os.OpenFile` and the `O_APPEND|O_CREATE|O_WRONLY` flags.
- [ ] Walk a directory tree with `filepath.WalkDir` and print every `.go` file you find.
- [ ] Read a missing file and detect it specifically with `errors.Is(err, os.ErrNotExist)`.
- [ ] Read a config value from an env var with `os.LookupEnv`, falling back to a default when unset.
