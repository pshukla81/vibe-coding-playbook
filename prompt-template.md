# 🧠 Vibe Coding Prompt Template

Use this structured format when generating code with Claude, Copilot, or any AI assistant. Store each prompt file under the `/prompts/` directory using the format `prompt-name-version.md`. Reference the `prompt_id` in your code and pull request.

---

## 📝 Prompt Metadata

- **Prompt ID:** `invoice_payment_v3`  
- **Author:** alice@company.com  
- **Date:** 2025-05-04  
- **Model Used:** Claude 3 Opus  
- **Prompt File Location:** `/prompts/invoice_payment_v3.md`  

---

## 🔧 Prompt Purpose

> Generate an async Python function that captures and logs invoice payment events, with retries and audit trails. The code should support high QPS and follow clean architectural boundaries.

---

## 🌐 Connected APIs

- Stripe Payments API  
- Internal Billing Microservice (v2)

---

## ⚙️ Runtime & System Constraints

- Cloud Environment: AWS Lambda  
- Language: Python 3.10  
- Framework: FastAPI  
- Expected QPS: 500  
- Latency Target: 250ms (p99)  
- Availability Goal: 99.9%  
- Timeout Limit: 2 seconds max execution  
- Retry Strategy: Exponential backoff on HTTP 5xx  
- Rate Limiting Context: Tenant-based throttling

---

## 🔄 Concurrency & Behavior Expectations

- Use `async def` and `await` for all I/O-bound operations  
- Avoid sync libraries and blocking operations  
- Streaming: Not required  
- Batching: Not required  
- Idempotency: Required — duplicate invoice processing must not result in multiple charges

---

## 🔐 Security & Compliance Requirements

- Mask PII (e.g., tokens, user emails) in logs  
- Never log or expose secrets, JWTs, or API keys  
- Enforce RBAC using decoded JWT tokens  
- Ensure compliance with SOC 2 masking and storage policies  
- Use secure methods for fetching credentials or environment secrets

---

## ✅ Testing Requirements

- Include unit and integration test stubs  
- Use mocks for external services (Stripe, billing)
