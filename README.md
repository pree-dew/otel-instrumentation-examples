# Instrumenting a Go application using OpenTelemetry

Build and run the backend:

```sh
docker compose up -d
go install otel-instrumentation/cmd/notesserver
notesserver
```

Build and use the CLI app:

```sh
go install otel-instrumentation/cmd/notes
notes
notes add "important work"
notes list
notes add "very long description that is extremely important"
```

Browse exported telemetry:

- [Traces](http://localhost:16686)
- [Metrics](http://localhost:8889/metrics)

