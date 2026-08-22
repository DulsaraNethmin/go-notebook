### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 35 of 35** · branch `35-deployment-and-capstone`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 35 — Deployment & Capstone

## 🎯 Learning goals
- Write a multi-stage Dockerfile that builds a static binary and ships it on `scratch`/`distroless`.
- Configure services the twelve-factor way: environment variables, no secrets in the image.
- Build a CI pipeline in GitHub Actions: `go vet`, `go test -race`, lint, build, on every push.
- Release cross-platform binaries with GoReleaser and semantic version tags.
- Add production basics: health/readiness endpoints, structured logs, graceful shutdown.
- Pull the whole curriculum together into one capstone project you'd actually show someone.

## 📚 Resources
- [Docker: Build your Go image](https://docs.docker.com/language/golang/build-images/)
- [GoReleaser documentation](https://goreleaser.com/intro/)
- [setup-go GitHub Action](https://github.com/actions/setup-go)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Containerise the REST API from topic 28 with a multi-stage build and compare image sizes.
- [ ] Add a GitHub Actions workflow running `go vet`, `go test -race ./...` and a build on every push.
- [ ] Move every hardcoded setting (port, DSN, log level) into env vars with sane defaults.
- [ ] Tag `v0.1.0` and cut a multi-platform release with GoReleaser.
- [ ] **Capstone:** ship one real project end to end — e.g. a URL shortener, a job queue with workers, or a CLI + REST + Postgres task manager — with tests, CI, Docker and a README.

---

⬅️ **Prev:** [34 · Build, embed & Tooling](https://github.com/DulsaraNethmin/go-notebook/tree/34-build-embed-and-tooling)  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
