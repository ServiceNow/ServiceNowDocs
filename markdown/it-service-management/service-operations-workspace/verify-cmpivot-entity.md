---
title: Verify a CMPivot entity
description: Verify a CMPivot entity and its attributes to configure the display of the CI metrics information on the Investigation tab of the Incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/verify-cmpivot-entity.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring CI metrics for MECM, Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation, Setting up Investigation Framework in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Verify a CMPivot entity

Verify a CMPivot entity and its attributes to configure the display of the CI metrics information on the Investigation tab of the Incident record.

## Before you begin

The Microsoft Endpoint Configuration Manager server must be logged in using the Microsoft Remote Desktop.

Role required: admin

## Procedure

1.  Open the Microsoft Endpoint Configuration Manager.

2.  On the Microsoft Endpoint Configuration Manager, select **Assets and Compliance**.

3.  On the Assets and Compliance section, select **Devices**.

    The list of devices are displayed on the right pane of the window.

4.  Select the required CI device from the list.

    **Note:** The selected CI device must be Active.

    In case the required CMPivot entity isn’t displayed on the list, extend the hardware inventory to add the CMPivot entity to the list. For more information, see [Extend hardware inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/extend-hardware-entity.md).

5.  Click **Start CMPivot**.

    Alternatively, you can also right-click on the device and select **Start CMPivot**.

    \[Omitted image "start-cmpivot-console.png"\] Alt text: Start CMPivot

6.  Verify the CMPivot entity and attributes.

    \[Omitted image "verify-cmpivot.png"\] Alt text: Verify the CMPivot entity


**Parent Topic:**[Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/config-ci-metrics-mecm-adapter.md)

