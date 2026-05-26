I have recorded a comprehensive video walkthrough explaining the architecture, core logic, and error-handling steps for both automation tasks.
https://github.com/user-attachments/assets/0e5b06ac-34dd-461c-86d0-c8125c0bcfb2
Uploading Production Pipeline, QA Report, and Health Checks.mp4…

Task 2 <img width="1858" height="752" alt="Screenshot 2026-05-26 152943" src="https://github.com/user-attachments/assets/61c7a1d1-f71d-4243-9842-6c9eccf189ab" />
Task3 <img width="906" height="467" alt="Screenshot 2026-05-26 124150" src="https://github.com/user-attachments/assets/32af71ba-993d-40be-90e2-1d1ed45b098d" />
# Backend-Automation-Pipeline
“Production-ready backend automation pipelines built using n8n for GitHub REST API data processing and automated application uptime monitoring.”
## 📝 Project Description

This repository showcases advanced backend workflows designed to automate infrastructure checks and data engineering tasks using **n8n (low-code automation platform)**. The project is split into two specialized pipelines:

### 🚀 1. GitHub Trending Ingestion Pipeline (Task 1 & 2)
- **Objective:** Connects to the official GitHub REST API to dynamically poll high-volume repository datasets.
- **Data Engineering:** Cleans, maps, and sanitizes complex JSON payloads using custom JavaScript blocks. It handles edge cases like empty arrays and filters out unnecessary data keys to extract the Top 5 trending repositories based on custom stargazers metrics.
- **QA & Reporting:** Includes a comprehensive Quality Assurance (QA) and Root-Cause Analysis (RCA) report documenting security practices (such as JWT token persistence vulnerabilities in localStorage) and pipeline exception handling.

### 🌐 2. Automated Application Uptime Monitor (Bonus Task)
- **Objective:** Works as an automated Site Reliability Engineering (SRE) tool that monitors web application health.
- **Heartbeat Checks:** Triggered every 5 minutes, it sends automated HTTP requests to a target URL to pull live network status and server response metadata.
- **Conditional Alerting:** Evaluates HTTP headers (`statusCode === 200`). If a service outage, server crash (500), or bad gateway (502) is detected, the workflow instantly reroutes to deliver live, structured alerts to slack/discord webhooks containing accurate error logs and timestamps.
