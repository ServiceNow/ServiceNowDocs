---
title: Migrate the server script from ITSM Agent Workspace to Service Operations Workspace for field decorators actions
description: Configure the server script to migrate field decorators actions from ITSM Agent Workspace to Service Operations Workspace.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration, Service Operations Workspace for ITSM, IT Service Management]
---

# Migrate the server script from ITSM Agent Workspace to Service Operations Workspace for field decorators actions

Configure the server script to migrate field decorators actions from ITSM Agent Workspace to Service Operations Workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **Field Decorators**.

2.  Filter the records based for **Implemented As** is set as **Server script**.

3.  View the log in the failed record in the migration process and find the **sys\_Id** of the record from the list of **Related List Actions**.

4.  Select the failed record with the corresponding sys\_id.

5.  Right-click on the header, and select **Insert and Stay**.

6.  Clear the **Workspace** and **View** fields.

7.  Select the **Experience Restricted** check box.

8.  In the **Action configuration** related list, select **Edit**, and then select **SOW Actions** from **Collection** to **Action configurations** list.

9.  Select **Save** to save the **Action configurations** related list.

10. Select **Update**.


**Parent Topic:**[Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/field-declarative-actions-aw-sow.md)

