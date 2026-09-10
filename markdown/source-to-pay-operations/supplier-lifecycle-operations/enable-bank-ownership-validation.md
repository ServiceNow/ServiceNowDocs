---
title: Enable bank account ownership validation
description: Configure the bank validation flow to include bank account ownership validation in addition to standard bank details validation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/enable-bank-ownership-validation.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 1
keywords: [bank ownership validation, bank validation, relish]
breadcrumb: [Verify banking information, Review supplier information using Relish, Manage supplier cases, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Enable bank account ownership validation

Configure the bank validation flow to include bank account ownership validation in addition to standard bank details validation.

## Before you begin

Ensure that the SLO Connector for Relish Data Assure plugin \(x\_reliq\_slo\_connec\) is installed. For more information on the required and dependent plugins for Relish, see [Relish Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/relish-slo-connector.md).

Role required: admin

## About this task

By default, bank validation checks only the bank routing number and address details. When bank account ownership validation is enabled, Relish also verifies the bank account number and account ownership information.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Search for and open the `Bank Details Validation` flow.

3.  In the flow, locate the fourth step that contains the **Use Bank Information for Ownership** option.

4.  Set the **Use Bank Information for Ownership** option to **Yes**.

    When set to Yes, Relish validates both bank details and bank account ownership. When set to No, Relish validates only bank routing numbers and address details.

5.  Save and publish the flow.


## Result

After enabling bank account ownership validation, all banking information change requests are validated for both bank details and account ownership. The overall validation result is determined by the least favorable outcome:

-   If bank details validation passes and ownership validation fails, the overall result is failed
-   If bank details validation passes and ownership validation passes with cautions, the overall result is passed with cautions
-   If both validations pass, the overall result is passed

**Parent Topic:**[Verify banking information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/verify-banking-information.md)

**Related topics**  


[Verify banking information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/verify-banking-information.md)

