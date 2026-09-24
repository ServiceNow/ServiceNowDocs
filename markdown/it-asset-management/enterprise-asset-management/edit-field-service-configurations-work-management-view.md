---
title: Edit Field Service Management configurations for the Work management view
description: Edit your Field Service Management configurations as needed so that you can access and use the Work management view in the Enterprise Asset Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/edit-field-service-configurations-work-management-view.html
release: brazil
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure, Enterprise Asset Management, Asset Management]
---

# Edit Field Service Management configurations for the Work management view

Edit your Field Service Management configurations as needed so that you can access and use the Work management view in the Enterprise Asset Workspace.

## Before you begin

Role required: wm\_admin

## About this task

For more information about Field Service Management configurations, see [Global domain configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/t_ConfigureFieldService.md).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Configuration**.

2.  Edit the following configurations on the **Business Process** tab:

    |Configuration|Setting|
    |-------------|-------|
    |Lifecycle|
    |Process life cycle|Set this configuration to **task-driven \(subtasks are required\)**.|
    |Qualification is required for new requests|Turn off this configuration.|
    |Agent must accept or reject the assigned task|Turn off this configuration.|
    |Track agent travel time|Turn off this configuration.|
    |Work notes are required to close or cancel a request or task|Enable this configuration.|
    |Copy task work notes to request|Turn off this configuration.|
    |Apply Work Order template in draft status|Enable this configuration.|
    |Catalog and Request Creation|
    |Create or update requests by inbound email|Turn off this configuration.|
    |Requests are created using|Set this configuration to **regular form only**.|
    |Templates create a dedicated catalog item|Turn off this configuration.|

3.  Edit the following configurations on the **Assignment** tab:

    |Configuration|Setting|
    |-------------|-------|
    |Assignment method for tasks|Set this configuration to **manually**.|
    |Use dispatch queue|Turn off this configuration.|
    |Assign requests or tasks based on assignment group coverage areas|Turn off this configuration.|
    |Assign tasks based on assignment group product models|Turn off this configuration.|
    |Assign tasks based on assignment group skills|Turn off this configuration.|
    |Scheduling|
    |Use agent or task scheduling|Turn off this configuration.|
    |Auto-selection of agents will consider time zone for tasks|Turn off this configuration.|
    |Enable priority assignment|Turn off this configuration.|
    |Additional Factors|
    |Auto-selection of agents will consider location of agents|Turn off this configuration.|
    |Auto-selection of agents for tasks requires them to have skills|Set this configuration to **None**.|

4.  Edit the following configurations on the **Add-ons** tab:

    |Configuration|Setting|
    |-------------|-------|
    |Part Requirements|
    |Part requirements are needed by agents|Enable this configuration.|
    |Reserve parts in agent stockroom|Turn off this configuration.|
    |Cancel open Transfer Orders|Turn off this configuration.|
    |Edit associated models|Leave this configuration empty.|
    |Documentation|
    |Enable a dedicated knowledge base|Turn off this configuration.|
    |Enable managed documents|Turn off this configuration.|
    |Enable task activities|Turn off this configuration.|
    |Associated Task Tables|
    |Select associated tables|Leave this configuration empty.|
    |Maps|
    |Enable maps|Turn off this configuration.|

5.  Select **Save**.


**Related topics**  


[Managing work orders for your enterprise assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/create-manage-wo-enterprise-assets.md)

