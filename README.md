# 🐹 Go Notebook — 0 to Hero

My personal learning notebook for Go. **Every topic lives on its own branch.** This `main`
branch is the master index — click any topic below to jump straight to its branch.

## How this notebook works

- Each of the 35 topics has a branch named `NN-topic-name` (e.g. `07-maps`).
- In the tables below, the **Branch** link opens that branch on GitHub, and the **Topic** link
  opens that branch's `NOTES.md` directly.
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
| 01 | [`01-setup-and-hello-world`](https://github.com/DulsaraNethmin/go-notebook/tree/01-setup-and-hello-world) | [Setup & Hello World](https://github.com/DulsaraNethmin/go-notebook/blob/01-setup-and-hello-world/NOTES.md) | Installing Go, `go run` vs `go build`, first module, `gofmt` | - [ ] |
| 02 | [`02-variables-constants-and-types`](https://github.com/DulsaraNethmin/go-notebook/tree/02-variables-constants-and-types) | [Variables, Constants & Types](https://github.com/DulsaraNethmin/go-notebook/blob/02-variables-constants-and-types/NOTES.md) | `var` vs `:=`, `const`/`iota`, zero values, type conversions | - [ ] |
| 03 | [`03-control-flow`](https://github.com/DulsaraNethmin/go-notebook/tree/03-control-flow) | [Control Flow](https://github.com/DulsaraNethmin/go-notebook/blob/03-control-flow/NOTES.md) | `if`/`else`, `switch`, the one `for` loop, `break`/`continue`, labels | - [ ] |
| 04 | [`04-functions`](https://github.com/DulsaraNethmin/go-notebook/tree/04-functions) | [Functions](https://github.com/DulsaraNethmin/go-notebook/blob/04-functions/NOTES.md) | Multiple & named returns, variadics, closures, `defer` | - [ ] |
| 05 | [`05-packages-and-modules`](https://github.com/DulsaraNethmin/go-notebook/tree/05-packages-and-modules) | [Packages & Modules](https://github.com/DulsaraNethmin/go-notebook/blob/05-packages-and-modules/NOTES.md) | `go.mod`, imports, exported names, `internal/`, project layout | - [ ] |

### Phase 2 — Core Data Structures

| No. | Branch | Topic | What you'll learn | Progress |
|----:|--------|-------|-------------------|----------|
| 06 | [`06-arrays-and-slices`](https://github.com/DulsaraNethmin/go-notebook/tree/06-arrays-and-slices) | [Arrays & Slices](https://github.com/DulsaraNethmin/go-notebook/blob/06-arrays-and-slices/NOTES.md) | `len`/`cap`, `append`, `copy`, slice internals and aliasing gotchas | - [ ] |
| 07 | [`07-maps`](https://github.com/DulsaraNethmin/go-notebook/tree/07-maps) | [Maps](https://github.com/DulsaraNethmin/go-notebook/blob/07-maps/NOTES.md) | CRUD, comma-ok idiom, random iteration order, maps as sets | - [ ] |
| 08 | [`08-strings-runes-and-bytes`](https://github.com/DulsaraNethmin/go-notebook/tree/08-strings-runes-and-bytes) | [Strings, Runes & Bytes](https://github.com/DulsaraNethmin/go-notebook/blob/08-strings-runes-and-bytes/NOTES.md) | UTF-8, `strings`, `strconv`, `strings.Builder`, `[]byte` vs `string` | - [ ] |
| 09 | [`09-structs`](https://github.com/DulsaraNethmin/go-notebook/tree/09-structs) | [Structs](https://github.com/DulsaraNethmin/go-notebook/blob/09-structs/NOTES.md) | Literals, embedding, struct tags, comparability, memory layout | - [ ] |
| 10 | [`10-pointers`](https://github.com/DulsaraNethmin/go-notebook/tree/10-pointers) | [Pointers](https://github.com/DulsaraNethmin/go-notebook/blob/10-pointers/NOTES.md) | `&` and `*`, pointers vs values, `new`, why there's no pointer arithmetic | - [ ] |
| 11 | [`11-methods`](https://github.com/DulsaraNethmin/go-notebook/tree/11-methods) | [Methods](https://github.com/DulsaraNethmin/go-notebook/blob/11-methods/NOTES.md) | Receivers, value vs pointer receivers, method sets, method values | - [ ] |

### Phase 3 — Abstractions

| No. | Branch | Topic | What you'll learn | Progress |
|----:|--------|-------|-------------------|----------|
| 12 | [`12-interfaces`](https://github.com/DulsaraNethmin/go-notebook/tree/12-interfaces) | [Interfaces](https://github.com/DulsaraNethmin/go-notebook/blob/12-interfaces/NOTES.md) | Implicit satisfaction, type assertions & switches, `any`, nil interfaces | - [ ] |
| 13 | [`13-error-handling`](https://github.com/DulsaraNethmin/go-notebook/tree/13-error-handling) | [Error Handling](https://github.com/DulsaraNethmin/go-notebook/blob/13-error-handling/NOTES.md) | Wrapping with `%w`, `errors.Is`/`As`, custom errors, `panic`/`recover` | - [ ] |
| 14 | [`14-generics`](https://github.com/DulsaraNethmin/go-notebook/tree/14-generics) | [Generics](https://github.com/DulsaraNethmin/go-notebook/blob/14-generics/NOTES.md) | Type parameters, constraints, type inference, when *not* to use them | - [ ] |
| 15 | [`15-io-and-standard-interfaces`](https://github.com/DulsaraNethmin/go-notebook/tree/15-io-and-standard-interfaces) | [io & Standard Interfaces](https://github.com/DulsaraNethmin/go-notebook/blob/15-io-and-standard-interfaces/NOTES.md) | `io.Reader`/`Writer`, `fmt.Stringer`, `sort.Interface`, composition | - [ ] |

### Phase 4 — Concurrency

| No. | Branch | Topic | What you'll learn | Progress |
|----:|--------|-------|-------------------|----------|
| 16 | [`16-goroutines`](https://github.com/DulsaraNethmin/go-notebook/tree/16-goroutines) | [Goroutines](https://github.com/DulsaraNethmin/go-notebook/blob/16-goroutines/NOTES.md) | The `go` keyword, scheduler basics, `WaitGroup`, the race detector | - [ ] |
| 17 | [`17-channels`](https://github.com/DulsaraNethmin/go-notebook/tree/17-channels) | [Channels](https://github.com/DulsaraNethmin/go-notebook/blob/17-channels/NOTES.md) | Buffered vs unbuffered, `close`, `range`, directional channel types | - [ ] |
| 18 | [`18-select-and-concurrency-patterns`](https://github.com/DulsaraNethmin/go-notebook/tree/18-select-and-concurrency-patterns) | [select & Concurrency Patterns](https://github.com/DulsaraNethmin/go-notebook/blob/18-select-and-concurrency-patterns/NOTES.md) | `select`, timeouts, pipelines, fan-in/fan-out, worker pools | - [ ] |
| 19 | [`19-sync-and-atomic`](https://github.com/DulsaraNethmin/go-notebook/tree/19-sync-and-atomic) | [sync & atomic](https://github.com/DulsaraNethmin/go-notebook/blob/19-sync-and-atomic/NOTES.md) | `Mutex`/`RWMutex`, `Once`, `sync/atomic`, `errgroup` | - [ ] |
| 20 | [`20-context`](https://github.com/DulsaraNethmin/go-notebook/tree/20-context) | [Context](https://github.com/DulsaraNethmin/go-notebook/blob/20-context/NOTES.md) | Cancellation, deadlines, values, and the conventions around them | - [ ] |

### Phase 5 — Standard Library in Practice

| No. | Branch | Topic | What you'll learn | Progress |
|----:|--------|-------|-------------------|----------|
| 21 | [`21-file-io-and-os`](https://github.com/DulsaraNethmin/go-notebook/tree/21-file-io-and-os) | [File I/O & os](https://github.com/DulsaraNethmin/go-notebook/blob/21-file-io-and-os/NOTES.md) | `os`, `bufio`, `path/filepath`, `os.Args`, environment variables | - [ ] |
| 22 | [`22-json-and-encoding`](https://github.com/DulsaraNethmin/go-notebook/tree/22-json-and-encoding) | [JSON & Encoding](https://github.com/DulsaraNethmin/go-notebook/blob/22-json-and-encoding/NOTES.md) | `encoding/json`, struct tags, custom marshalling, `encoding/csv` | - [ ] |
| 23 | [`23-time-and-scheduling`](https://github.com/DulsaraNethmin/go-notebook/tree/23-time-and-scheduling) | [Time & Scheduling](https://github.com/DulsaraNethmin/go-notebook/blob/23-time-and-scheduling/NOTES.md) | `time.Time`, durations, timers & tickers, the reference-time layout | - [ ] |
| 24 | [`24-logging-and-slog`](https://github.com/DulsaraNethmin/go-notebook/tree/24-logging-and-slog) | [Logging & slog](https://github.com/DulsaraNethmin/go-notebook/blob/24-logging-and-slog/NOTES.md) | `log`, `log/slog`, structured logging, levels, handlers | - [ ] |
| 25 | [`25-testing`](https://github.com/DulsaraNethmin/go-notebook/tree/25-testing) | [Testing](https://github.com/DulsaraNethmin/go-notebook/blob/25-testing/NOTES.md) | `go test`, table-driven tests, subtests, fakes & mocks, coverage | - [ ] |
| 26 | [`26-benchmarking-and-fuzzing`](https://github.com/DulsaraNethmin/go-notebook/tree/26-benchmarking-and-fuzzing) | [Benchmarking & Fuzzing](https://github.com/DulsaraNethmin/go-notebook/blob/26-benchmarking-and-fuzzing/NOTES.md) | `go test -bench`, `b.Loop`, allocation stats, native fuzzing | - [ ] |

### Phase 6 — Web, Data & Services

| No. | Branch | Topic | What you'll learn | Progress |
|----:|--------|-------|-------------------|----------|
| 27 | [`27-http-client`](https://github.com/DulsaraNethmin/go-notebook/tree/27-http-client) | [HTTP Client](https://github.com/DulsaraNethmin/go-notebook/blob/27-http-client/NOTES.md) | `net/http` client, building requests, timeouts, consuming JSON APIs | - [ ] |
| 28 | [`28-http-server-and-rest-apis`](https://github.com/DulsaraNethmin/go-notebook/tree/28-http-server-and-rest-apis) | [HTTP Server & REST APIs](https://github.com/DulsaraNethmin/go-notebook/blob/28-http-server-and-rest-apis/NOTES.md) | Handlers, `ServeMux` method+path routing, middleware, JSON APIs | - [ ] |
| 29 | [`29-databases`](https://github.com/DulsaraNethmin/go-notebook/tree/29-databases) | [Databases](https://github.com/DulsaraNethmin/go-notebook/blob/29-databases/NOTES.md) | `database/sql`, drivers, prepared statements, transactions, `pgx`/`sqlx` | - [ ] |
| 30 | [`30-grpc`](https://github.com/DulsaraNethmin/go-notebook/tree/30-grpc) | [gRPC](https://github.com/DulsaraNethmin/go-notebook/blob/30-grpc/NOTES.md) | Protocol Buffers, service definitions, streaming, interceptors | - [ ] |
| 31 | [`31-cli-applications`](https://github.com/DulsaraNethmin/go-notebook/tree/31-cli-applications) | [CLI Applications](https://github.com/DulsaraNethmin/go-notebook/blob/31-cli-applications/NOTES.md) | `flag`, Cobra, reading stdin, exit codes, good CLI design | - [ ] |

### Phase 7 — Hero Level

| No. | Branch | Topic | What you'll learn | Progress |
|----:|--------|-------|-------------------|----------|
| 32 | [`32-reflection-unsafe-and-cgo`](https://github.com/DulsaraNethmin/go-notebook/tree/32-reflection-unsafe-and-cgo) | [Reflection, unsafe & cgo](https://github.com/DulsaraNethmin/go-notebook/blob/32-reflection-unsafe-and-cgo/NOTES.md) | `reflect`, reading struct tags, `unsafe` and cgo basics and their costs | - [ ] |
| 33 | [`33-profiling-and-optimization`](https://github.com/DulsaraNethmin/go-notebook/tree/33-profiling-and-optimization) | [Profiling & Optimization](https://github.com/DulsaraNethmin/go-notebook/blob/33-profiling-and-optimization/NOTES.md) | `pprof`, the race detector, escape analysis, an optimization workflow | - [ ] |
| 34 | [`34-build-embed-and-tooling`](https://github.com/DulsaraNethmin/go-notebook/tree/34-build-embed-and-tooling) | [Build, embed & Tooling](https://github.com/DulsaraNethmin/go-notebook/blob/34-build-embed-and-tooling/NOTES.md) | Build tags, `go:embed`, `go generate`, cross-compilation, `vet`/lint | - [ ] |
| 35 | [`35-deployment-and-capstone`](https://github.com/DulsaraNethmin/go-notebook/tree/35-deployment-and-capstone) | [Deployment & Capstone](https://github.com/DulsaraNethmin/go-notebook/blob/35-deployment-and-capstone/NOTES.md) | Multi-stage Docker builds, CI, GoReleaser, and a capstone project | - [ ] |

---

## Progress

- **0 / 35** topics complete.
- Started: August 2026

> The topic links above are GitHub branch links — they resolve once the branches are pushed.
