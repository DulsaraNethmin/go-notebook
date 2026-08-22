### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 27 of 35** · branch `27-http-client`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 27 — HTTP Client

## 🎯 Learning goals
- Make requests with `http.Get`/`http.Post`, and know why you should build your own `http.Client`.
- Always set a `Timeout` on the client — the default zero value means wait forever.
- Build requests with `http.NewRequestWithContext` and set headers, query params and bodies.
- Always `defer resp.Body.Close()` and drain the body so connections get reused.
- Check `resp.StatusCode` explicitly — a 500 is not an `error` from `client.Do`.
- Decode JSON responses with `json.NewDecoder(resp.Body)`, and add retries/backoff where appropriate.

## 📚 Resources
- [pkg.go.dev: net/http — Client](https://pkg.go.dev/net/http#Client)
- [Go by Example: HTTP Client](https://gobyexample.com/http-client)
- [pkg.go.dev: net/http/httptest](https://pkg.go.dev/net/http/httptest)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] GET a public JSON API and decode the response into a struct you defined.
- [ ] Build a shared `http.Client` with a 10s timeout and reuse it for several requests.
- [ ] POST a JSON body with the right `Content-Type` header and check the status code.
- [ ] Cancel an in-flight request with a context timeout and inspect the resulting error.
- [ ] Wrap the call in a small `APIClient` struct and test it against `httptest.NewServer`.

---

⬅️ **Prev:** [26 · Benchmarking & Fuzzing](https://github.com/DulsaraNethmin/go-notebook/tree/26-benchmarking-and-fuzzing)  **Next:** [28 · HTTP Server & REST APIs](https://github.com/DulsaraNethmin/go-notebook/tree/28-http-server-and-rest-apis) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
