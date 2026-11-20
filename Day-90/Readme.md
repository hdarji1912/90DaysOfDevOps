# Day 90 -- Grand Finale: The Complete DevOps Journey

## The Full 90-Day Map

```
LINUX FUNDAMENTALS (Days 1-13)
  Commands, processes, files, permissions, LVM
  "The foundation. Every DevOps tool runs on Linux."
         |
NETWORKING (Days 14-15)
  DNS, IP, subnets, ports
  "How machines talk to each other."
         |
SHELL SCRIPTING (Days 16-21)
  Bash basics, functions, projects
  "Automating what you'd otherwise type by hand."
         |
GIT & GITHUB (Days 22-28)
  Branching, advanced git, GitHub CLI
  "Version control. The backbone of everything that follows."
         |
DOCKER (Days 29-37)
  Images, Dockerfile, volumes, networking, Compose, multi-stage builds
  "Packaging applications so they run the same everywhere."
         |
CI/CD & GITHUB ACTIONS (Days 38-49)
  YAML, workflows, triggers, runners, secrets, DevSecOps
  "Automating build, test, and deploy on every push."
         |
KUBERNETES (Days 50-58)
  Pods, Deployments, Services, Namespaces, RBAC
  "Orchestrating containers at scale."
         |
TERRAWEEK (Days 59-67)
  Terraform, providers, state, modules, workspaces
  "Infrastructure as Code. Provision cloud resources declaratively."
         |
ANSIBLE (Days 68-72)
  Inventory, playbooks, roles, templates, Vault
  "Configuration management. Keep servers in the desired state."
         |
OBSERVABILITY (Days 73-77)
  Prometheus, Grafana, Loki, Promtail, OpenTelemetry, alerting
  "The three pillars: metrics, logs, traces. Know WHY things break."
         |
HELM (Days 78-80)
  Charts, templates, values, subcharts, multi-env deployment
  "Package manager for Kubernetes. One chart, many environments."
         |
AMAZON EKS (Days 81-83)
  Terraform for EKS, Gateway API, EBS storage, IRSA, HPA
  "Production-grade managed Kubernetes on AWS."
         |
ARGOCD & GITOPS (Days 84-86)
  GitOps principles, ArgoCD, sync strategies, App of Apps, CI/CD pipeline
  "Git is the single source of truth. The cluster always matches the repo."
         |
AGENTIC AI FOR DEVOPS (Days 87-89)
  LLM agents, ReAct pattern, MCP, KubeHealer, Temporal
  "AI that diagnoses and fixes infrastructure autonomously."
         |
        YOU ARE HERE (Day 90)
```

---

## Task 1: The End-to-End Pipeline

Trace a single code change through every tool you learned:

```
1. A developer writes code on a Linux machine (Days 1-13)
   using shell scripts (Days 16-21) and Git (Days 22-28)

2. They push to GitHub, which triggers GitHub Actions (Days 40-49)

3. The CI pipeline builds a Docker image (Days 29-37)
   and pushes it to DockerHub

4. The pipeline updates the Kubernetes manifest in Git
   with the new image tag

5. ArgoCD (Days 84-86) detects the change and syncs
   to an EKS cluster (Days 81-83)

6. The EKS cluster, provisioned by Terraform (Days 59-67)
   and configured by Ansible (Days 68-72), runs the app

7. Helm (Days 78-80) manages the deployment with
   environment-specific values

8. Prometheus, Grafana, and Loki (Days 73-77) monitor
   metrics, logs, and traces

9. If something breaks, an AI agent (Days 87-89)
   diagnoses the issue and proposes a fix

10. The fix goes through Git, ArgoCD syncs it,
    and the cycle continues
```

Every single block connects to the next. Nothing was learned in isolation.


---

## Task 2: Skills Inventory

Rate yourself on each skill. Be honest -- this is for you, not anyone else.

| Skill | Days | Confidence (1-5) |
|-------|------|------------------|
| Linux command line | 1-13 | |
| Shell scripting | 16-21 | |
| Git & GitHub | 22-28 | |
| Docker | 29-37 | |
| CI/CD (GitHub Actions) | 38-49 | |
| Kubernetes | 50-58 | |
| Terraform | 59-67 | |
| Ansible | 68-72 | |
| Observability (Prometheus, Grafana, Loki) | 73-77 | |
| Helm | 78-80 | |
| Amazon EKS | 81-83 | |
| ArgoCD / GitOps | 84-86 | |
| Agentic AI for DevOps | 87-89 | |

For anything below 3, go back and redo that block. The day folders are still there. The tasks have not changed.

---

## Task 3: What Comes Next

DevOps does not stop at day 90. Here is what to explore next:

**Deepen what you learned:**
- Multi-cluster Kubernetes (federation, fleet management)
- Advanced Terraform (custom providers, Terragrunt, drift detection)
- Service mesh (Istio, Linkerd)
- Secrets management (HashiCorp Vault, AWS Secrets Manager, External Secrets Operator)
- Database operations (backups, migrations, blue-green database deployments)
- Chaos engineering (Litmus, Chaos Monkey)
- FinOps (cloud cost optimization)

**Certifications to pursue:**
- Certified Kubernetes Administrator (CKA)
- Certified Kubernetes Application Developer (CKAD)
- HashiCorp Terraform Associate
- GitHub Actions Certification

**Build a portfolio project:**
Take everything from days 78-89 and build it from scratch for your own application:
1. Write an app (any language)
2. Dockerize it
3. Create a Helm chart
4. Provision EKS with Terraform
5. Deploy with ArgoCD
6. Monitor with Prometheus + Grafana
7. Set up the full GitOps CI/CD pipeline
8. Add an AI agent for troubleshooting

Put it on GitHub. Write a blog post about it. Share it on LinkedIn.

---

### 90-Day Timeline

| **Days** | **Topic** | **Learned** | **Key Lesson** |
|---|---|---|---|
| 1–13 | Linux | Commands, permissions, processes, LVM, packages, SSH | Linux is the foundation of DevOps |
| 14–21 | Networking + Shell | DNS, ports, subnetting, routing, Bash, automation | Automate repetitive work |
| 22–28 | Git & GitHub | Branching, merging, rebasing, cherry-picking, workflows | Version control enables collaboration |
| 29–37 | Docker | Images, containers, Dockerfiles, Compose, networking, volumes | Package apps to run consistently |
| 38–49 | CI/CD | GitHub Actions, YAML, secrets, runners, DevSecOps | Automate build, test, and deployment |
| 50–58 | Kubernetes | Pods, deployments, services, RBAC, scaling, troubleshooting | Orchestrate applications at scale |
| 59–67 | Terraform | Providers, resources, state, modules, variables, workspaces | Manage infrastructure as code |
| 68–72 | Ansible | Inventory, playbooks, roles, templates, Vault | Automate consistent server configuration |
| 73–77 | Observability | Prometheus, Grafana, Loki, OpenTelemetry, alerting | Monitor systems and troubleshoot faster |
| 78–80 | Helm | Charts, templates, values, hooks, multi-env deployments | Simplify Kubernetes deployments |
| 81–83 | Amazon EKS | EKS, Gateway API, storage, autoscaling, IAM | Run scalable workloads on AWS |
| 84–86 | ArgoCD / GitOps | Sync waves, App of Apps, declarative deployments | Git becomes the source of truth |
| 87–89 | Agentic AI for DevOps | ReAct, MCP, KubeHealer, AI troubleshooting, automated fixes | Use AI to accelerate troubleshooting |

---