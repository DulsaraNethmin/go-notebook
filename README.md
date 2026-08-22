# 🐹 Go Notebook — 0 to Hero

My personal learning notebook for Go. **Every topic lives on its own branch.** This `main`
branch is the master index — the curriculum below, plus a progress checkbox for each topic.

## How this notebook works

- Each of the 35 topics has a branch named `NN-topic-name` (e.g. `07-maps`).
- Every topic branch ships a study template:
  - **`NOTES.md`** — learning goals, canonical resources, empty sections for my own notes and
    gotchas, and a short exercise checklist.
  - **`examples/`** — where I drop the Go code I write while learning that topic.
- I check out a topic, study it, fill in `NOTES.md`, write code in `examples/`, then commit and
  push that branch. Branches are never merged into `main` — each one stays a standalone notebook
  page, and `main` stays the clean index.
- When a topic is done I tick its box in the table below and commit that on `main`.

## My study workflow

```bash
# 1. Pick a topic and check it out
git checkout 07-maps

# 2. Study. Fill in NOTES.md, write code in examples/
#    go run examples/main.go

# 3. Commit my work on that topic branch
git add -A
git commit -m "Study notes and examples for maps"

# 4. Push the topic branch
git push origin 07-maps

# 5. Back to the index, tick the checkbox, commit on main
git checkout main
```

---

## Curriculum

### Phase 1 — Foundations

| No. | Branch | Topic | What you'll learn | Progress |
|----:|--------|-------|-------------------|----------|
| 01 | `01-setup-and-hello-world` | Setup & Hello World | Installing Go, `go run` vs `go build`, first module, `gofmt` | - [ ] |
| 02 | `02-variables-constants-and-types` | Variables, Constants & Types | `var` vs `:=`, `const`/`iota`, zero values, type conversions | - [ ] |
| 03 | `03-control-flow` | Control Flow | `if`/`else`, `switch`, the one `for` loop, `break`/`continue`, labels | - [ ] |
| 04 | `04-functions` | Functions | Multiple & named returns, variadics, closures, `defer` | - [ ] |
| 05 | `05-packages-and-modules` | Packages & Modules | `go.mod`, imports, exported names, `internal/`, project layout | - [ ] |

### Phase 2 — Core Data Structures

| No. | Branch | Topic | What you'll learn | Progress |
|----:|--------|-------|-------------------|----------|
| 06 | `06-arrays-and-slices` | Arrays & Slices | `len`/`cap`, `append`, `copy`, slice internals and aliasing gotchas | - [ ] |
| 07 | `07-maps` | Maps | CRUD, comma-ok idiom, random iteration order, maps as sets | - [ ] |
| 08 | `08-strings-runes-and-bytes` | Strings, Runes & Bytes | UTF-8, `strings`, `strconv`, `strings.Builder`, `[]byte` vs `string` | - [ ] |
| 09 | `09-structs` | Structs | Literals, embedding, struct tags, comparability, memory layout | - [ ] |
| 10 | `10-pointers` | Pointers | `&` and `*`, pointers vs values, `new`, why there's no pointer arithmetic | - [ ] |
| 11 | `11-methods` | Methods | Receivers, value vs pointer receivers, method sets, method values | - [ ] |

### Phase 3 — Abstractions

| No. | Branch | Topic | What you'll learn | Progress |
|----:|--------|-------|-------------------|----------|
| 12 | `12-interfaces` | Interfaces | Implicit satisfaction, type assertions & switches, `any`, nil interfaces | - [ ] |
| 13 | `13-error-handling` | Error Handling | Wrapping with `%w`, `errors.Is`/`As`, custom errors, `panic`/`recover` | - [ ] |
| 14 | `14-generics` | Generics | Type parameters, constraints, type inference, when *not* to use them | - [ ] |
| 15 | `15-io-and-standard-interfaces` | io & Standard Interfaces | `io.Reader`/`Writer`, `fmt.Stringer`, `sort.Interface`, composition | - [ ] |

### Phase 4 — Concurrency

| No. | Branch | Topic | What you'll learn | Progress |
|----:|--------|-------|-------------------|----------|
| 16 | `16-goroutines` | Goroutines | The `go` keyword, scheduler basics, `WaitGroup`, the race detector | - [ ] |
| 17 | `17-channels` | Channels | Buffered vs unbuffered, `close`, `range`, directional channel types | - [ ] |
| 18 | `18-select-and-concurrency-patterns` | select & Concurrency Patterns | `select`, timeouts, pipelines, fan-in/fan-out, worker pools | - [ ] |
| 19 | `19-sync-and-atomic` | sync & atomic | `Mutex`/`RWMutex`, `Once`, `sync/atomic`, `errgroup` | - [ ] |
| 20 | `20-context` | Context | Cancellation, deadlines, values, and the conventions around them | - [ ] |

### Phase 5 — Standard Library in Practice

| No. | Branch | Topic | What you'll learn | Progress |
|----:|--------|-------|-------------------|----------|
| 21 | `21-file-io-and-os` | File I/O & os | `os`, `bufio`, `path/filepath`, `os.Args`, environment variables | - [ ] |
| 22 | `22-json-and-encoding` | JSON & Encoding | `encoding/json`, struct tags, custom marshalling, `encoding/csv` | - [ ] |
| 23 | `23-time-and-scheduling` | Time & Scheduling | `time.Time`, durations, timers & tickers, the reference-time layout | - [ ] |
| 24 | `24-logging-and-slog` | Logging & slog | `log`, `log/slog`, structured logging, levels, handlers | - [ ] |
| 25 | `25-testing` | Testing | `go test`, table-driven tests, subtests, fakes & mocks, coverage | - [ ] |
| 26 | `26-benchmarking-and-fuzzing` | Benchmarking & Fuzzing | `go test -bench`, `b.Loop`, allocation stats, native fuzzing | - [ ] |

### Phase 6 — Web, Data & Services

| No. | Branch | Topic | What you'll learn | Progress |
|----:|--------|-------|-------------------|----------|
| 27 | `27-http-client` | HTTP Client | `net/http` client, building requests, timeouts, consuming JSON APIs | - [ ] |
| 28 | `28-http-server-and-rest-apis` | HTTP Server & REST APIs | Handlers, `ServeMux` method+path routing, middleware, JSON APIs | - [ ] |
| 29 | `29-databases` | Databases | `database/sql`, drivers, prepared statements, transactions, `pgx`/`sqlx` | - [ ] |
| 30 | `30-grpc` | gRPC | Protocol Buffers, service definitions, streaming, interceptors | - [ ] |
| 31 | `31-cli-applications` | CLI Applications | `flag`, Cobra, reading stdin, exit codes, good CLI design | - [ ] |

### Phase 7 — Hero Level

| No. | Branch | Topic | What you'll learn | Progress |
|----:|--------|-------|-------------------|----------|
| 32 | `32-reflection-unsafe-and-cgo` | Reflection, unsafe & cgo | `reflect`, reading struct tags, `unsafe` and cgo basics and their costs | - [ ] |
| 33 | `33-profiling-and-optimization` | Profiling & Optimization | `pprof`, the race detector, escape analysis, an optimization workflow | - [ ] |
| 34 | `34-build-embed-and-tooling` | Build, embed & Tooling | Build tags, `go:embed`, `go generate`, cross-compilation, `vet`/lint | - [ ] |
| 35 | `35-deployment-and-capstone` | Deployment & Capstone | Multi-stage Docker builds, CI, GoReleaser, and a capstone project | - [ ] |

---

## Progress

- **0 / 35** topics complete.
- Started: August 2026
