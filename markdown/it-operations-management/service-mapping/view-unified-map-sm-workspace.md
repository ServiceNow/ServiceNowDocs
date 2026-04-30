---
title: Access the Unified Map feature from the Service Mapping Workspace
description: View a hierarchical map of CIs and the relationships between them by adding access to the Unified Map feature to the Service Mapping Workspace.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Access the Unified Map feature from the Service Mapping Workspace

View a hierarchical map of CIs and the relationships between them by adding access to the Unified Map feature to the Service Mapping Workspace.

## Before you begin

Ensure that you have the following:

-   Vancouver release or later
-   Service Mapping Plus, November 2023 release
-   CMDB Workspace, v. 4.0.1 or later.

Role required: service\_mapping\_admin

## About this task

Review [Unified Map](https://www.servicenow.com/docs/access?context=cmdb-workspace-unified-map&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) to learn more about the Unified Map feature.

**Note:** The Unified Map feature offers limited Service Mapping functionality.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Enter **sn\_sm\_scoped\_app.sa.unified\_map.enabled** in the Search field.

3.  Confirm that the value of the property is set to true.

4.  Navigate to **Workspaces** &gt; **Service Mapping**.

    **Note:** Access to the Unified Map is only available through the Service Mapping Workspace.

5.  Select the Mapped application services widget.

6.  Select the check box next to the desired application service.

7.  Select the **View map** button.

    A new tab opens displaying the Unified Map for the application service in the CMDB Workspace.


**Parent Topic:**[Using Service Mapping](../concept/using-service-mapping.md)

**Related topics**  


[View the attributes of a CI or a relationship](https://www.servicenow.com/docs/access?context=unified-map-show-attributes&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[View service instances for a CI](https://www.servicenow.com/docs/access?context=unified-map-show-app-service&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[View historical changes for a CI](https://www.servicenow.com/docs/access?context=unified-map-show-ci-changes&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

