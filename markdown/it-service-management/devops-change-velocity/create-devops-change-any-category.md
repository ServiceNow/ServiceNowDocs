---
title: DevOps change request without mandating category as DevOps
description: Enable categorizing DevOps change request from DevOps properties. Change requests that are created as part of pipeline execution steps can be created with a category other than DevOps.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# DevOps change request without mandating category as DevOps

Enable categorizing DevOps change request from DevOps properties. Change requests that are created as part of pipeline execution steps can be created with a category other than DevOps.

## Before you begin

Role required: sn\_devops.admin

## About this task

Change requests created in the DevOps application aren’t created with **Category** as DevOps.

Use related templates for specific categories, such as **Hardware, Software, Database** and so on, to create DevOps change requests. You can categorize DevOps change requests from the DevOps properties.

New change requests that are created in the DevOps application after you enable the property can continue to use custom change policies and approval workflows, in addition to the base system's DevOps Demo Change Automation flow, and the DevOps Model Change Request flow. If you don’t enable this property, change requests continue to be created and processed with the category attribute set to DevOps.

## Procedure

1.  From the DevOps Change Workspace, navigate to **Administration** &gt; **System configuration** &gt; **Properties**.

    You can also navigate from **All** &gt; **DevOps** &gt; **Administration** &gt; **Properties**.

2.  Enable the **Categorize DevOps changes requests on "DevOps change" field** property.

    Select the check box to enable categorizing any change request created from the DevOps application, as a DevOps change request.

    By default, the property check box is cleared. To make changes, set the application scope to DevOps Data Model.

    **Important:** DevOps Insights capabilities are disabled when this property is selected.


## Result

Any new change request that is created from the DevOps application is considered as a DevOps change irrespective of the category attribute and processed accordingly. DevOps change request creation and processing no longer depend only on the category attribute being set to DevOps.

**Parent Topic:**[Accelerating your DevOps change process](../concept/dev-ops-change-acceleration.md)

