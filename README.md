### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 29 of 35** · branch `29-databases`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 29 — Databases

## 🎯 Learning goals
- Understand `database/sql` as a driver-agnostic layer, and how blank-import drivers register themselves.
- Open a pool with `sql.Open` (it's lazy — `Ping` to actually connect) and tune `SetMaxOpenConns` etc.
- Use `QueryRow`/`Query`/`Exec` correctly, always `defer rows.Close()`, and check `rows.Err()`.
- Use placeholders for every user value — never string-concatenate SQL.
- Handle `sql.ErrNoRows` explicitly, and use `sql.NullString`/pointers for nullable columns.
- Run transactions with `BeginTx` + `defer tx.Rollback()` + `tx.Commit()`, and try `pgx` and `sqlx`.

## 📚 Resources
- [Tutorial: Accessing a relational database](https://go.dev/doc/tutorial/database-access)
- [pkg.go.dev: database/sql](https://pkg.go.dev/database/sql)
- [pgx — PostgreSQL driver and toolkit](https://github.com/jackc/pgx)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Connect to SQLite or Postgres, create a `users` table, and insert a row with `Exec`.
- [ ] Query many rows, scan them into a `[]User`, and remember to check `rows.Err()`.
- [ ] Query a missing row and handle `sql.ErrNoRows` as "not found" rather than a hard failure.
- [ ] Write a transfer function using a transaction that rolls back cleanly on error.
- [ ] Write the same query with string concatenation and with a placeholder, and write down the injection risk.

---

⬅️ **Prev:** [28 · HTTP Server & REST APIs](https://github.com/DulsaraNethmin/go-notebook/tree/28-http-server-and-rest-apis)  **Next:** [30 · gRPC](https://github.com/DulsaraNethmin/go-notebook/tree/30-grpc) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
