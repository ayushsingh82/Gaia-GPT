# Kubernetes Deployment

```bash
# Deploy the service
$ kubectl apply -f ubitgpt-lite-deployment.yaml -f env-secret.yaml
namespace/ubitgpt-lite created
deployment.apps/ubitgpt-lite created
service/ubitgpt-lite created
secret/env created

# Get the service
$ kubectl -n ubitgpt-lite get svc
NAME           TYPE        CLUSTER-IP    EXTERNAL-IP   PORT(S)    AGE
ubitgpt-lite   ClusterIP   10.0.199.26   <none>        3000/TCP   7m8s

# Use port-forward to access the service
$ kubectl -n ubitgpt-lite port-forward svc/ubitgpt-lite 5566:3000
Forwarding from 127.0.0.1:5566 -> 3000
Forwarding from [::1]:5566 -> 3000
```
