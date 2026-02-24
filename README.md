# Home Lab – Proxmox & Elastic Stack (WIP)

## Overview
This repository documents my personal home lab used for learning **virtualization, networking, and security monitoring**.

The lab is built on **Proxmox VE**, connected directly to an ISP router, and currently runs multiple **Ubuntu Server VMs** to experiment with the Elastic Stack.  
This setup is **work in progress** and will evolve as I test different architectures and best practices.

---

## Current Architecture (Initial Setup)

**Host**
- Hypervisor: Proxmox VE
- Network: Proxmox bridge connected to ISP router

**Virtual Machines**
1. **Ubuntu Server – Elasticsearch & Kibana**
   - Purpose: Elasticsearch node for log storage and search
2. **Ubuntu Server – Fleet Server**
   - Purpose: Manages Fleet Server & Elastic Agents for data collection
3. **Ubuntu Server - Logstash**
   - Purpose: Central component for log management, real-time analytics and data aggregation

> Note: This separation is temporary. The architecture may change (e.g. single-node stack, Elastic Agent on separate hosts, or containerized deployment).

---

## Network Topology (Simplified)

ISP Router  
→ Proxmox Host  
→ Proxmox Bridge (vmbr0)  
→ Ubuntu Server VMs

All VMs currently obtain IP addresses from the ISP router network.

---

## Goals of This Lab
- Learn Proxmox virtualization and VM management
- Understand Elastic Stack deployment and communication
- Practice log ingestion, visualization, and monitoring
- Experiment with different Elastic Stack architectures
- Learn deeper about Elastic's security
- Build proper documentation for future reference and troubleshooting

---

## What Will Change
Planned or possible changes:
- Add Elastic Agents on additional VMs or hosts
- Introduce VLANs or firewall segmentation
- Replace VMs with containers (Docker / Podman)
- Integrate security tools (e.g. Suricata, Zeek)

This README will be updated as the lab evolves.

---

## Documentation Structure
