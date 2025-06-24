## 🟩 **Problem 1: Container Image Vulnerability Scanner**

```markdown
# 🔐 Problem 1: Container Image Vulnerability Scanner

## 📌 Objective
Design a product that helps users identify and fix vulnerabilities in container images efficiently.

## 🧠 Why This Is Needed
Organizations using CI/CD pipelines push thousands of images. Without a clear UI to view scan results, it's hard to know which images are most vulnerable.

## ✅ Features
- Dashboard: View all scanned images
- Severity filters: Critical, High, Medium
- Image metadata: Name, tag, last scanned
- Drill-down: View detailed CVE report per image
- Export option: JSON or CSV reports
- Search bar and pagination for scaling
- Role-based access: Admin vs Analyst views

## 📄 Deliverables
- Product Requirements Document (PRD)
- Low-fidelity Wireframes (submitted separately)
```

---

## 🟨 **Problem 2: Kubernetes Security Scan**

````markdown
# 🛡️ Problem 2: Kubernetes Security Scan

## 📌 Objective
Use a scanning tool to check the security posture of a local Kubernetes cluster and generate a report of findings.

## 🔧 Tool Used
- Kubescape (or Trivy, kube-bench)

## 🪜 Steps to Reproduce
1. Install Kubescape:
```bash
curl -s https://raw.githubusercontent.com/kubescape/kubescape/master/install.sh | /bin/bash
````

2. Run the scan:

```bash
kubescape scan framework nsa --output json --output-file k8s-findings.json
```

3. Open the `k8s-findings.json` file to see:

* Summary of failed and passed controls
* Risk score
* Control descriptions
* Affected resources (if any)

## 📄 Deliverables

* `k8s-findings.json` file with results of the scan

````

---

## 🟦 **Problem 3: Go Web App + Docker + Kubernetes**

```markdown
# 🕒 Problem 3: DateTime Web App (Go + Docker + Kubernetes)

## 📌 Objective
Create a simple Go web app that shows the current date and time, containerize it, and deploy on Kubernetes with 2 replicas.

---

## 📁 File Structure

````

datetime-app/
├── main.go              # GoLang source code
├── Dockerfile           # Container build instructions
├── .dockerignore        # Ignore files during build
├── deployment.yaml      # Kubernetes deployment (2 replicas)
├── service.yaml         # Kubernetes service (LoadBalancer)
└── README.md            # Instructions for setup and deployment

````

---

## ▶️ Run Locally
```bash
go run main.go
````

## 🐳 Build & Push Docker Image

```bash
docker build -t yourdockerhubusername/datetime-app .
docker push yourdockerhubusername/datetime-app
```

## ☸️ Deploy on Kubernetes

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

To access the app:

```bash
kubectl get svc datetime-service
```

It should expose your app on a public IP (if supported) or node port.

```

---

Let me know if you'd like all this saved to a single downloadable `.md` file!
```
