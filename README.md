
# Kubernetes Prompt Engineering Portfolio

This repository demonstrates examples of Kubernetes YAML manifests generated using AI-prompted instructions. Each manifest corresponds to a specific prompt and use case, covering deployment patterns, probes, volume mounts, and more.

## 📄 Prompt Table

| NAME                    | PROMPT                                                                                                | DESCRIPTION                                             | EXAMPLE                                                      |
| ----------------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------------ |
| app.yaml                | Create a basic Deployment named 'demo-app' with a single nginx container exposing port 80.            | Basic Deployment with Nginx container                   | [yaml/app.yaml](yaml/app.yaml)                               |
| app-livenessProbe.yaml  | Create a Deployment with livenessProbe on path / port 80, delay 5s, period 10s                        | Adds liveness check for HTTP-based health check         | [yaml/app-livenessProbe.yaml](yaml/app-livenessProbe.yaml)   |
| app-readinessProbe.yaml | Create Deployment with readinessProbe on `/` port 80, delay 5s, period 10s                            | Adds readiness check for ensuring service readiness     | [yaml/app-readinessProbe.yaml](yaml/app-readinessProbe.yaml) |
| app-volumeMounts.yaml   | Create Deployment that mounts ConfigMap demo-config to /usr/share/nginx/html as config-volume         | Demonstrates how to mount ConfigMap as volume in Pod    | [yaml/app-volumeMounts.yaml](yaml/app-volumeMounts.yaml)     |
| app-cronjob.yaml        | Create CronJob named demo-cronjob running every 5 minutes with nginx, printing date and Hello         | Shows how to define a simple periodic CronJob in Kuber  | [yaml/app-cronjob.yaml](yaml/app-cronjob.yaml)               |
| app-job.yaml            | Create Job named demo-job running nginx with a custom echo command                                    | Demonstrates one-off task execution with Kubernetes Job | [yaml/app-job.yaml](yaml/app-job.yaml)                       |
| app-multicontainer.yaml | Create a Deployment with nginx and a busybox sidecar                                                  | Demonstrates use of multi-container Pods with sidecar   | [yaml/app-multicontainer.yaml](yaml/app-multicontainer.yaml) |
| app-resources.yaml      | Create Deployment with resource requests and limits for an nginx container                            | Limits and guarantees resource usage per Pod            | [yaml/app-resources.yaml](yaml/app-resources.yaml)           |
| app-secret-env.yaml     | Inject env var `API_KEY` into nginx container from Secret `demo-secret` with same key                 | Demonstrates secret-based env injection in Pods         | [yaml/app-secret-env.yaml](yaml/app-secret-env.yaml)         |

---

All YAML files are available in the `/yaml` directory.

Prompts were engineered and refined using guidance from the [Prompt Engineering Google Whitepaper](https://www.kaggle.com/whitepaper-prompt-engineering) and tested via [kubectl-ai](https://github.com/GoogleCloudPlatform/kubectl-ai).

