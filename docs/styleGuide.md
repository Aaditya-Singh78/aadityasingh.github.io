# Best Practices for Portfolio: Aadityasingh.github.io

## Principles for code and structure
- Prefer explicit, consistent formatting and naming, enforced by automated tools. short, descriptive identifiers and conventional file/package naming reduce friction and aid reviews.

- Keep modules small and cohesive; design boundaries that are easy to test, document public surfaces clearly, and avoid “grab‑bag” utility packages.

- Treat types and schemas as contracts, generate or validate interfaces from a single source of truth so clients and servers stay in lockstep.

## Error handling and reliability
- Fail fast, return structured errors, and attach context that preserves causality without exposing internals. Never ignore errors in normal control flow.

- Make cancellation and timeouts first‑class. propagate request lifetime through contexts or equivalents and ensure cleanup on exit.

- Prefer idempotent, retriable operations and guard shared state. Design concurrency with bounded work, backpressure, and safe shutdown.


## APIs, contracts, and documentation
- Auto‑generate interactive documentation from code and types; keep docs tied to the implementation so drift is impossible.
    
- Standardize request/response shapes, pagination, and error envelopes, version public interfaces and deprecate with timelines.

- Validate inputs at the boundary and encode outputs deterministically. keep serialization rules centralized and testable.


## Testing and verification
- Use table‑style and fixture‑based tests. Test behavior at module seams and keep fast feedback as the default path.

- Add component and contract tests for UI and API layers. Exercise generated clients against the live spec to catch drift early.

- Measure what matters: 
1. Set budgets for latency, errors, and bundle size 
2. Add benchmarks and profiling where performance is critical.


## Performance and scalability
- Optimize only after correctness; profile, locate bottlenecks, and apply targeted changes like streaming, pagination, and code‑splitting.

- Prefer async/non‑blocking I/O and connection pooling. Use caching for read‑heavy paths and apply sensible defaults for timeouts and limits.

- Keep builds incremental and dev‑loop fast. Hot‑reload where possible and ensure component/state preservation during refresh.


## Security and safety
- Apply least privilege across tokens, database roles, and service accounts. rotate secrets and keep configuration out of code.

- Enforce CORS, auth flows, and input validation at edges. log security‑relevant events with trace correlation.

- Treat dependency policy as code; lock versions, audit regularly, and pin transitive risks in CI.


## Developer experience and CI/CD
- Make the happy path one command: format, lint, type‑check, test, and build. CI must reproduce local steps exactly.

- Generate artifacts (API specs, client types) in CI that fail builds on drift, schema breaks, lint violations, and test regressions.

- Support fast local iteration with hot reload/refresh and realistic dev configs; isolate env‑specific settings via configuration layers.


## Observability and operations
- Standardize logs, metrics, and traces which include correlation IDs and request scopes for cross‑service debugging.

- Expose health, readiness, and profiling endpoints in non‑production and  automate rollbacks and validate deployments with smoke tests.

- Define SLOs per surface area and alert on user‑visible symptoms first then keep dashboards simple and actionable.


## User interface and client ergonomics
- Keep components pure and named for predictable hot updates; decouple data‑loading from presentation. code‑split at route or feature boundaries.
    
- Derive client types from the same API schema, handle error states, loading, and retries uniformly across views.

- Maintain a consistent build setup with documented presets and minimal customizations to reduce drift and speed onboarding.