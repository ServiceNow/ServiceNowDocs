---
title: Configure services metrics
description: Configure the services metrics for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring CI metrics for MECM, Investigation using Microsoft Endpoint Configuration Manager, Setting up Investigation Framework in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure services metrics

Configure the services metrics for Microsoft Endpoint Configuration Manager for Investigation \(MECM\).

## Before you begin

Role required: sn\_cimaf.sn\_cimaf\_admin

## Procedure

1.  Open the Microsoft Endpoint Configuration Manager.

2.  Select the required CI device, and verify the CMPivot entities and attributes.

    For more information, see [Verify a CMPivot entity](verify-cmpivot-entity.md).

3.  Configure the services metrics by verifying that the **Services** CMPivot entity exists and has the attributes **Name**, **DisplayName**, **State**, and **ProcessId**.


## Result

The services metrics are displayed on the **Investigation** tab of the incident record in Service Operations Workspace.

**Parent Topic:**[Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation](../concept/config-ci-metrics-mecm-adapter.md)

