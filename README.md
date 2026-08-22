### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)

> **Topic 30 of 35** · branch `30-grpc`
> Code I write for this topic lives in **[examples/](examples)**.

---

# 30 — gRPC

## 🎯 Learning goals
- Write `.proto` service and message definitions and understand proto3 field numbering.
- Generate Go code with `protoc` (or `buf`) plus `protoc-gen-go` and `protoc-gen-go-grpc`.
- Implement a server: register your service, serve on a listener, embed the `Unimplemented` struct.
- Write a client: dial a connection, call methods, pass a context deadline.
- Use all four call types: unary, server-streaming, client-streaming, bidirectional.
- Handle errors with `status`/`codes`, and add cross-cutting behaviour with interceptors.

## 📚 Resources
- [gRPC Go quick start](https://grpc.io/docs/languages/go/quickstart/)
- [Protocol Buffers: Go tutorial](https://protobuf.dev/getting-started/gotutorial/)
- [gRPC Go basics tutorial](https://grpc.io/docs/languages/go/basics/)

## 📝 My notes
<!-- Write what you learn here as you go. -->

## ⚠️ Gotchas
<!-- Surprises, footguns, and things that bit you. -->

## ✅ Exercises
- [ ] Define a `Greeter` service in a `.proto` file and generate the Go stubs.
- [ ] Implement the server and a client, and get a unary `SayHello` round trip working.
- [ ] Add a server-streaming method that pushes several messages for one request.
- [ ] Return a `codes.NotFound` error from the server and inspect it client-side with `status.FromError`.
- [ ] Write a unary server interceptor that logs the method name and duration of every call.

---

⬅️ **Prev:** [29 · Databases](https://github.com/DulsaraNethmin/go-notebook/tree/29-databases)  **Next:** [31 · CLI Applications](https://github.com/DulsaraNethmin/go-notebook/tree/31-cli-applications) ➡️  

### ⬅️ [Back to the Go Notebook index](https://github.com/DulsaraNethmin/go-notebook/blob/main/README.md)
