# 🛰️ Technical Baseline

> Current technical baseline of the Project Sentinel laboratory environment.

---

## Purpose

This document establishes the current technical baseline of Project Sentinel.

Its purpose is to document the hardware, operating system, virtualization, networking, storage, tooling, and current capabilities available for building cybersecurity laboratories.

This baseline represents the starting point for the Technical Preparation Sprint and will be used to identify gaps, limitations, and improvements required before the first engineering laboratories are developed.

---

## Hardware

The primary Project Sentinel laboratory machine is a Lenovo ThinkPad X260.

| Component         | Specification                   |
| ----------------- | ------------------------------- |
| Model             | Lenovo ThinkPad X260            |
| CPU               | Intel Core i5-6300U             |
| CPU Cores/Threads | 4                               |
| RAM               | 8 GB                            |
| Storage           | 256 GB SSD                      |
| Graphics          | Intel HD Graphics 520 (SKL GT2) |

The current hardware provides the foundation for the laboratory environment, but available resources must be considered when designing virtualized and containerized laboratories.

Hardware expansion is currently limited. RAM is the main component that can be expanded if additional capacity becomes necessary.

---

## Operating System

The host operating system is Fedora Linux Workstation.

| Component           | Specification                       |
| ------------------- | ----------------------------------- |
| Distribution        | Fedora Linux 44 Workstation Edition |
| Desktop Environment | GNOME 50                            |
| Architecture        | 64-bit                              |
| Window System       | Wayland                             |
| Kernel              | Linux 7.1.8-200.fc44.x86_64         |
| Firmware            | R02ET76W (1.49)                     |

Fedora is currently used as the primary operating environment for Project Sentinel.

---

## Virtualization

Oracle VirtualBox is installed and currently provides the primary virtualization capability.

| Component         | Version |
| ----------------- | ------- |
| Oracle VirtualBox | 7.2.4   |

A Kali Linux virtual machine is currently available through VirtualBox.

The Kali environment originated from the Ethical Hacker course provided through Cisco Networking Academy and is available as a security-focused laboratory system.

VirtualBox currently provides the main mechanism for creating isolated laboratory environments.

---

## Containerization

Docker is installed on the host system.

The current environment includes:

- Docker Desktop
- Docker Compose

Both were installed through the terminal.

Containerization has not yet been extensively incorporated into the Project Sentinel laboratory methodology and will be further evaluated during the Technical Preparation Sprint.

---

## Version Control

Git is installed locally and is already integrated into the Project Sentinel development workflow.

| Component | Version |
| --------- | ------- |
| Git       | 2.55.0  |

The Project Sentinel repository is hosted on GitHub and follows the engineering standards established in the Engineering Handbook.

---

## Network

The laboratory machine provides two primary network interfaces:

- Ethernet — 10/100 local connection
- Native Wi-Fi adapter

The current network configuration provides connectivity for the host environment and will serve as the foundation for future laboratory network segmentation and communication scenarios.

Network isolation and laboratory-specific segmentation have not yet been formally designed.

---

## Storage

The primary storage available to the laboratory is the internal 256 GB SSD.

Additional storage may be provided through:

- External storage devices
- Cloud storage

Storage capacity must be considered when designing laboratories involving virtual machines, container images, logs, telemetry, packet captures, and other potentially large datasets.

---

## Installed Tooling

The currently identified engineering and laboratory tooling includes:

- Google Chrome
- Mozilla Firefox
- Visual Studio Code
- Git
- Docker
- Docker Compose
- Oracle VirtualBox
- Kali Linux virtual machine

Additional tools will be introduced according to the requirements of future laboratories rather than installed preemptively.

---

## Current Laboratory Capabilities

### Isolated Environments

The current environment can create isolated systems through Oracle VirtualBox.

Container-based isolation is also available through Docker, although its use as part of the standard laboratory methodology has not yet been established.

### Environment Destruction and Reproduction

The current environment provides the technical possibility of destroying and recreating laboratory environments.

However, reproducible environment creation has not yet been implemented as a formal process.

This represents one of the key areas to be addressed during the Technical Preparation Sprint.

### Automation

The current Project Sentinel workflow remains predominantly manual.

Examples include:

- Code creation and modification
- Git operations
- GitHub publication
- Notion updates
- Laboratory creation and configuration

Automation has not yet been formally introduced into the laboratory workflow.

---

## Current Limitations

The primary identified limitation is hardware capacity.

The current system provides:

- 8 GB RAM
- 256 GB SSD
- Intel Core i5-6300U processor

These resources are sufficient for the current development environment, but may become restrictive when multiple virtual machines, containers, security platforms, telemetry systems, or other resource-intensive components are executed simultaneously.

At present, RAM is the primary hardware upgrade path available.

---

## Current Technical Gaps

The following capabilities exist only partially or have not yet been formally established:

- Standardized laboratory architecture
- Network segmentation methodology
- Reproducible environment provisioning
- Standardized container usage
- Centralized telemetry
- Laboratory observability
- Automated environment deployment
- Automated validation
- Automated teardown and recreation
- Resource monitoring and capacity planning

These gaps will be evaluated during the Technical Preparation Sprint.

---

## Baseline Assessment

Project Sentinel currently has a functional development and laboratory foundation consisting of:

```text
ThinkPad X260
      │
      ├── Fedora Linux
      │
      ├── VirtualBox
      │      └── Kali Linux
      │
      ├── Docker
      │      └── Docker Compose
      │
      ├── Git
      │      └── GitHub
      │
      └── VS Code