### Overview

- create a highly available Kubernetes cluster using the Kubeadm with Ansible. 



work arounds

- https://github.com/kubernetes-sigs/metrics-server/issues/525


```bash
kubectl patch deployment metrics-server -n kube-system --type 'json' -p '[{"op": "add", "path": "/spec/template/spec/containers/0/args/-", "value": "--kubelet-insecure-tls"}]'
```