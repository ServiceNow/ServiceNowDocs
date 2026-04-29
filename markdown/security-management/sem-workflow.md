---
title: Security Exposure Management workflow
description: Unified Security Exposure Management \(USEM\) is ServiceNow’s next-generation platform that consolidates multiple security exposure applications—Vulnerability Response \(VR\), Application Vulnerability Response \(AVR\), Container Vulnerability Response \(CVR\), and Configuration Compliance \(CC\)—into a unified architecture. It provides a single source of truth for security exposure, enabling real-time visibility, streamlined workflows, and automated remediation.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Unified Security Exposure Management, Security Operations]
---

# Security Exposure Management workflow

Unified Security Exposure Management \(USEM\) is ServiceNow’s next-generation platform that consolidates multiple security exposure applications—Vulnerability Response \(VR\), Application Vulnerability Response \(AVR\), Container Vulnerability Response \(CVR\), and Configuration Compliance \(CC\)—into a unified architecture. It provides a single source of truth for security exposure, enabling real-time visibility, streamlined workflows, and automated remediation.

The workflow involves the following steps:

1.  **Install and activate USEM applications**: Install the Unified Security Exposure Management plugin from the ServiceNow® Store.This automatically installs dependent apps such as:
    -   Security Exposure Management Workspace
    -   Administration for Security Exposure Management
    -   Risk Scoring
    -   Exception Management
    -   Remediation Task Management
2.  **Access the USEM Workspace**: Navigate to the Security Exposure Management Workspace.
3.  **Ingest and correlate data**: USEM supports ingestion from multiple scanners \(Qualys, Tenable, Veracode, etc.\). It deduplicates and correlates findings across infrastructure, applications, containers, and cloud environments.
4.  **Prioritise and remediate**: Use the Risk Scoring module to assign severity based on business impact. Launch remediation tasks directly from findings. Exception management is modularised and unified across all apps.
5.  **Monitor and report**: Dashboards provide real-time insights into exposure, remediation progress, and exception trends. Saved filters and watch topics help track critical findings.

