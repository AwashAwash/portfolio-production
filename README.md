DevSecOps Portfolio – End-to-End Journey

Overview

This project represents my complete journey from a basic static portfolio hosted on shared infrastructure to a fully self-managed, production-grade DevSecOps platform built on a Rocky Linux VPS.

It demonstrates practical, real-world implementation of:

Infrastructure ownership
CI/CD automation
Security-first engineering (DevSecOps)
Monitoring & observability
High-availability deployment practices


My Journey (3 Phases Evolution)

Phase 1 – Shared Hosting (Starting Point)

Built my first personal portfolio website
Hosted on traditional shared hosting
Limited control over:
Server configuration
Security
Deployment workflows
No automation, no observability
This phase helped me understand the limitations of traditional hosting.


Phase 2 – DevSecOps Migration (Ubuntu VPS)
I migrated from shared hosting → self-managed Ubuntu 24.04 VPS

What I Built:
Full containerization using Docker
Custom Dockerfile-based deployment
CI/CD-ready image pushed to Docker Hub
Cloudflare integration:
HTTPS (SSL/TLS)
HSTS
Proxy (Orange Cloud)
Staging subdomain
Security integration:
Trivy (image vulnerability scanning)
SonarCloud (code quality & analysis)
Monitoring stack:
Prometheus
Grafana
Netdata
Automated daily backups
Server hardening:
SSH key-based authentication
UFW firewall
Fail2Ban
Non-root user

Live Links:

Phase1 - https://www.linkedin.com/posts/activity-7412107817433812992-Q2Bd?utm_source=share&utm_medium=member_desktop&rcm=ACoAACY74gkBUtwskDdA_IAvKNLeRaESUXIyFis

Phase2 - https://www.linkedin.com/posts/activity-7424926449561686018-tUq3?utm_source=share&utm_medium=member_desktop&rcm=ACoAACY74gkBUtwskDdA_IAvKNLeRaESUXIyFis

Phase3 - 


This phase marked my transition into DevOps/DevSecOps practices.
Phase 3 – Enterprise Rebuild (Rocky Linux VPS) ⭐ Current

To gain enterprise-level experience, I rebuilt the entire project using Rocky Linux (RHEL-based).

High-Level Architecture

Architecture Summary
Cloudflare
DNS, HTTPS, WAF, DDoS protection
Nginx Reverse Proxy
Routes traffic to:
Production
Staging
Internal tools (Jenkins, Grafana)
Docker
Containerized applications
Separate environments:
portfolio-app (production)
portfolio-staging
Jenkins CI/CD Pipeline
GitHub integration
Automated:
Build
Security scan (Trivy)
Deployment

Monitoring Stack
Prometheus → metrics collection
Grafana → dashboards & visualization
Security Layer
Trivy → vulnerability scanning
Fail2Ban → brute-force protection
SSH hardening
Cloudflare WAF

Tech Stack
Categor Tools Used
OS 	                Rocky Linux (RHEL-based)
Containerization	Docker
Web Server	        Nginx
CI/CD	                Jenkins
Monitoring 	        Prometheus, Grafana
Security	        Trivy, Fail2Ban, SSH Hardening
DNS / CDN	        Cloudflare
Version Control	        GitHub

CI/CD Pipeline Flow
GitHub → Jenkins → Docker Build → Trivy Scan → Deploy Container
Pipeline Steps:
Clone repository from GitHub
Build Docker image
Run security scan (Trivy)
(Optional) Run SonarQube analysis
Deploy container (staging/production)

Environments
Environment	URL	Description
Production	awashmasketech.co.uk	Live portfolio
Staging	staging.awashmasketech.co.uk	Testing environment
Jenkins	jenkins.awashmasketech.co.uk	CI/CD
Grafana	grafana.awashmasketech.co.uk	Monitoring dashboard

Security Implementation
SSH key-based authentication (no password login)
Fail2Ban intrusion prevention
Nginx reverse proxy with security headers
Cloudflare WAF + DDoS protection
Trivy vulnerability scanning integrated into pipeline


Monitoring & Observability


Prometheus collects:
System metrics
Container metrics
Application health



Grafana dashboards:
CPU / Memory / Disk
Docker containers
Nginx traffic
Service health



Key Learnings

Real-world CI/CD pipeline implementation
Debugging complex pipeline failures (Trivy, SonarQube, Jenkins)
Reverse proxy & domain routing (Nginx)
Container lifecycle management
Resource constraints handling (RAM, swap, SonarQube tuning)
Security-first infrastructure design



Current Status
Production & staging environments running
CI/CD pipeline functional
Monitoring active (Grafana + Prometheus)
SonarQube used on-demand (due to resource constraints)


Future Improvements
Kubernetes (container orchestration)
Terraform (Infrastructure as Code)
OWASP ZAP integration (DAST scanning)
Advanced alerting (Grafana + Alertmanager)
Auto-scaling & load balancing
Blue/Green or Canary deployments



Final Note
This project reflects my evolution from:

“Deploying a website” → Designing and operating a full DevSecOps platform


