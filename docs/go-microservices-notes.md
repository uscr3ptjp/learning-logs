# Go Microservices Notes

- Prefer `context.WithTimeout` for all external calls.
- Use `errors.Is` / `errors.As` instead of string matching.
- Keep protobuf definitions in a separate module for reuse.
- For retries, use exponential backoff with jitter.
- Always set `Server.Header` timeouts on `http.Server`.
- Use `go.uber.org/zap` for structured logging in production.

## Gotcha
- `sync.WaitGroup` with `Add` inside a loop can race — call `Add` before spawning goroutines.