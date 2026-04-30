---
title: Review access to OT knowledge bases for unauthenticated users
description: Review the Operational Technology \(OT\) knowledge bases that are accessible to unauthenticated users by using the user criteria and glide.knowman.block\_access\_with\_no\_user\_criteria property settings.
locale: en-US
release: yokohama
product: Operational Technology Knowledge Management
classification: operational-technology-knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Operational Technology Knowledge Management, Operational Technology]
---

# Review access to OT knowledge bases for unauthenticated users

Review the Operational Technology \(OT\) knowledge bases that are accessible to unauthenticated users by using the user criteria and **glide.knowman.block\_access\_with\_no\_user\_criteria** property settings.

## Before you begin

Role required: knowledge\_admin or admin

## About this task

If you want to restrict unauthenticated users for a knowledge base, you can use the user criteria or the **glide.knowman.block\_access\_with\_no\_user\_criteria** property settings.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Knowledge Bases**.

2.  Review the OT knowledge bases that are accessible to unauthenticated users.

3.  To restrict unauthenticated users for a knowledge base by using the user criteria, select the knowledge base record and update its user criteria.

    For more information about creating the user criteria, see [Create the user criteria for an OT knowledge base](create-user-criteria-otkm.md). For more information about assigning the user criteria, see [Assign the user criteria to an OT knowledge base](assign-ot-user-criteria-otkm.md).

4.  Restrict unauthenticated users for a knowledge base by using the **glide.knowman.block\_access\_with\_no\_user\_criteria** property settings.

    1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Properties**.
    2.  Set the **glide.knowman.block\_access\_with\_no\_user\_criteria** property settings to true.
    3.  Select **Save**.

**Parent Topic:**[Configuring Operational Technology Knowledge Management](../concept/configuring-operational-technology-knowledge-management.md)

