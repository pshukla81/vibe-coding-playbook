# Vibe Coding Playbook for AI-Assisted Software Development

Welcome to the Vibe Coding Playbook — a practical, production-focused guide to building, reviewing, and scaling AI-assisted code in modern SaaS environments.

This project curates best practices, prompt templates, code review workflows, and system-level considerations to safely and effectively use tools like Cursor, Claude, Copilot, and Devin in engineering teams.

---

## 🔍 What's Inside

* `vibe-coding-checklist.md` – A full-stack checklist for generating, reviewing, and approving AI-authored PRs in production systems
* `prompt-template.md` – A reusable prompt specification for engineers using AI code assistants
* `CONTRIBUTING.md` – How to suggest changes or submit ideas

---
## 🔄 Collaboration Workflow

🧑‍💻 Developer
* Creates structured prompt using the prompt-template.md 

* Saves as .prompt.md with unique ID in /prompts/

* Generates code using Claude, Cursor, or Copilot

* Adds prompt metadata to the code and PR

* Pushes PR with clear AI flag (e.g., ai-gen, prompt:claude)

👀 Reviewer
* Validates prompt context, traceability, and logic

* Uses checklist vibe-coding-checklist.md to audit code, test, security, and maintainability

* Approves only after confirming alignment with system constraints

## 👤 Who This Is For

This playbook is designed for:

* Engineering leaders looking to formalize their team’s AI coding practices
* Founders shipping early-stage GenAI or SaaS products
* Engineers contributing AI-generated features to secure, high-SLA products

---

## 💡 Core Philosophy

AI coding can increase velocity — but without context, constraints, and versioning, it risks introducing:

* Latency violations
* Security regressions
* Poor maintainability

This playbook introduces practical governance without stalling innovation.

---

## 🔒 License & Use

This project is licensed under **Creative Commons Attribution-NonCommercial 4.0 (CC BY-NC 4.0)**.
That means:

* ✅ You may share, remix, and adapt the materials with attribution
* 🚫 You may **not use it commercially** without express permission

Want to use this internally at your company? Just reach out.

---

## 🤝 Contributing

Want to improve this playbook? Open an [Issue](https://github.com/your-repo/issues) or submit a PR. Please read `CONTRIBUTING.md` before submitting.

---

## 👋 Maintainer

This project is built and maintained by Preeti Shukla, engineering leader and AI SaaS builder. Follow for more insights on AI-driven SaaS product development and scalable team practices.
www.linkedin.com/in/preeti-shukla-lead-technology
---

> AI tools may write your code, but only humans can own the outcomes. This playbook helps you do both responsibly.

---
