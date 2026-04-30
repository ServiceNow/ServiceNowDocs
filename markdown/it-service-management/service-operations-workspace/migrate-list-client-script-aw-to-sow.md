---
title: Migrate the client script from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Configure the client script to migrate list actions from ITSM Agent Workspace to Service Operations Workspace for ITSM.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration, Service Operations Workspace for ITSM, IT Service Management]
---

# Migrate the client script from ITSM Agent Workspace to Service Operations Workspace for ITSM

Configure the client script to migrate list actions from ITSM Agent Workspace to Service Operations Workspace for ITSM.

## Before you begin

When performing the migration, you must have selected the **List actions** option for ITSM Agent Workspace features. For example, the **List actions** option for List. For information about the migration process, see [Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](migrate-itsm-agent-workspace-to-sow.md).

Role required: admin

## About this task

At the end of the migration process, a confirmation message specifies if the migration is successful or not. You can review the migration information and perform the post-migration steps to confirm successful migration of your configuration or customization.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **List actions**.

2.  Filter the records based for **Implemented As** is set as **Client script**.

3.  View the log in the failed record in the migration process and find the **sys\_Id** of the record from the list of **List Actions**.

4.  Select the failed record with the corresponding sys\_id.

5.  Select and hold \(or right-click\) on the header, and select **Insert and Stay**.

6.  Clear the **Workspace** and **View** fields.

7.  Select the **Experience Restricted** check box.

8.  In the **Action configuration** related list, select **Edit**, and then select **SOW Actions** from **Collection** to **Action configurations** list.

9.  Select **Save** to save the **Action configurations** list.

10. Select **Update**.


**Parent Topic:**[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/list-actions-migration-itsm-aw-sow.md)

