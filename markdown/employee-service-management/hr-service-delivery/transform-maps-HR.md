---
title: Create transform maps in Enterprise Service Management Integrations Framework
description: Create a transform map to specify data relationships between the import set table and the target table.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Service Management Integrations Framework, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Create transform maps in Enterprise Service Management Integrations Framework

Create a transform map to specify data relationships between the import set table and the target table.

## Before you begin

Role required: sn\_hr\_integr\_fw.admin

## About this task

For every transformation, you must either create a transform map or select an existing one.

## Procedure

1.  Navigate to **Integrations Framework** &gt; **Transform Maps**.

2.  View the existing transform maps.

    |Name|Description|
    |----|-----------|
    |HR Pull to-do transform map|Moves tasks or Todos from the HR Pulled To-do Integration Staging \[sn\_hr\_integr\_fw\_todo\_inbound\_staging\] table into the HR Pulled Integration To-do \[sn\_hr\_integr\_fw\_todo\_inbound\] table.|
    |HR Profile Transform Map|Maps workers, future workers, and effective workers from the HR Profile Staging \[sn\_hr\_integr\_fw\_hr\_profile\_staging\] table into the HR Profile \[sn\_hr\_core\_profile\] table.|
    |Job Transform Map|Maps job profiles from the Job Staging \[sn\_hr\_integr\_fw\_job\_staging\] table to the Job \[sn\_hr\_core\_job\] table.|
    |Department Transform Map|Maps departments from the Department Staging \[sn\_hr\_integr\_fw\_department\_staging\] table to the Department \[cmn\_department\] table.|
    |Location Transform Map|Maps locations from the Location Staging \[sn\_hr\_integr\_fw\_location\_staging\] table to the Location \[cmn\_location\] table.|
    |Position Transform Map|Maps positions from the Position Staging \[sn\_hr\_integr\_fw\_position\_staging\] table to the Position \[sn\_hr\_core\_position\] table.|

3.  To create a transform map, click **New**.

    For details of how to create a transform map, refer to the table in [Transformation scripts](https://www.servicenow.com/docs/access?context=t_CreateATransformMap&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).


