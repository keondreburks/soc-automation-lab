# soc-automation-lab
# 🔐 SOC Automation Lab: Wazuh + Shuffle + TheHive

## 📌 Overview

This project demonstrates an end-to-end SOC automation pipeline that detects threats (Mimikatz), triggers automated workflows, and creates incident cases.

## 🧱 Architecture

* SIEM: Wazuh ![SIEM](https://img.shields.io/badge/SIEM-Wazuh-blue)
* SOAR: Shuffle   ![SOAR](https://img.shields.io/badge/SOAR-Shuffle-orange)
* Case Management: TheHive

## 🔄 Workflow

1. Wazuh detects Mimikatz activity
2. Alert is sent via webhook to Shuffle
3. Shuffle processes alert
4. Case is created in TheHive


## 🏗️ Architecture Diagram
![SOC Architecture](drawio.png)

## ⚙️ Technologies Used

* Wazuh
* Shuffle SOAR
* TheHive
* Elasticsearch
* Ubuntu Server

## 🚨 Use Case: Mimikatz Detection

* Detect credential dumping activity
* Automate alert triage
* Generate incident cases

## 📸 Screenshots

### Shuffle Workflow

![Shuffle](https://github.com/keondreburks/soc-automation-lab/blob/c47abd3a255b45e694e106f3db6b582bcb13d087/shuffle-workflow.png)

### TheHive Case

![TheHive](https://github.com/keondreburks/soc-automation-lab/blob/834e6f461daf37bb97300c1ae15b071829ae7a59/mimikatz%20case.png)

### Wazuh Alert

![Wazuh](https://github.com/keondreburks/soc-automation-lab/blob/df6fa6f83a10987d7024be5a29a45d5d500c1250/mimikatz%20alert.png)

## 🛠️ Setup Guide

See: docs/setup-guide.md

## 📂 Config Files

* configs/wazuh-ossec.conf
* configs/elasticsearch.yml
* configs/thehive-application.conf

## 🚀 Future Improvements

* Add Cortex analyzers
* Integrate VirusTotal
* Add Slack notifications

## 👤 Author

Keondre Burks
