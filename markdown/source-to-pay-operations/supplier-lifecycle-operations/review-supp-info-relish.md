---
title: Review supplier information using Relish
description: Using Relish integration, checking supplier's banking details, physical addresses, and sanction screening can be done efficiently.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage supplier details, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Review supplier information using Relish

Using Relish integration, checking supplier's banking details, physical addresses, and sanction screening can be done efficiently.

**Important:** Check your entitlements to determine whether you have access to Relish integration.

The details of the following case types in the **Review supplier primary data request** playbook can be verified using Relish integration:

-   Banking information change request
-   Supplier location change request
-   Conduct sanction screening

For more information on required and dependent plugins for Relish, see [Relish Integration for Supplier Lifecycle Operations](relish-slo-connector.md).

## Verifying Supplier location change request

When a location change request is assigned to a supplier manager and they start working on it, they can verify the new location by clicking **Validate**.

![Verify supplier information](../image/validate.png "Verify supplier information")

Clicking the **Validate** button invokes the Relish verification process.

![Screen showing Please wait while Relish is verifying information message](../image/validate-relish.png "Verify supplier information using Relish")

It takes few minutes for Relish to complete the verification process. Depending on the result, the supplier manager can approve or reject the request.

![Approve or reject changes](../image/validate-approve.png "Approve or reject changes")

Also, a notification can be sent to the requester.

![Notify the supplier](../image/validate-email.png "Notify the supplier")

**Parent Topic:**[Manage supplier details](supp-ws-details-page.md)

**Related topics**  


[Playbook for updating the supplier primary data](primary-playbook-cases.md)

