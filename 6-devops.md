# ⚙️ DevOps and CI/CD

> Design and document your development-to-deployment pipeline. Use this section to simulate industry-grade DevOps practices such as CI/CD, infrastructure automation, observability, and secure delivery.

---

## 🔄 Continuous Integration (CI)

> Ensure every change is tested, linted, and built automatically before being merged.

### ✅ CI Tool Selection

- [ ] CI Tool Chosen:
  - [ ] GitHub Actions  
  - [ ] GitLab CI  
  - [ ] Jenkins  
  - [ ] CircleCI  
  - [ ] Bitbucket Pipelines  
  - [ ] Other: `__________________`

### ⚙️ Build & Test Automation

- [ ] Install/build dependencies  
- [ ] Run linters/formatters  
- [ ] Run unit & integration tests  
- [ ] Generate code coverage reports  
- [ ] Perform static code analysis (e.g., SonarQube, ESLint)  
- [ ] PR checks & required jobs configured  
- [ ] Caching strategies for build optimization (e.g., Docker, node_modules)

### 📝 Sample CI Config

> Add a `.yml` config example or link to your CI pipeline configuration.

**GitHub Actions Example**
```yaml
name: CI Pipeline 
on: [push, pull_request] 
jobs: 
  test: 
    runs-on: ubuntu-latest 
    steps: 
      - uses: actions/checkout@v3 
      - name: Install 
        run: npm ci 
      - name: Lint 
        run: npm run lint 
      - name: Test 
        run: npm test
```

---

## 🚀 Continuous Deployment (CD)

> Define how code gets deployed to different environments.

### 🧱 Environment Configuration

- [ ] Environments defined:
  - [ ] Development  
  - [ ] Staging  
  - [ ] Production  
- [ ] Secrets and environment variables managed securely via:
  - [ ] GitHub Secrets  
  - [ ] AWS Parameter Store  
  - [ ] HashiCorp Vault  
  - [ ] Doppler  
  - [ ] Other: `_________________`
- [ ] IaC tools used (e.g., Terraform, Pulumi):  
- [ ] Are deployments version-controlled?

### 🚦 Deployment Strategy

- [ ] Deployment method:
  - [ ] Rolling  
  - [ ] Blue/Green  
  - [ ] Canary  
  - [ ] Manual approval  
  - [ ] Other: `____________________`
- [ ] Zero-downtime deployment setup  
- [ ] Manual steps documented (if any)

### 🔁 Rollback & Recovery

- [ ] Rollback method:
  - [ ] Git Revert  
  - [ ] Previous Image/Tag  
  - [ ] Infra snapshot/restore  
- [ ] When rollback is triggered:  
- [ ] How rollback is tested/validated:

---

## 🪄 Infrastructure as Code (IaC)

> Automate infrastructure creation and updates.

- [ ] Tool used:
  - [ ] Terraform  
  - [ ] Pulumi  
  - [ ] AWS CloudFormation  
  - [ ] Other: `____________________`
- [ ] IaC stored in version control?  
- [ ] Linting/dry runs configured before apply?  
- [ ] Environments provisioned via IaC?  

---

## 📦 Containerization & Orchestration

- [ ] Using containers?
  - [ ] Docker  
  - [ ] Podman  
- [ ] Orchestration:
  - [ ] Kubernetes  
  - [ ] AWS ECS  
  - [ ] Docker Compose  
- [ ] Image tagging strategy defined (e.g., `latest`, `v1.0.0`, commit hash)  
- [ ] Local dev setup matches production (via Docker Compose, etc.)?

---

## 🧪 Test Environments & Preview Deployments

> Useful for collaboration and review before merging.

- [ ] Preview environments deployed on PRs?  
  - [ ] Vercel  
  - [ ] Netlify  
  - [ ] GitHub Actions + Docker Compose  
  - [ ] Custom scripts  
- [ ] Tear down previews after merge/close?  
- [ ] QA/Stakeholder access to previews?

---

## 🧭 Environment Promotion Process

- [ ] How is code promoted between environments?  
  - [ ] Branch-based  
  - [ ] Tag-based  
  - [ ] Manual promotion steps  
- [ ] Feature flags or toggles used?  
- [ ] Parity between environments documented?

---

## 🧠 Secrets & Security Practices

> Ensure secrets are stored, rotated, and scanned properly.

- [ ] Secrets stored in secure systems  
- [ ] `.env` and credential files ignored in Git  
- [ ] Tools used for scanning leaks:
  - [ ] GitGuardian  
  - [ ] truffleHog  
  - [ ] Gitleaks  
- [ ] Rotation policy for secrets defined?

---

## 📊 Monitoring & Observability Plan

- **Logging Tools:**
  - [ ] ELK Stack  
  - [ ] Loki + Grafana  
  - [ ] Cloud-native (e.g., AWS CloudWatch)  
- **Metrics & Dashboards:**
  - [ ] Prometheus  
  - [ ] Datadog  
  - [ ] New Relic  
  - [ ] Grafana  
- **Alerting:**
  - [ ] Email  
  - [ ] Slack  
  - [ ] PagerDuty  
  - [ ] Other: `______________`
- [ ] Dashboards created for key services?
- [ ] Logs/metrics integrated into CI/CD pipelines?

---

## 🛡️ Approval Gates & Compliance

> Optional but important for enterprise-grade pipelines.

- [ ] Manual approvals required for production?  
- [ ] RBAC enabled on CI/CD tooling?  
- [ ] Deployment history/audit logs available?  
- [ ] Compliance scans included (e.g., OWASP, Snyk)?  

---

## 🔁 Release Management & Automation

- [ ] Versioning strategy:
  - [ ] Semantic Versioning  
  - [ ] Date-based  
  - [ ] Commit-based  
- [ ] Changelogs generated?
  - [ ] Manually  
  - [ ] From PR titles / commits  
- [ ] Release notes published?

---

## 📉 Cost & Pipeline Efficiency

- [ ] Use of build caching or dependency caching  
- [ ] Resource usage monitored in pipelines  
- [ ] Ephemeral environments used to reduce cloud costs  
- [ ] Job timeout rules in place?

---

## ✅ CI/CD Testing Checklist

- [ ] CI triggers on PRs and commits  
- [ ] CD deploys to correct environments  
- [ ] Pipeline fails early on critical issues  
- [ ] Rollback tested successfully  
- [ ] Monitoring validates app health post-deploy  
- [ ] Secrets redacted in logs/output  

---

## 📌 Notes & Customizations

> Use this area for diagrams, constraints, or project-specific logic.

- Link to CI/CD dashboard: `_______________________`  
- Known limitations or risks:  
- Diagram of the CI/CD flow (optional):  
