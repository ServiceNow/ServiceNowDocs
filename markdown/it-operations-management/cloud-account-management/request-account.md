---
title: Request a cloud account
description: Request a cloud account as a requester. A notification email is sent when the requester creates an account request.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Creating a cloud account, Use, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Request a cloud account

Request a cloud account as a requester. A notification email is sent when the requester creates an account request.

## Before you begin

The ServiceNow admin must have populated the data for the account owner, cost center, business unit, department, and business application.

Role required: sn\_itom\_cam.cw\_requester

## Procedure

1.  Navigate to **All** &gt; **Cloud Workspace**.

2.  From the home page, select **Request**.

3.  On the Request new cloud account form, fill in the fields.

    For a description of the field values, see [New cloud account request form](../reference/account-creation-details.md).

    **Note:** For information about how to create your custom catalog, see [Configure a custom catalog ID in Cloud Account Management account request](configuring-catalog-ids-in-cam-account-request.md).

4.  Request a GovCloud cloud account by selecting the **This is a GovCloud account** check box.

    This action adds additional fields on the new cloud account request form for entering your GovCloud organization details.

    **Note:** GovCloud account creation is supported only for the AWS cloud provider.

5.  Select **Submit**.


