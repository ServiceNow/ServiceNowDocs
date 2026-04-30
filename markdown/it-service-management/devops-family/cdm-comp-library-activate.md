---
title: Activate a component library
description: Activate a component library to make all of its shared components available for use.
locale: en-US
release: xanadu
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Sharing components among applications — Component libraries, Use, DevOps Config, IT Service Management]
---

# Activate a component library

Activate a component library to make all of its shared components available for use.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: cdm\_admin

## About this task

A library can be in the Unavailable state in the following situations:

-   When a library is created for the first time
-   When a library and its components are being created
-   When a newer version of the library is being created

If a library is unavailable, no component within that library can be used, updated, or exported. However, it does not impact applications that are already using components within this library.

When the library is ready for use, you can activate it.

## Procedure

1.  Navigate to **All** &gt; **DevOps Config** &gt; **DevOps Config Workspace**.

2.  Click the component libraries icon \(![Component libraries icon.](../image/icon-component-libraries.png)\) in the left navigation to open the **Component libraries** tab.

3.  In the left pane, select a component library.

4.  Select the **Available** toggle switch to make the library available so that its shared components can be used in applications.


## Result

-   The library and the shared components in it become available for use.
-   The status of the library is set as Available.

