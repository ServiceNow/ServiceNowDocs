---
title: Configure a custom catalog ID in Cloud Account Management account request
description: Configure the catalog ID used for Cloud Account Management request to map the custom service catalog and streamline account provisioning.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up Cloud Account Management in Cloud Workspace, Configure, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Configure a custom catalog ID in Cloud Account Management account request

Configure the catalog ID used for Cloud Account Management request to map the custom service catalog and streamline account provisioning.

## Before you begin

Verify whether the catalog is a valid service catalog tested on various portals, such as the Employee Center.

Role required: sn\_itom\_cam.cw\_admin

## About this task

The Catalog ID uniquely identifies the Catalog used for Cloud Account Management. To map your custom cloud account request catalog, update the default sys\_id value with the custom catalog sys\_id value.

## Procedure

1.  Navigate to **Workspaces** &gt; **Cloud Workspace**.

2.  Enter `sys_properties.list` in the navigation filter.

3.  In the System Properties \[sys\_properties\] table, search for and click the **sn\_itom\_cam.cam\_catalog\_id** record.

4.  In the **Value** field, enter the unique sys\_id of the custom catalog.

    **Note:** You can add only one sys\_id in the **Value** field.

5.  Click **Update**.


