# ✅ Vibe Coding Checklist for AI-Assisted Development in SaaS

This checklist supports engineering leaders, reviewers, and AI-powered developers in safely deploying AI-generated code in production SaaS environments.

---

##  Prompt Review Checklist

- [ ] Prompt file exists and is linked in the PR
- [ ] Prompt includes input/output contract and connected APIs
- [ ] Prompt captures system requirements: QPS, latency, availability
- [ ] Prompt specifies async/sync constraints, timeouts, retry logic
- [ ] Prompt version is tracked via prompt_id and markdown file
- [ ] Prompt references tech stack (frontend/backend/cloud runtime)
- [ ] Prompt references previous prompt version if revised

---

## Code Structure & Logic Checklist

- [ ] AI metadata header is present in generated code
- [ ] Code is modular and follows service boundaries
- [ ] Async usage is correct (`async def`, `await`) and justified
- [ ] No hallucinated methods, libraries, or vague function names
- [ ] Prompted logic reflects intended behavior with clarity
- [ ] Idempotency is enforced (e.g., payment or batch-processing)
- [ ] Streaming vs batching decisions match expected system behavior

---

## Security & Compliance Checklist

- [ ] No secrets, keys, or tokens are hard-coded or logged
- [ ] JWTs, emails, and PII are masked in logs
- [ ] Role-based access control (RBAC) logic is preserved
- [ ] Third-party dependencies are verified and minimal
- [ ] Meets company compliance needs (e.g., SOC 2, GDPR)
- [ ] External APIs handle errors, retries, and rate limits explicitly

---

## Testing & Verification Checklist

- [ ] Unit and integration tests included and scoped
- [ ] External APIs are mocked or sandboxed in tests
- [ ] Edge cases (timeouts, invalid input, retries) are covered
- [ ] Tests verify QPS, timeout, and performance constraints
- [ ] No skipped, commented, or placeholder tests

---

## Scalability & Observability Checklist

- [ ] Latency-sensitive sections are async or backgrounded
- [ ] Timeouts and retry strategies align with SLAs
- [ ] Proper rate-limiting and circuit-breaking are implemented
- [ ] Logs are structured (e.g., JSON, trace IDs)
- [ ] Metrics (e.g., latency, errors) are exposed and labeled

---

##  Documentation & Maintainability Checklist

- [ ] Prompt version and context are documented in code
- [ ] Prompt markdown file lives under `/prompts/`
- [ ] Reviewer can explain purpose of AI-generated logic
- [ ] Code is readable, testable, and owner-ready
- [ ] No brittle patterns or hidden coupling introduced

---

> Use this checklist during every PR review involving AI-authored code.  
> Production AI code should be just as accountable and observable as human-written code.
