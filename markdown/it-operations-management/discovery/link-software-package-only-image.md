---
title: Link software package information to images only
description: Link software package information to images rather than containers to avoid empty records that associate to short-lived containers.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-03-09"
reading_time_minutes: 1
breadcrumb: [Container image scanning for software decomposition, Kubernetes discovery using patterns, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Link software package information to images only

Link software package information to images rather than containers to avoid empty records that associate to short-lived containers.

## Before you begin

Role required: admin

## About this task

Software package information is linked to both images and containers when the **sn\_itom\_pattern.image\_scan\_process\_container** system property is set to its default value of **true**. To link this data to images only, set the property value to **false**.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** field, search for `sn_itom_pattern.image_scan_process_container`.

3.  Select the **sn\_itom\_pattern.image\_scan\_process\_container** property.

4.  In the **Value** field, enter `false`.

5.  Select **Update**.


**Parent Topic:**[Container image scanning for software decomposition](../concept/container-image-concept.md)

**Related topics**  


[Scan container images](container-image-task.md)

[Container image discovery](../reference/container_image_scan_pattern.md)

