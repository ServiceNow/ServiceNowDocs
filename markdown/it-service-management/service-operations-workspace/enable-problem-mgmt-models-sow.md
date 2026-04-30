---
title: Enable Problem Management models in Service Operations Workspace
description: Enable the Problem Management models system property so that you can create and use custom models.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Problem Management in Service Operations Workspace, Getting started, Service Operations Workspace for ITSM, IT Service Management]
---

# Enable Problem Management models in Service Operations Workspace

Enable the Problem Management models system property so that you can create and use custom models.

## Before you begin

See considerations for enabling and disabling Problem Management models at [Problem Management models in Service Operations Workspace](../concept/problem-mgmt-models-sow.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  From the Name column, search for `*models`.

3.  Select the **com.snc.problem\_management.models.enabled** system property.

4.  Set the **Value** field to **True**.

5.  Select **Update**.


## Result

Problem Management models are enabled.

