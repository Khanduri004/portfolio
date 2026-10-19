# DevOps Engineer | SRE | Platform Engineering
 
Based in Dublin, Ireland. Authorized to work in Ireland, no sponsorship required.
 
[Email](mailto:shreya.khanduri104@gmail.com) · [LinkedIn](https://linkedin.com/in/shreya-khanduri-bhatt) · [GitHub](https://github.com/Khanduri004)
 
---
 
## About Me
 
I'm a DevOps Engineer with 3.5+ years of experience supporting production environments, building CI/CD pipelines, automating infrastructure, and improving reliability across cloud-native systems. My day-to-day toolkit covers Linux, AWS, Kubernetes, Terraform, Ansible, Jenkins, Docker, Prometheus, Grafana, Python, and Bash.
 
My background is in production support and release engineering: incident monitoring, troubleshooting, runbooks, on-call rotations, and building alerting that gives engineers clear signals instead of noise.
 
I moved to Dublin in 2025 and I'm actively looking for DevOps, SRE, and Platform Engineering roles in the Irish tech market. During this time I completed a Postgraduate Diploma in DevOps (Edureka, in association with Purdue University) and have kept building hands-on projects on AWS and Kubernetes, which you'll find below. Outside of work I volunteer with Dublin City Volunteers.
 
---
 
## Technical Skills
 
| Area | Tools |
|---|---|
| **Cloud** | AWS (EC2, S3, VPC, EKS, CloudWatch), Azure |
| **CI/CD & GitOps** | Jenkins (Groovy pipelines, shared libraries), GitHub Actions, Argo CD |
| **Infrastructure as Code** | Terraform, Ansible |
| **Containers & Orchestration** | Docker, Kubernetes, Helm |
| **Monitoring & Observability** | Prometheus, Grafana, AlertManager, CloudWatch |
| **Version Control** | Git, GitHub, GitLab |
| **Build Tools** | Maven, NPM, Gradle |
| **Scripting** | Python, Bash, YAML, PowerShell |
| **Operating Systems** | Linux (RHEL, Ubuntu) |
| **Networking** | TCP/IP, DNS, Load Balancers |
 
---
 
## Work Experience
 
### System Engineer, Tata Consultancy Services
*Oct 2023 – Nov 2024 · Delhi, India*
 
- Managed Jenkins CI/CD pipelines (Groovy) for multiple application teams, reducing deployment errors and manual release effort.
- Automated infrastructure provisioning with Terraform and Ansible across Dev, QA, and Prod environments, supported by Python and Bash scripts to streamline releases.
- Configured SLI-based alerting on the team's Prometheus and Grafana stack, defining thresholds so on-call engineers received specific, actionable alerts instead of generic health alerts and spent less time triaging noise.
- Managed Git repositories and branching strategies, and maintained runbooks and documentation to support on-call responders during incidents.
### Application Development Analyst, Accenture
*Jul 2019 – Sep 2021 · Pune, India*
 
- Supported and maintained Jenkins CI/CD pipelines, automating deployment steps with Python and Bash to cut down manual effort.
- Containerized application deployments with Docker and Kubernetes across dev and staging, using rolling updates for zero-downtime releases.
- Supported Linux production servers as part of a 24x7 on-call rotation, executing operational runbooks to help maintain service uptime.
---
 
## Featured Projects
 
### 1. ABC Technologies: End-to-End CI/CD on AWS EKS
 
**[View repository](https://github.com/Khanduri004/ABC-Technologies)**
 
**The problem:** a retail business running on conventional, manual development and deployment, with low availability, limited scalability, and slow releases. I designed and built the delivery platform to replace that.
 
**What I built:**
- **Infrastructure with Terraform:** VPC with public subnets, a Jenkins EC2 server bootstrapped by an install script (Jenkins, Docker, Maven, Java 17, kubectl, Helm, AWS CLI), and an EKS cluster.
- **Jenkins CI/CD pipeline:** GitHub webhook trigger, Maven tests with JaCoCo coverage reports, WAR build, multi-stage Docker image build, push to Docker Hub with Jenkins-managed credentials, then automated deployment to EKS.
- **Kubernetes deployment:** namespace, persistent volume claim, NodePort service, deployment with resource limits, and a Horizontal Pod Autoscaler.
- **Observability:** `kube-prometheus-stack` installed via Helm, with Prometheus scraping the application's `/metrics` endpoint, Grafana dashboards, and AlertManager.
**Stack:** Terraform · AWS (VPC, EC2, EKS) · Jenkins · Maven · JaCoCo · Docker · Kubernetes · Helm · Prometheus · Grafana · AlertManager
 
**Troubleshooting along the way:** fixed a provisioning script that broke on a rotated Jenkins GPG key and a Java version mismatch (Jenkins needing a newer JDK than the app targets) by installing both JDKs and pointing Jenkins at the right one.
 
---
 
### 2. EasyShop: Cloud-Native E-Commerce Platform on EKS (GitOps)
 
**[View repository](https://github.com/Khanduri004/tws-e-commerce-app)**
 
*Built from the TrainWithShubham EasyShop project (forked from [LondheShubham153/tws-e-commerce-app](https://github.com/LondheShubham153/tws-e-commerce-app)). The application is theirs; the infrastructure, pipeline, and deployment work is my hands-on implementation.*
 
A three-tier Next.js, TypeScript, and MongoDB application taken from commit to a live HTTPS deployment on Kubernetes.
 
**What I implemented:**
- **Terraform** for the AWS infrastructure: EKS cluster, bastion host, and Jenkins server in `eu-west-1`.
- **Jenkins CI** driven by a Jenkinsfile and a shared pipeline library, with GitHub and Docker Hub credentials managed in Jenkins and a webhook trigger.
- **GitOps continuous delivery with Argo CD**, syncing Kubernetes manifests from Git to the cluster automatically.
- **Ingress and TLS:** NGINX Ingress Controller via Helm, plus cert-manager with Let's Encrypt for HTTPS on a custom domain.
- Private cluster access through a bastion host configured with the AWS CLI and kubeconfig.
**Stack:** Terraform · AWS EKS · Jenkins · Argo CD · Docker · Kubernetes · Helm · NGINX Ingress · cert-manager
 
---
 
### 3. Multi-Environment Infrastructure as Code
 
**[View repository](https://github.com/Khanduri004/terraform-ansible-multi-env)**
 
*Built from the TrainWithShubham project (forked from [LondheShubham153/terraform-ansible-multi-env](https://github.com/LondheShubham153/terraform-ansible-multi-env)), with my own implementation and documentation of each step.*
 
Isolated **dev, staging, and production** environments provisioned from a single reusable Terraform module and configured with Ansible.
 
**What it covers:**
- **Modular Terraform:** one `infra` module (EC2, S3, DynamoDB) instantiated per environment with its own settings, and outputs exposing each environment's public IPs.
- **Remote state:** S3 bucket for state with a DynamoDB table for locking.
- **Ansible configuration management:** an Nginx role created with Ansible Galaxy, applied per environment through separate inventories.
- **Glue automation:** a shell script that reads Terraform outputs and regenerates the Ansible inventories for dev, staging, and prod, so provisioning and configuration stay in sync.
- Full teardown with `terraform destroy` to keep cloud costs under control.
**Stack:** Terraform · Ansible · AWS (EC2, S3, DynamoDB) · Bash · Nginx
 
---
 
## Education & Certifications
 
- **Postgraduate Diploma in DevOps**, Edureka in association with Purdue University (Jan 2025 – Nov 2025)
- **Bachelor of Engineering in Computer Science**, Banasthali Vidyapith, India (2015 – 2019)
---
 
## Community
 
- **Dublin City Volunteers:** active volunteer, supporting community events and projects across Dublin.
---
 
## Let's Connect
 
I'm open to DevOps, SRE, and Platform Engineering opportunities in Ireland.
 
- Email: [shreya.khanduri104@gmail.com](mailto:shreya.khanduri104@gmail.com)
- LinkedIn: [linkedin.com/in/shreya-khanduri-bhatt](https://linkedin.com/in/shreya-khanduri-bhatt)
- GitHub: [github.com/Khanduri004](https://github.com/Khanduri004)
 
