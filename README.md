# GitOps: WordPress + MySQL on Kubernetes with ArgoCD

This repo contains Kubernetes manifests for a WordPress + MySQL stack.

## Structure
- `mysql/` → MySQL Deployment, Service, PVC
- `wordpress/` → WordPress Deployment, Service, PVC

## Steps
1. Add this repo to ArgoCD (Settings → Repositories).
2. Create two ArgoCD Applications:
   - **MySQL**: Path `mysql/`
   - **WordPress**: Path `wordpress/`
3. Sync both apps from ArgoCD UI.
4. Access WordPress → `http://<EC2_PUBLIC_IP>:30080`
