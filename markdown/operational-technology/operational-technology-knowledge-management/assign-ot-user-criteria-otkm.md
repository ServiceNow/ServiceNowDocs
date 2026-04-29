---
title: Assign the user criteria to an OT knowledge base
description: Assign the user criteria records to an Operational Technology \(OT\) knowledge base to control which users can create, read, write, and retire knowledge articles within the knowledge base.
locale: en-US
release: australia
product: Operational Technology Knowledge Management
classification: operational-technology-knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Operational Technology Knowledge Management, Operational Technology]
---

# Assign the user criteria to an OT knowledge base

Assign the user criteria records to an Operational Technology \(OT\) knowledge base to control which users can create, read, write, and retire knowledge articles within the knowledge base.

## Before you begin

Role required: knowledge\_manager, knowledge\_admin, or admin

## About this task

You can assign user criteria to an OT knowledge base to control read or contribute access.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Knowledge Bases**.

2.  Select the OT knowledge base record that you want to manage.

3.  Add the user criteria to the OT knowledge base.

    1.  Depending on the user criteria that you want to set, select one or more of the related lists.

        |Related list|Description|
        |------------|-----------|
        |Can Read|Users can read knowledge articles in the knowledge base.|
        |Cannot Read|Users can't read knowledge articles in the knowledge base.|
        |Can Contribute|Users can create, modify, and retire knowledge articles in a knowledge base. Contribute access to a knowledge base also provides read access to all articles in the knowledge base.|
        |Cannot Contribute|Users can't create, modify, retire, or read knowledge articles in the knowledge base.|

    2.  In the selected related list, add the required user criteria.
        -   As a user with the admin role, add a new user criteria record by selecting **New**, specifying the required fields, and selecting **Submit**.
        -   As a user with the knowledge\_manager, knowledge\_admin, or admin role, add an existing user criteria record by selecting **Edit**, moving the required user criteria from the Collection column to the Knowledge column, and selecting **Save**.
4.  On the knowledge base form, select **Update**.


**Parent Topic:**[Configuring Operational Technology Knowledge Management](../concept/configuring-operational-technology-knowledge-management.md)

