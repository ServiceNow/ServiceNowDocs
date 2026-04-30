---
title: Create a basic authentication configuration to migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Authenticate the Table API that the migration utility uses to perform creation, updating, and deletion of records.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Create a basic authentication configuration to migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM

Authenticate the Table API that the migration utility uses to perform creation, updating, and deletion of records.

## Before you begin

Role required: admin

## About this task

This configuration must contain the credentials of the user who is logged in and has the admin role.

## Procedure

1.  From the **All** menu, in the navigation filter, enter **sys\_auth\_profile\_basic.list**.

2.  On the Basic Auth Configurations page, select **New**.

3.  On the Basic Auth Configuration form, specify the name, user name, and password.

4.  Select **Submit**.


**Parent Topic:**[Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](../concept/migration-from-itsm-aw-sow.md)

