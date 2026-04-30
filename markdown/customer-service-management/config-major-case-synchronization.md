---
title: Configure case synchronization
description: Configure the major issue management system properties to enable synchronization between major cases and associated child cases.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure major issue management, Configure case management, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configure case synchronization

Configure the major issue management system properties to enable synchronization between major cases and associated child cases.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Properties**.

2.  Enable the **Synchronize fields from parent to child case** property.

3.  In the **Comma separated list of fields that synchronize from parent to child cases** property, add a comma-separated list of fields that synchronize from the major case to each of the associated child cases.

4.  Set the **Processes SLA asynchronously during parent to child case creation and synchronization** property to false to process the SLA synchronously.

    This property is enabled by default.

5.  Click **Save**.


