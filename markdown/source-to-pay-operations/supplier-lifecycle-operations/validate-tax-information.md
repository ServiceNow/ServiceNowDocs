---
title: Verify tax information
description: When a tax information change request is assigned to a supplier manager and they start working on it, they can verify the tax details using Relish.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/validate-tax-information.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 1
keywords: [tax validation, tax information, relish, supplier tax]
breadcrumb: [Review supplier information using Relish, Manage supplier cases, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Verify tax information

When a tax information change request is assigned to a supplier manager and they start working on it, they can verify the tax details using Relish.

## Before you begin

Ensure that the SLO Connector for Relish Data Assure plugin \(x\_reliq\_slo\_connec\) is installed. For more information on the required and dependent plugins for Relish, see [Relish Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/relish-slo-connector.md).

Role required: sn\_slm.manager, sn\_slm.owner, or sn\_slm.admin

## About this task

Tax information change requests can be created by supplier managers or submitted by suppliers through the supplier portal. Each supplier can have only one tax record per country.

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Navigate to **Lists** &gt; **All work** &gt; **Cases**.

3.  Open the case for the tax information change request.

    The **Review supplier primary data request** playbook opens.

4.  Select **Start work** to initiate the process.

5.  If the Relish plugin is installed, select **Validate** to invoke the Relish verification process.

    It takes a few minutes for Relish to complete the verification process. The validation result appears in the case, showing one of the following statuses:

    -   **Passed**: Tax information is valid
    -   **Failed**: Tax information is invalid
    -   **Bypass**: Country is not supported for tax validation
    If the Relish plugin is not installed, the **Approve changes** and **Reject changes** options appear directly without validation.

6.  Approve or reject changes based on the validation result.

7.  Select **Accept** to verify that the changes are made in other systems, if required.

8.  Notify the supplier by email.

9.  Close the case.


-   **[View supplier tax information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/view-supplier-tax-information.md)**  
Supplier managers can view all tax information records for a supplier from the supplier record.

**Parent Topic:**[Review supplier information using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/review-supp-info-relish.md)

**Related topics**  


[Conduct sanction screening](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/conduct-sanction-screening.md)

[Verify banking information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/verify-banking-information.md)

[Update tax information using the supplier catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/submit-tax-information-from-portal.md)

