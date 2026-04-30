---
title: Edit Field Service Management configurations for the Work management view
description: Edit your Field Service Management configurations as needed so that you can access and use the Work management view in the Enterprise Asset Workspace.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Edit Field Service Management configurations for the Work management view

Edit your Field Service Management configurations as needed so that you can access and use the Work management view in the Enterprise Asset Workspace.

## Before you begin

Role required: admin

## About this task

See [Global domain configurations](https://www.servicenow.com/docs/access?context=t_ConfigureFieldService&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US) for more information on Field Service Management configurations.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Configuration**.

2.  Edit the following configurations on the **Business Process** tab:

    |Configuration|Setting|
    |-------------|-------|
    |Lifecycle|
    |Process lifecycle|Set this configuration to **task-driven \(subtasks are required\)**.|
    |Approval for new request required|Disable this configuration.|
    |Qualification is required for new requests|Disable this configuration.|
    |Agent must accept or reject the assigned task|Disable this configuration.|
    |Track agent travel time|Disable this configuration.|
    |Work notes are required to close or cancel a request or task|Enable this configuration.|
    |Copy task work notes to request|Disable this configuration.|
    |Apply Work Order template in draft status|Enable this configuration.|
    |Catalog and Request Creation|
    |Create or update requests by inbound email|Disable this configuration.|
    |Create requests using catalog and form or form only|Set this configuration to **regular form only**.|
    |Templates create a dedicated catalog item|Disable this configuration.|

3.  Edit the following configurations on the **Assignment** tab:

    |Configuration|Setting|
    |-------------|-------|
    |Assignment Methods|
    |Assignment method for tasks|Set this configuration to **manually**.|
    |Dispatch Queue and Group Coverage|
    |Use dispatch queue|Disable this configuration.|
    |Assign requests or tasks based on assignment group coverage areas|Disable this configuration.|
    |Assign tasks based on assignment group product models|Disable this configuration.|
    |Assign tasks based on assignment group skills|Disable this configuration.|
    |Scheduling|
    |Use agent or task scheduling|Disable this configuration.|
    |Auto-selection of agents will consider time zone for tasks|Disable this configuration.|
    |Enable priority assignment|Disable this configuration.|
    |Additional Factors|
    |Auto-selection of agents will consider location of agents|Disable this configuration.|
    |Auto-selection of agents for tasks requires them to have skills|Set this configuration to **None**.|
    |Auto-selection will attempt to assign the same agent to all tasks in a request|Disable this configuration.|

4.  Edit the following configurations on the **Add-ons** tab:

    |Configuration|Setting|
    |-------------|-------|
    |Part Requirements|
    |Part requirements are needed by agents|Enable this configuration.|
    |Reserve parts in agent stockroom|Disable this configuration.|
    |Cancel open Transfer Orders|Disable this configuration.|
    |Edit associated models|Disable this configuration.|
    |Documentation|
    |Enable a dedicated knowledge base|Disable this configuration.|
    |Enable managed documents|Disable this configuration.|
    |Enable task activities|Disable this configuration.|
    |Associated Task Tables|
    |Edit associated task tables|Leave this configuration empty.|
    |Maps|
    |Enable maps|Disable this configuration.|

5.  Select **Save**.


