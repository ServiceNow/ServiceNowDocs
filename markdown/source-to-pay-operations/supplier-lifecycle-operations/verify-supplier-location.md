---
title: Verify supplier location change request
description: When a location change request is assigned to a supplier manager and they start working on it, they can verify the new location using Relish.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/verify-supplier-location.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 1
breadcrumb: [Review supplier information using Relish, Manage supplier cases, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Verify supplier location change request

When a location change request is assigned to a supplier manager and they start working on it, they can verify the new location using Relish.

## Before you begin

Ensure that the SLO Connector for Relish Data Assure plugin \(x\_reliq\_slo\_connec\) is installed. For more information on the required and dependent plugins for Relish, see [Relish Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/relish-slo-connector.md).

Role required: sn\_slm.manager, sn\_slm.owner, or sn\_slm.admin

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Navigate to **Lists** &gt; **All work** &gt; **Cases**.

3.  Open the case for the supplier location change request which needs to be verified.

    The **Review supplier primary data request** playbook opens.

4.  Select **Validate** to invoke the Relish verification process.

    It takes a few minutes for Relish to complete the verification process. Depending on the result, the supplier manager can approve or reject the request.

    \[Omitted image "relish-location-change.png"\] Alt text: Screen showing Wait while Relish is verifying information message

    For more about the parameters sent to and received from Relish, see [Address verification parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/location-change-request-response.md).

5.  Approve or reject changes.

6.  Notify the supplier by email.

7.  Close the case.


-   **[Address verification parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/location-change-request-response.md)**  
Request and response parameters for location change requests sent to and received from the Relish Data Assure API.

**Parent Topic:**[Review supplier information using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/review-supp-info-relish.md)

**Related topics**  


[Verify banking information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/verify-banking-information.md)

[Conduct sanction screening](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/conduct-sanction-screening.md)

[Playbook for updating the supplier primary data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/primary-playbook-cases.md)

