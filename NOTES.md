# 31 — CLI Applications

## 🎯 Learning goals
- Parse arguments with the standard `flag` package: typed flags, defaults, usage text, positional args.
- Build subcommands with `flag.NewFlagSet`, and know when to graduate to Cobra.
- Read piped input from stdin with `bufio.Scanner`, and detect whether stdin is a terminal or a pipe.
- Write user output to stdout and diagnostics to stderr — the Unix contract.
- Return meaningful exit codes with `os.Exit`, and remember `defer` does not run after it.
- Handle Ctrl-C gracefully with `signal.NotifyContext`.

## 📚 Resources
- [pkg.go.dev: flag](https://pkg.go.dev/flag)
- [Go by Example: Command-Line Flags](https://gobyexample.com/command-line-flags)
- [Cobra — a CLI framework for Go](https://github.com/spf13/cobra)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Write a `greet` CLI with `-name` and `-count` flags and a sensible `-h` usage message.
- [ ] Write a line-filter that upper-cases stdin, so `cat file | ./tool` works.
- [ ] Add two subcommands (`add`, `list`) using separate `flag.FlagSet`s.
- [ ] Exit with code 1 and an stderr message on bad input; verify with `echo $?`.
- [ ] Rebuild the same CLI with Cobra and note in your notes what you gained and what you paid.
