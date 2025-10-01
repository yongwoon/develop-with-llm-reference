**Code Comment Guidelines:**

**HCL/Terraform Comments:**

```hcl
# 基本的な Binary Authorization を有効化
enable_binary_auth = true

# Container Registry から Image を Pull
repository_name = module.container_registry.repository_name

# Production 環境での Policy 実施
default_enforcement_mode = "ENFORCED_BLOCK_AND_AUDIT_LOG"
```

**Shell Script Comments:**

```bash
# Binary Authorization Policy を移動
terraform state mv \
  module.security.google_binary_authorization_policy.policy \
  module.container_security.google_binary_authorization_policy.policy

# CI/CD での Image 署名例
cosign sign --key env://COSIGN_PRIVATE_KEY \
  ${REGION}-docker.pkg.dev/${PROJECT_ID}/${REPOSITORY}/${IMAGE}:${TAG}
```

**YAML Comments:**

```yaml
# Container Security Module の設定
container_security:
  # Binary Authorization を有効化
  enable_binary_auth: true

  # Vulnerability Scan を有効化
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
