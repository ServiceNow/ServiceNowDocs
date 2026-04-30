---
title: Create an IRE data source rule for non-CMDB tables
description: When using Identification and Reconciliation Engine \(IRE\), you can prevent a specific data source from inserting new records for a specific non-CMDB table. Create IRE data source rules for data sources that you don't trust in creating records but continue to trust in updating those records that exist.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [IRE support for non-CMDB tables, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create an IRE data source rule for non-CMDB tables

When using Identification and Reconciliation Engine \(IRE\), you can prevent a specific data source from inserting new records for a specific non-CMDB table. Create IRE data source rules for data sources that you don't trust in creating records but continue to trust in updating those records that exist.

## Before you begin

Role required: itil\_admin

## About this task

IRE data source rules have no impact when dynamic reconciliation rules are in effect.

-   Child classes derive IRE data source rules from parent classes like identification rules do.
-   IRE data source rules that are specified for a child class, override any IRE data source rules derived from a parent class.

When IRE processes an insert operation that is prohibited by an IRE data source rule, the insert operation fails. This failure happens when the data source and record class in the insert operation and in an IRE data source rule, match. When [CreateOrUpdateCIEnhanced\(\)](https://www.servicenow.com/docs/access?context=IdentificationEngineScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) is used, IRE stores the failed payload in the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table for future potential use.

**Note:** When an insert operation is not allowed by the IRE data source rule, then when using [createOrUpdateCI\(\)](https://www.servicenow.com/docs/access?context=c_IdentEngineScriptAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US), the entire IRE payload fails since [createOrUpdateCI\(\)](https://www.servicenow.com/docs/access?context=c_IdentEngineScriptAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) doesn't allow partial commits.

If later, a permitted data source attempts to insert that same record, then IRE inserts the record after merging it with the matching record from the partial payloads. IRE then deletes the partial payload from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table, and allows future updates by the data source specified in the rule.

IRE data source rules do not apply to lookup and related items, and only a single rule can be active for any class/data source pair.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **IRE Data Source Rules**.

2.  In the IRE Data Source Rules list view, click **New** and fill out the IRE Data Source Rule form.

    |Field|Description|
    |-----|-----------|
    |Data source|Data source that is not allowed to create CIs of the specified class.|
    |Active|Activates the IRE data source rule.|
    |Applies to|The class \(and child classes\) that the specified data source is not allowed to create records for.|
    |Insert Not Allowed|Disables the specified data source from inserting new records of the specified class, to the non-CMDB table.|

3.  Click **Submit**.


## Result

If a payload item with an insert request, and in which the data source and the record class match the data source and the record class specified in the IRE data source rule:

1.  The insert operation fails and IRE logs the following message:

    INSERT\_NOT\_ALLOWED\_FOR\_SOURCE Insert into \[xyz\] is blocked for data source \[xyz\] by IRE data source rule.

2.  If using [CreateOrUpdateCIEnhanced\(\)](https://www.servicenow.com/docs/access?context=IdentificationEngineScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US), then IRE stores the payload item as a partial payload in the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.

If later, a permitted data source successfully inserts a record that matches the record from a partial payload item:

1.  The current record is merged with the matching record from the partial payload, applying static reconciliation rules as needed.
2.  The respective partial payload in the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table is deleted.
3.  Later payloads in which the non-permitted data source updates the respective record, run successfully.
4.  IRE allows the data source, that was previously prohibited from inserting the record, to update that same record which now exists in the non-CMDB table.

**Parent Topic:**[IRE support for non-CMDB tables](../concept/ire-support-non-cmdb-tables.md)

