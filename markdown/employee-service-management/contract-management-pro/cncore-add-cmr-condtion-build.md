---
title: Provide access to contract request fields in condition builders
description: As an administrator, provide access to contract request fields so they can be selected in condition builders.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/contract-management-pro/cncore-add-cmr-condtion-build.html
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Add and configure contract request functionality, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Provide access to contract request fields in condition builders

As an administrator, provide access to contract request fields so they can be selected in condition builders.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**

2.  Select the application table whose variables should be used in condition builders.

3.  Add the contract request as a reference field to the table.

    1.  Select the **Columns** tab and select **New**.

    2.  In the **Type** field, select the Lookup using list icon \(\[Omitted image "look-up-icon.png"\] Alt text: Lookup using list icon\) and search for `Reference` and select it.

    3.  Select **Reference Specification** tab.

    4.  In the **Reference** field, select the Contract Request \[sn\_cm\_core\_contract\_request\] table.

    5.  On the Dictionary entry form, fill in the fields.

        For more information, see [Dictionary entry form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/table-administration-and-data-management/r_DictionaryEntryForm.md).

    6.  Select **Submit**.

4.  Select **Update**.


**Parent Topic:**[Add and configure contract request functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/contract-management-pro/cncore-uptake-steps.md)

