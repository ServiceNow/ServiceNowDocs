---
title: Add an entitlement to a case
description: Add one or more entitlements to a customer service case record in CSM Configurable Workspace.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage cases, Use, Customer Service Management]
---

# Add an entitlement to a case

Add one or more entitlements to a customer service case record in CSM Configurable Workspace.

## Before you begin

Role required: sn\_esm\_agent, sn\_customerservice.consumer\_agent

## About this task

Agents can view the available entitlements on a customer service case and associate one or more entitlements to the case. Available entitlements are associated with the account, consumer, or contract selected on the case record.

Starting with the Zurich release, the **sn\_customerservice.advanced\_entitlements** system property determines if agents can associate one entitlement to a case or multiple entitlements.

-   If set to true, the Case Entitlements related list is visible on the Case form and the **Entitlement** field is hidden. Agents can use this list to associate multiple entitlements to the case.
-   If set to false, the **Entitlement** field is visible on the Case form and the Case Entitlements related list is hidden. Agents can use this field to associate one entitlement to the case.

For more information, see [Properties installed with Customer Service Management](../reference/r_PropInstallWcustServ.md).

## Procedure

1.  Open a case record in CSM Configurable Workspace.

2.  Add one or more entitlements to the case.

3.  Select the Case Entitlements related list tab and then select **Add**.

    If the record page displays the Related Lists tab in the contextual side panel, expand the Case Entitlements list and then select **View all** to display the Case Entitlements list.

4.  Select one or more entitlements from the Add case entitlements pop-up window.

    The Add entitlements pop-up window displays the entitlements associated with the account, consumer, product, and contract selected on the case record.

5.  Select **Add** on the Add case entitlements pop-up window.

    The selected entitlements are added to the Case Entitlements list.

6.  Select **Save** to save the changes to the case.


