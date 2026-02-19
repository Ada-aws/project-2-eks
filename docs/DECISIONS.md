# Decisions Log (ADR-lite)

This file tracks important choices in this project, so I can explain them in interviews.

---

## 2026-02-19 — Repository structure
**Decision:** Use folders `terraform/`, `k8s/`, `helm/`, `scripts/`, `docs/`.

**Why:**
- `terraform/` = infrastructure (AWS)
- `k8s/` = Kubernetes manifests (deployments/services/ingress)
- `helm/` = Helm charts (packaging + reusable deployments)
- `scripts/` = helper scripts (bootstrap, validate, cleanup)
- `docs/` = architecture + decisions + runbooks

**Tradeoffs:**
- More folders upfront, less confusion later.

---

## 2026-02-19 — Preserve empty folders using `.gitkeep`
**Decision:** Add `.gitkeep` files to empty directories.

**Why:** Git only tracks files, not empty folders.

---

## 2026-02-19 — Use Terraform to provision EKS
**Decision:** Use Terraform instead of clicking in the AWS Console.

**Why:** Reproducible infrastructure, easier to audit, easier to destroy/clean up, real-world DevOps workflow.
