# Lab 2 — hello-app on Kubernetes

Your copy of this repository is your submission. The lab sheet is on the course site; this file is where you record what you did.

What's here:

| File | What it is |
|---|---|
| `src/`, `index.html` | a small React page that shows which Pod answered |
| `nginx.conf` | serves the page, and answers `/whoami` with the Pod name |
| `Dockerfile` | builds the page, then serves it with nginx on port 80 |

You don't change any of these. You add `hello-app.yaml` and fill in the sections below.

## Before you push, check

- [x] `hello-app.yaml` is in the root of this repository
- [x] `screenshot.png` is in the root of this repository
- [x] every section below is filled in

---

## 1. My image

Docker Hub image I deployed (for example `ravi123/hello-app:v1`):

```
such1t/hello-app:v1
```

## 2. Pods across nodes

Output of `kubectl get pods -o wide` after you applied `hello-app.yaml`:

```
<<RUN: kubectl get pods -o wide   and paste the 4-row output here>>
```

## 3. The Service and its endpoints

Output of `kubectl get service hello-app` and `kubectl get endpointslices -l kubernetes.io/service-name=hello-app`:

```
<<RUN: kubectl get service hello-app   and paste here>>

NAME              ADDRESSTYPE   PORTS   ENDPOINTS                                      AGE
hello-app-7tf8j   IPv4          80      10.244.2.7,10.244.1.6,10.244.2.8 + 1
