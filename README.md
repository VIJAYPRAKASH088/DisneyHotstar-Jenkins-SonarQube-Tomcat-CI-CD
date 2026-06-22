# DisneyHotstar-Jenkins-SonarQube-Tomcat-CI/CD
End-to-End DevOps Project | Jenkins CI/CD | SonarQube | AWS EC2 &amp; S3 | Apache Tomcat Deployment | Disney+ Hotstar Clone
An end-to-end DevOps project demonstrating CI/CD automation for a Java-based Disney+ Hotstar Clone application using Jenkins, Maven, SonarQube, AWS EC2 Instances and  S3 Bucket, and Apache Tomcat.

## Project Overview

This project automates the complete software delivery lifecycle:

- Source code checkout from GitHub
- Build and test using Maven
- Static code analysis using SonarQube
- WAR artifact generation
- Artifact upload to Amazon S3
- Automatic deployment to Apache Tomcat

---

## Architecture
GitHub Repository
        │
        ▼
     Jenkins
        │
 ┌───────────────┐
 │ Maven Compile │
 │ Maven Test    │
 └───────────────┘
        │
        ▼
  SonarQube Analysis
        │
        ▼
 Generate WAR File
        │
        ▼
 Upload Artifact to S3
        │
        ▼
 Deploy to Apache Tomcat
        │
        ▼
 Disney+ Hotstar Clone

##  Tech Stack

- Java
- Maven
- Git & GitHub
- Jenkins
- SonarQube
- AWS EC2
- Amazon S3
- Apache Tomcat 9

## AWS Infrastructure

### Jenkins Server
- Jenkins installed
- Maven configured
- Pipeline execution

### SonarQube Server
- SonarQube Community Edition
- Static code analysis and Quality Gate verification

### Tomcat Server
- Apache Tomcat 9
- Automatic application deployment

## 📊 SonarQube Results

✅ Quality Gate Passed

| Metric | Result |
|----------|--------|
| Bugs | 0 |
| Vulnerabilities | 0 |
| Security Hotspots | 0 |
| Reliability Rating | A |
| Security Rating | A |
| Maintainability Rating | A |

---

## 📦 Artifact Storage

Artifacts are stored in Amazon S3 for backup and centralized storage.

Bucket Name:
pipeline-s3-publisher

##  Project Structure
├── src/
├── target/
├── pom.xml
├── Jenkinsfile
├── README.md
└── screenshots/

## Features

- CI/CD Pipeline Automation
- Maven Build and Packaging
- SonarQube Static Code Analysis
- Quality Gate Validation
- Artifact Storage in Amazon S3
- Automated Deployment to Apache Tomcat
- Multi-Server AWS Infrastructure
- End-to-End DevOps Workflo

##  Future Enhancements

- Docker Containerization
- DockerHub Integration
- Trivy Security Scanning
- Kubernetes Deployment
- Terraform Infrastructure Automation
- Monitoring using Prometheus and Grafana

##  Author

**Vijay Prakash**

AWS | DevOps Engineer

GitHub: https://github.com/VIJAYPRAKASH088

---

⭐ If you found this project useful, consider giving it a star.
