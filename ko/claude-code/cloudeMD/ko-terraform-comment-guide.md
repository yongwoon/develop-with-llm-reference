# Code Comment Guidelines

**HCL/Terraform Comments:**

```hcl
# 기본적인 Binary Authorization을 활성화
enable_binary_auth = true
# Container Registry 에서 image 를 가져옴
repository_name = module.container_registry.repository_name
# production 환경에서 policy 적용
default_enforcement_mode = "ENFORCED_BLOCK_AND_AUDIT_LOG"
```

**Shell Script Comments:**

```bash
# Binary Authorization Policy 를 이동
terraform state mv \
  module.security.google_binary_authorization_policy.policy \
  module.container_security.google_binary_authorization_policy.policy
# CI/CD에서 image signing 예시
cosign sign --key env://COSIGN_PRIVATE_KEY \
  ${REGION}-docker.pkg.dev/${PROJECT_ID}/${REPOSITORY}/${IMAGE}:${TAG}
```

**YAML Comments:**

```yaml
# Container Security Module 설정
container_security:
  # Binary Authorization 활성화
  enable_binary_auth: true
  # Vulnerability scan 활성화
  enable_vulnerability_scanning: true
```

**Technical Terms to Keep in English:**

- API, Backend, Frontend, Database, Cache, Service, Repository
- Application, Component, Module, Framework, Library
- Request, Response, Schema, Model, Controller
- Test, Debug, Deploy, Build, Configuration
- Docker, Container, Server, Client, Router, Middleware
- Binary Authorization, Policy, Attestor, Registry, Image
- Terraform, Resource, Output, Variable, Data Source
- Cloud Run, GCP, AWS, Kubernetes, Deployment
