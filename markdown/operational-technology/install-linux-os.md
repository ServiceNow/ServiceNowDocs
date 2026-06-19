---
title: Install a Linux operating system
description: Install a Linux operating system on a virtual machine and then install the Discovery Console for OT on the same VM.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/install-linux-os.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Discovery Console for OT, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Install a Linux operating system

Install a Linux operating system on a virtual machine and then install the Discovery Console for OT on the same VM.

## Before you begin

Role required: admin

## About this task

-   Install the distribution with minimal configuration, including an SSH server, and confirm the VM supports AVX/AVX2 instructions.
-   Allocate 16 GB of RAM for installation. ​For resource requirements, see [Operational Technology Discovery deployment scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/deployment-scenarios.md) or .

## Procedure

1.  Install any of the following Linux distributions.

    |OS|Description|
    |---|-----------|
    |**Red Hat/Rocky 8.x and 9.x**|See [https://docs.redhat.com/en/documentation/red\_hat\_enterprise\_linux/10\#Installing%20RHEL](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/10#Installing%20RHEL).|
    |**Debian 12**|See [https://www.debian.org/releases/testing/amd64/](https://www.debian.org/releases/testing/amd64/).|
    |**Ubuntu 22.04 and 24.04**|See [https://ubuntu.com/tutorials/install-ubuntu-desktop\#1-overview](https://ubuntu.com/tutorials/install-ubuntu-desktop#1-overview).|


