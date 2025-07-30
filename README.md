### Directory Overview

*   `deploy/`: Contains basic Kubernetes deployment manifests.
*   `nodejs/`: A sample Node.js application with its `Dockerfile` for containerization.
*   `nodejs/kube-workloard/`: Demonstrates various Kubernetes workload resources.
    *   `pod.yaml`: A basic Pod definition.
    *   `deployment.yaml`: Manages a set of replicated Pods.
    *   `service.yaml`: Exposes the deployment as a network service.
    *   `daemonset.yaml`: Ensures a copy of a Pod runs on all (or some) nodes.
    *   `cronjob.yaml`: Creates Jobs on a repeating schedule.
*   `nodejs/multi-container-pods/`: An example of a Pod with multiple containers (e.g., a Node.js app and an Nginx sidecar).
*   `nodejs/persistent-storage/`: Examples for using persistent storage in Kubernetes.
    *   `pv-pvc.yaml`: Defines a PersistentVolume and a PersistentVolumeClaim.
    *   `storage-demo-pod.yaml`: A Pod that uses the PVC to mount a volume.

## Prerequisites

Before you begin, ensure you have the following tools installed:
*   **Docker**: To build and manage container images.
*   **kubectl**: The Kubernetes command-line tool.
*   **A Kubernetes Cluster**: Such as [Minikube](https://minikube.sigs.k8s.io/docs/start/), [Kind](https://kind.sigs.k8s.io/docs/user/quick-start/), or a cloud-based cluster.

## How to Use

Each directory contains self-contained examples. Navigate into a directory to explore a specific concept.

### Applying Kubernetes Manifests

To deploy a Kubernetes resource, use the `kubectl apply` command:
```bash
# Example from the 'kube-workloard' directory
kubectl apply -f nodejs/kube-workloard/deployment.yaml
kubectl apply -f nodejs/kube-workloard/service.yaml
