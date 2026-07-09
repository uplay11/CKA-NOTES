# Pod Commands

## Create a Pod

```bash
kubectl run nginx --image=nginx
```

---

## List Pods

```bash
kubectl get pods
```

---

## Show More Details

```bash
kubectl get pods -o wide
```

---

## Describe a Pod

```bash
kubectl describe pod <pod-name>
```

---

## View Pod Logs

```bash
kubectl logs <pod-name>
```

---

## Execute Commands Inside a Pod

### Open a Bash Shell

```bash
kubectl exec -it <pod-name> -- /bin/bash
```

> **Note:** If `/bin/bash` is not available, use:

```bash
kubectl exec -it <pod-name> -- /bin/sh
```

---

## Create a Pod Using a YAML File

```bash
kubectl create -f pod.yaml
```

---

## Generate Pod YAML

### Generate YAML Without Creating the Pod

```bash
kubectl run nginx --image=nginx --dry-run=client -o yaml
```

### Save the YAML to a File

```bash
kubectl run nginx --image=nginx --dry-run=client -o yaml > pod.yaml
```

---

## Edit a Running Pod

```bash
kubectl edit pod <pod-name>
```

> **Note:** Most Pod fields (such as the container image) cannot be edited directly. If changes are not allowed, delete and recreate the Pod or update the managing Deployment.

---
