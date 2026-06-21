---
title: Publish a contract template
description: Publish a contract template to make it available for generating a standard contract document with predefined content when a contract user submits a request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/contract-management-pro/cncore-publish-template.html
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure contract templates for a contract request, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Publish a contract template

Publish a contract template to make it available for generating a standard contract document with predefined content when a contract user submits a request.

## Before you begin

Ensure that the clause mapping has been completed before you publish a contract template with clauses. For more information, see [Complete clause mapping to build a clause library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/contract-management-pro/cncore-clause-map-addin.md) and [Classify and map imported clauses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/contract-management-pro/cncore-import-clauses.md).

Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contracts Template**.

2.  Open a contract template.

3.  Review the contract document.

    1.  Generate and preview the contract document.

        For more information, see [Generate and preview a contract document from a template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/contract-management-pro/cncore-preview-template.md).

    2.  If any changes are necessary, update the document and save it.

4.  On finalizing the content of the contract document, select **Publish**.


## Result

The contract template is published.

**Note:** If the contract type associated with the contract template is deactivated when the contract template is in the Draft or Editing state, an error is displayed when you try to publish the template.

