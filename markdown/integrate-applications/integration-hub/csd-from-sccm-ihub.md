---
title: Client software distribution from SCCM
description: Use Client Software Distribution \(CSD\) to deploy and revoke software deployments from Microsoft System Center Configuration Management \(SCCM\) and manage distributions on SCCM hosts.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Client Software Distribution using Integration Hub, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Client software distribution from SCCM

Use Client Software Distribution \(CSD\) to deploy and revoke software deployments from Microsoft System Center Configuration Management \(SCCM\) and manage distributions on SCCM hosts.

The [Microsoft SCCM spoke](microsoft-sccm-spoke.md) contains actions that CSD uses to deploy software from a service catalog request and manage user and device collections on SCCM servers. In addition, CSD can manage license counts for deployed software using ServiceNow Software Asset Management, revoke software deployed by SCCM without user interaction, and manage lease periods.

-   **[Configuring SCCM](configure-sccm-ihub.md)**  
Follow the SCCM configuration procedures in the order shown.
-   **[SCCM deployment process](../reference/sccm-deployment-ihub.md)**  
Order an SCCM application from a client software distribution \(CSD\) catalog item in the service catalog triggers the Order Client Software flow.
-   **[Client software distribution validation process](csd-validation.md)**  
After SCCM deploys software to a target computer, client software distribution \(CSD\) detects the installation and validates its status.
-   **[SCCM software revocation](sccm-revocation-ihub.md)**  
Revoke software without any user interaction using Microsoft System Center Configuration Manager \(SCCM\) if the software configuration specifies an SCCM uninstall collection, even if the software was installed by some other process or user.

**Parent Topic:**[Client Software Distribution using Integration Hub](csd-integrationhub.md)

