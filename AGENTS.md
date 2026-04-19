# AGENTS.md

## Review guidelines

- Treat this repository as security-sensitive. Prioritize security findings over style issues.
- Focus on P0/P1 issues first.
- Flag any new or existing code that can enable:
  - authentication or authorization bypass
  - secret/token/cookie leakage
  - suspicious outbound network calls or data exfiltration
  - dynamic code execution (`eval`, `new Function`, shell execution, reflection, runtime loading)
  - unsafe deserialization or template injection
  - arbitrary file write/read, path traversal, archive extraction issues
  - dependency tampering, install/postinstall/preinstall abuse
  - hidden scheduled jobs, background tasks, webhooks, telemetry, or kill-switch behavior
  - obfuscated, minified, encrypted, or intentionally hard-to-review logic
- Treat “looks suspicious but not proven” as a finding that still needs human review.
- For every finding, include:
  - severity
  - exact file/function
  - why it is risky
  - realistic attack path or abuse path
  - minimal fix
  - whether a regression test should be added
- Do not make code changes until you first present a review plan and findings summary.
