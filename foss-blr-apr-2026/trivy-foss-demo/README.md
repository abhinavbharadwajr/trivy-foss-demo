# DevSecOps with Trivy Demo

This repository demonstrates how to integrate security into a CI/CD pipeline using open-source tools.

## What this demo shows

- Scanning container images using Trivy
- Identifying vulnerabilities (CVEs)
- Fixing issues by updating dependencies
- Enforcing security in CI/CD pipelines

## Run locally

### Build image
docker build -t demo-app .

### Scan image
trivy image demo-app

## Fix vulnerabilities

- Update base image in Dockerfile
- Upgrade dependencies in requirements.txt

## CI/CD

GitHub Actions runs Trivy on every push and fails the build on HIGH/CRITICAL vulnerabilities.