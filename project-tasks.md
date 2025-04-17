# Developer Platform Tasks

## Service Bootstrapping
1. **init-service CLI tool**  
   *Description*: CLI to scaffold a new microservice with Dockerfile, Helm chart, GitHub Actions, and service docs.  
   *Est. Effort*: Large  
   *Labels*: scaffold, CLI, devxp  

2. **Boilerplate with tracing & metrics**  
   *Description*: Embed OpenTelemetry, Prometheus, and health checks in the template.  
   *Est. Effort*: Medium  
   *Labels*: observability, tracing  

3. **Auto-generate README + Swagger**  
   *Description*: Template includes README, API versioning, and Swagger boilerplate.  
   *Est. Effort*: Small  
   *Labels*: docs, api  

4. **GitHub repo creation**  
   *Description*: Add GitHub repo creation & team permission automation to CLI.  
   *Est. Effort*: Medium  
   *Labels*: GitHub API, automation  

## CI/CD
5. **Shared GitHub Actions workflows**  
   *Description*: Create reusable build.yaml, deploy.yaml, lint.yaml workflows.  
   *Est. Effort*: Medium  
   *Labels*: ci-cd, github  

6. **Canary + rollback with Argo**  
   *Description*: Add Argo Rollouts support to default Helm chart + GitHub Actions integration.  
   *Est. Effort*: Large  
   *Labels*: argo, helm, deployment  

7. **PR preview environments**  
   *Description*: Auto-deploy to temp namespace + post preview URL in PR comment.  
   *Est. Effort*: Medium  
   *Labels*: preview, github-actions  

8. **Add security/static checks**  
   *Description*: Add kube-linter, trivy, hadolint to CI templates.  
   *Est. Effort*: Small  
   *Labels*: security, ci  

## K8s Tooling
9. **Default Helm chart**  
   *Description*: Shared chart with probes, labels, annotations, and sane defaults.  
   *Est. Effort*: Medium  
   *Labels*: helm, k8s  

10. **Kyverno policies**  
    *Description*: Block :latest, enforce labels, limits, securityContext.  
    *Est. Effort*: Medium  
    *Labels*: policy, security  

11. **Auto-inject labels**  
    *Description*: Mutating webhook to add team, owner, cost-center.  
    *Est. Effort*: Large  
    *Labels*: k8s, automation  

12. **K8s dashboard RBAC**  
    *Description*: Setup OIDC + RBAC for team-based access to dashboard.  
    *Est. Effort*: Large  
    *Labels*: rbac, k8s, security  

## Observability
13. **Prometheus metrics enabled by default**  
    *Description*: Expose /metrics in scaffold, auto-register with Prometheus.  
    *Est. Effort*: Medium  
    *Labels*: metrics, observability  

14. **OpenTelemetry integration**  
    *Description*: SDK included in scaffold + optional sidecar config.  
    *Est. Effort*: Medium  
    *Labels*: tracing, otel  

15. **Centralized logging**  
    *Description*: Fluentbit config + Loki support for logs out of the box.  
    *Est. Effort*: Medium  
    *Labels*: logs, observability  

16. **Auto-generated dashboards**  
    *Description*: Use templates to provision Grafana dashboards per service.  
    *Est. Effort*: Large  
    *Labels*: grafana, automation  

## Dev Environments
17. **dev up command**  
    *Description*: Use Tilt or Skaffold to spin up service with dependencies locally.  
    *Est. Effort*: Large  
    *Labels*: tilt, skaffold  

18. **Ephemeral namespaces**  
    *Description*: PR triggers namespace + deploy preview via GitHub Action.  
    *Est. Effort*: Medium  
    *Labels*: preview-env, k8s  

19. **Local secret injector**  
    *Description*: Load secrets from SSM/Vault into local .env file.  
    *Est. Effort*: Medium  
    *Labels*: secrets, devtools  

## Cost & Tags
20. **Enforce tagging on deploy**  
    *Description*: Mutating webhook to enforce required tags on services.  
    *Est. Effort*: Medium  
    *Labels*: tagging, governance  

21. **Infracost in PRs**  
    *Description*: GitHub Action to show cost diff of Terraform plan in PR.  
    *Est. Effort*: Small  
    *Labels*: cost, github-actions  

22. **Weekly cost report**  
    *Description*: Generate and email cost breakdown per team/service.  
    *Est. Effort*: Large  
    *Labels*: cost, reporting  

23. **Idle resource detector**  
    *Description*: Lambda to find unused EC2/EBS/S3 and suggest cleanup.  
    *Est. Effort*: Large  
    *Labels*: cost, automation  

## Enablement
24. **Dev onboarding docs**  
    *Description*: Write quick-start guide for new devs using the platform.  
    *Est. Effort*: Small  
    *Labels*: docs, enablement  

25. **Golden path examples**  
    *Description*: Add template for REST, event-driven, scheduled services.  
    *Est. Effort*: Small  
    *Labels*: examples, docs  

26. **Platform changelog**  
    *Description*: Add a changelog to track platform updates and tools.  
    *Est. Effort*: Small  
    *Labels*: docs  

27. **Support Slack bot**  
    *Description*: Answer common platform Qs via a Slack bot or link to docs.  
    *Est. Effort*: Medium  
    *Labels*: support, automation  
