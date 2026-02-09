# ELK Stack Architecture

## Overview
This file documents about Elasticsearch, Kibana and Fleet in the office-lab1. All of these have been successfully installed inside the respective VMs.

---

## Current VM Architecture

**Host/Resources**
1. **ubuntu-server – Elasticsearch & Kibana**
   - Purpose: Elasticsearch node for log storage and search
   - Elastic Agent is also installed to collect & send data
2. **ubuntu-fleet – Fleet Server**
   - Purpose: Manages Fleet Server & Elastic Agents for data collection

> Note: This separation is temporary. The architecture may change (e.g. single-node stack, Elastic Agent on separate hosts, or containerized deployment).

---
