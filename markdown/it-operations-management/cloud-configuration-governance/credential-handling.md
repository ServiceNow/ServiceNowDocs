---
title: Credential handling
description: Extend the workflow engine to manage processes and automate things outside of an instance with Orchestration. Use the appropriate credentials required by Orchestration SSH and PowerShell activity elements: SSH requires SSH and PowerShell requires Windows.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Day 2 operations using Workflow Studio subflow, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Credential handling

Extend the workflow engine to manage processes and automate things outside of an instance with Orchestration. Use the appropriate credentials required by Orchestration SSH and PowerShell activity elements: SSH requires SSH and PowerShell requires Windows.

The Cloud Provisioning and Governance application generates credentials \(node credentials\) after a VM is provisioned. Node credentials are used to connect to a VM. In addition to node credentials, the system generates SSH/Windows credentials. These credentials are required for Orchestration, which provides the automation for workflows.

## Pre-existing VMs

Cloud Provisioning and Governance now generates SSH private key credentials and Windows credentials for all active pre-existing VMs provisioned through Cloud Provisioning and Governance.

## Delete credentials

When you deprovision or delete a VM, all associated credentials are deleted, including the node credential and SSH private key credentials/Windows credentials, as well as the credentials alias tag.

