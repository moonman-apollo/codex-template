# Engineering guidance

Use applicable sections for design, implementation, and review; mark exclusions briefly. Follow project/language conventions and select tools during approved setup.

## Code and contracts

- Prefer cohesive modules, explicit interfaces/types, simple control flow, and testable domain rules. Make side effects and ownership clear; explain non-obvious rationale. Add abstractions for demonstrated needs.
- Validate untrusted inputs at boundaries. Define API/message schemas, errors, limits, access rules, and compatibility; follow the protocol's semantics. Document breaking changes and consumer transitions.
- Enforce data invariants with appropriate constraints/transactions. Review races, duplicate processing, and partial failure. Plan migrations for compatibility, verification, and recovery; reversing a migration may lose data.
- Handle failures explicitly. Bound external work with suitable timeouts, cancellation, resource limits, and cleanup. Retry only safe-to-repeat or deduplicated operations, with bounded retries.

## Verification and security

- Test behavior and invariants with appropriate unit/integration/critical-flow tests, including meaningful failures and regressions. Keep tests isolated and deterministic; avoid mocking away the behavior or chasing arbitrary coverage.
- Document supported versions, reproducible dependency resolution, safe example configuration, and exact formatter/lint/static/test/build commands. Run relevant local/CI checks; report failed/skipped/blocked checks. Assess dependency changes and applicable security scans.
- Keep secrets/private data out of source and logs. Use parameterized data access, vetted authentication/crypto, and least privilege. Review server-side authorization/tenant isolation, injection/escaping, sessions, uploads/paths/outbound requests, CSRF/CORS, and resource abuse where applicable.
- For elevated risk, document assets, entry points, trust boundaries, abuse tests, and independent review needs. For deployed services, assess configuration, health, observability, shutdown, and recovery. For UI, inspect accessibility, key states/devices, and browser/server contracts.

## References

Verified 2026-10-21; check applicable versions when using controls/specifications:

[Google review practices](https://google.github.io/eng-practices/review/reviewer/looking-for.html), [OWASP ASVS](https://owasp.org/projects/asvs) (select version/control IDs; no blanket compliance claim), [HTTP semantics](https://www.rfc-editor.org/rfc/rfc9110.html).
