# Go Module Versioning Notes

- `go mod init <module>` sets the module path.
- Semantic import versioning: v2+ requires `/vN` suffix in module path.
- `replace` directives are local-only, don't commit them for shared projects.
- Tag with `git tag v1.0.0` before pushing for version discovery.
- Use `go get module@version` to pin dependencies.
- `go mod tidy` removes unused deps and adds missing ones.

# Today's date: 2026-08-13
- Revisit after reading "Go Modules in Real Life" article.