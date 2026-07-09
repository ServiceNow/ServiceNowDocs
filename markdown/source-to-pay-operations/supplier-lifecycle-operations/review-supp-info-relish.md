---
title: Review supplier information using Relish
description: Using Relish integration, checking supplier's banking details, physical addresses, and sanction screening can be done efficiently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/source-to-pay-operations/supplier-lifecycle-operations/review-supp-info-relish.html
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Source-to-Pay Workspace Supplier page, Using Source-to-Pay Workspace, Using Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Review supplier information using Relish

Using Relish integration, checking supplier's banking details, physical addresses, and sanction screening can be done efficiently.

**Important:** Check your entitlements to determine whether you have access to Relish integration.

The details of the following case types in the **Review supplier primary data request** playbook can be verified using Relish integration:

-   Banking information change request
-   Supplier location change request
-   Conduct sanction screening

For more information on required and dependent plugins for Relish, see [Relish Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/supplier-lifecycle-operations/relish-slo-connector.md).

## Verifying Supplier location change request

When a location change request is assigned to a supplier manager and they start working on it, they can verify the new location by clicking **Validate**.

\[Omitted image "validate.png"\] Alt text: Verify supplier information

Clicking the **Validate** button invokes the Relish verification process.

\[Omitted image "validate-relish.png"\] Alt text: Screen showing Please wait while Relish is verifying information message

It takes few minutes for Relish to complete the verification process. Depending on the result, the supplier manager can approve or reject the request.

\[Omitted image "validate-approve.png"\] Alt text: Approve or reject changes

Also, a notification can be sent to the requester.

\[Omitted image "validate-email.png"\] Alt text: Notify the supplier

**Parent Topic:**[Source-to-Pay Workspace Supplier page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/source-to-pay-workspace/supp-ws-details-page.md)

**Related topics**  


[Playbook for updating the supplier primary data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/supplier-lifecycle-operations/primary-playbook-cases.md)

