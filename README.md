# @http/axum — Ergonomic Web Framework for Zeta

Auto-converted from [axum](https://crates.io/crates/axum) v0.8.9 via [Dark Factory](https://github.com/murphsicles/dark-factory).

## Features
- **Router** — type-safe routing with nesting and fallbacks
- **Extractors** — Path, Query, Json, Form, Bytes, String, State, Request parts, custom extractors
- **Middleware** — tower-based middleware stack (auth, CORS, compression, tracing)
- **Responses** — JSON, HTML, streaming, SSE, WebSocket upgrades, redirects
- **Error handling** — unified error type with IntoResponse
- **Sharing state** — thread-safe application state via extractors

## Usage
```zeta
use axum::{Router, routing::get};

let app = Router::new()
    .route("/", get(|| async { "Hello, World!" }));

axum::Server::bind(&"0.0.0.0:3000".parse().unwrap())
    .serve(app.into_make_service())
    .await
    .unwrap();
```

## Dependency chain
axum → tower → hyper → tokio-util → tokio → futures

## Stats: ~10,502 lines across 50+ source files, 0 unsupported items

## License
MIT