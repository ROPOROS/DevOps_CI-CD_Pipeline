# ⚙️ DevOps CI/CD Pipeline – ESPRIT Project

> A complete CI/CD pipeline integrating Jenkins, SonarQube, Nexus, Docker, Prometheus, Grafana, JUnit, and JMeter to automate build, test, deployment, and monitoring processes.

---

## 🧩 Tech Stack
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?logo=jenkins&logoColor=white)
![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?logo=sonarqube&logoColor=white)
![Nexus](https://img.shields.io/badge/Nexus-1B1F23?logo=sonatype&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?logo=grafana&logoColor=white)
![JUnit](https://img.shields.io/badge/JUnit-25A162?logo=junit5&logoColor=white)
![JMeter](https://img.shields.io/badge/JMeter-D22128?logo=apachejmeter&logoColor=white)

---

## 📚 Table of Contents
1. [Overview](#overview)
2. [Pipeline Stages](#pipeline-stages)
3. [Architecture](#architecture)
4. [Setup](#setup)
5. [Testing Frameworks](#testing-frameworks)
6. [Achievements](#achievements)
7. [Author](#author)

---

## Overview
This project demonstrates a **complete CI/CD pipeline** that automates source code integration, testing, quality analysis, artifact management, containerization, and monitoring.

It was developed as part of an **academic DevOps project at ESPRIT** to simulate a real-world continuous delivery workflow for modern web applications (Spring Boot + Angular).

---

## Pipeline Stages
1. **Source Control:**  
   Developers push code changes to a GitHub repository.

2. **Build & Unit Test (JUnit):**  
   Jenkins executes Maven builds and JUnit test suites to validate core functionality.

3. **Code Quality (SonarQube):**  
   SonarQube performs static analysis and enforces quality gates (bugs, coverage, code smells).

4. **Artifact Repository (Nexus):**  
   Successful builds are versioned and stored as artifacts in Nexus for traceability.

5. **Containerization (Docker):**  
   The pipeline builds and tags Docker images for both frontend and backend.

6. **Load Testing (JMeter):**  
   Jenkins executes JMeter test plans to simulate concurrent users and measure performance under load.

7. **Deployment:**  
   The Dockerized services are deployed automatically using Docker Compose.

8. **Monitoring (Prometheus & Grafana):**  
   Infrastructure and application metrics are scraped and visualized through dashboards.

---

## Architecture
- **CI/CD Engine:** Jenkins  
- **Code Quality & Testing:** JUnit, JMeter, SonarQube  
- **Artifact Management:** Nexus  
- **Container Runtime:** Docker  
- **Monitoring Stack:** Prometheus + Grafana

<p align="center">
  <img src="/ci-cd.jpg" alt="CI/CD Architecture" width="750">
</p>

---

## Setup
```bash
# Start Jenkins, SonarQube, and Nexus
docker-compose up -d

# Run CI/CD pipeline manually
jenkins build full-pipeline
