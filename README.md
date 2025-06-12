# BINGO-CI-CD


This repository demonstrates a full CI/CD pipeline for a Node.js app using **Jenkins**, **SonarQube**, **Trivy**, **OWASP Dependency-Check**, **Docker**, and **Docker Hub**.

## Project Highlights

- **Jenkins** Pipeline as Code (Jenkinsfile)
- **Static Code Analysis** via SonarQube
- **Dependency Security Scans**:
  - OWASP Dependency-Check (via Jenkins plugin)
  - Trivy FS & Image scanning for vulnerabilities
- **Dockerized** application pushed to Docker Hub
- **Automated deployment** of container on build agent

## 🚀 Setup Instructions

1. **Clone repo** and push to GitHub.
2. Setup Jenkins:
   - Install plugins: Pipeline, SonarQube Scanner, OWASP Dependency-Check, Docker, Trivy.
   - Define tools and credentials:
     - JDK (jdk-17), NodeJS (Node16), Sonar Scanner
     - Credentials: `sonar-token`, `docker` (Docker Hub), `dependency-check`
3. Configure SonarQube and Dependency-Check servers.
4. Create Jenkins pipeline project pointing to this repo.
5. Run pipeline and view the stages.

## 🛡️ Security Tools Overview

### SonarQube
Static analysis for code quality; enforces a quality gate to prevent vulnerabilities/bugs from slipping through.

### OWASP Dependency-Check
Scans `package.json` and `package-lock.json` to report known vulnerable libraries.

### Trivy FS & Image
FS scan spots insecure config and files; image scan checks Docker images for CVEs before deployment.

## ✅ Usage

- On build, code is checked out✅
- SonarQube runs analysis & pauses pipeline until quality gate passes✅
- Dependencies are checked for known vulnerabilities✅
- Docker image build, push, and vulnerability scanning✅
- Deployment to container runtime✅

---

## 🌟 Learnings & Skills

- Mastered **Jenkins pipeline scripting**
- Integrated **multiple security tools** into CI/CD
- Gained hands-on experience with **Docker build & deployment**
- Emphasized **security & quality gates** in automated workflows

---
