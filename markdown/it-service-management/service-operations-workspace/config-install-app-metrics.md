---
title: Configure Installed application metrics
description: Configure the display of the installed application metrics for Microsoft Endpoint Configuration Manager for Investigation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/config-install-app-metrics.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring CI metrics for MECM, Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation, Setting up Investigation Framework in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure Installed application metrics

Configure the display of the installed application metrics for Microsoft Endpoint Configuration Manager for Investigation.

## Before you begin

Role required: sn\_cimaf.sn\_cimaf\_admin

## Procedure

1.  Open the Microsoft Endpoint Configuration Manager.

2.  Select the required CI device, and verify the CMPivot entities and attributes.

    For more information, see [Verify a CMPivot entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/verify-cmpivot-entity.md).

3.  Verify that the **InstalledSoftware** CMPivot entity exists and has the attributes **ProductName**, **ProductVersion**, and **Publisher**.

    **Note:** If the **InstalledSoftware** CMPivot entity isn’t available, you must add the entity to the hardware inventory. For more information, see [Extend hardware inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/extend-hardware-entity.md).


## Result

The installed application metrics is displayed on the **Investigation** tab of the incident record in Service Operations Workspace.

**Parent Topic:**[Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/config-ci-metrics-mecm-adapter.md)

