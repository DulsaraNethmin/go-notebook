### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 28 of 35** · branch `28-http-server-and-rest-apis`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 28 — HTTP Server & REST APIs

## 🎯 Learning goals
- Understand `http.Handler`, `http.HandlerFunc`, and `ResponseWriter`/`*Request`.
- Route with the standard `http.ServeMux`, including method + wildcard patterns (`GET /users/{id}`).
- Read path values, query params, headers and JSON request bodies.
- Write JSON responses with the correct status code and `Content-Type`, and centralise error responses.
- Write middleware as `func(http.Handler) http.Handler` and chain it (logging, recovery, auth).
- Configure `http.Server` properly: read/write timeouts and graceful shutdown with `Shutdown(ctx)`.

## 📚 Resources
- [The Go Blog: Routing Enhancements for Go 1.22](https://go.dev/blog/routing-enhancements)
- [pkg.go.dev: net/http](https://pkg.go.dev/net/http)
- [Go by Example: HTTP Server](https://gobyexample.com/http-servers)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Serve a JSON `/health` endpoint returning `{"status":"ok"}` with the right content type.
- [ ] Build a full CRUD `/todos` API backed by an in-memory map guarded by a mutex.
- [ ] Use `GET /todos/{id}` routing and read the id with `r.PathValue("id")`.
- [ ] Write logging and panic-recovery middleware and chain them around your mux.
- [ ] Add graceful shutdown on SIGINT with `signal.NotifyContext` and `srv.Shutdown(ctx)`.

---

⬅️ **Prev:** [27 · HTTP Client](https://github.com/DulsaraNethmin/go-notebook/tree/27-http-client)  **Next:** [29 · Databases](https://github.com/DulsaraNethmin/go-notebook/tree/29-databases) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
