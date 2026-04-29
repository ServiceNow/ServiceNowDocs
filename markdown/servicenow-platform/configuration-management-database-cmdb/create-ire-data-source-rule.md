---
title: Create an IRE data source rule
description: When using Identification and Reconciliation Engine \(IRE\), you can prevent a specific discovery \(data\) source from inserting new CIs for a specific class. Create IRE data source rules for discovery sources that you don't trust in creating CIs but continue to trust in updating those CIs that exist.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create an IRE data source rule

When using Identification and Reconciliation Engine \(IRE\), you can prevent a specific discovery \(data\) source from inserting new CIs for a specific class. Create IRE data source rules for discovery sources that you don't trust in creating CIs but continue to trust in updating those CIs that exist.

## Before you begin

Role required: sn\_cmdb\_admin or itil\_admin

## About this task

IRE data source rules have no impact when dynamic reconciliation rules are in effect.

For example, an IP scan tool that discovers network gear but does not discover servers and therefore creates server CIs without details. You can prevent such discovery source from creating specific CIs, while still permitting it to update those specific CIs if they exist. IRE data source rules are stored in the IRE Data Source Rule \[cmdb\_ire\_data\_source\_rule\] table.

-   Child classes derive IRE data source rules from parent classes like identification rules do.
-   IRE data source rules that are specified for a child class, override any IRE data source rules derived from a parent class.

When IRE processes an insert operation that is prohibited by an IRE data source rule, the insert operation fails. This failure happens when the discovery source and CI class in the insert operation and in an IRE data source rule, match. When [CreateOrUpdateCIEnhanced\(\)](https://www.servicenow.com/docs/access?context=IdentificationEngineScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) is used, IRE stores the failed payload in the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table for future potential use.

**Note:** When an insert operation is not allowed by the IRE data source rule, then when using [createOrUpdateCI\(\)](https://www.servicenow.com/docs/access?context=c_IdentEngineScriptAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US), the entire IRE payload fails since [createOrUpdateCI\(\)](https://www.servicenow.com/docs/access?context=c_IdentEngineScriptAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) doesn't allow partial commits.

If later, a permitted discovery source attempts to insert that same CI, then IRE inserts the CI after merging it with the matching CI from the partial payloads. IRE then deletes the partial payload from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table, and allows future updates by the discovery source specified in the rule.

IRE data source rules do not apply to lookup and related items, and only a single rule can be active for any class/discovery source pair.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **IRE Data Source Rule**.

2.  In the list view, click **New** and fill out the IRE Data Source Rule form.

    |Field|Description|
    |-----|-----------|
    |Active|Activates the IRE data source rule.|
    |Applies to|The class \(and child classes\) that the specified discovery \(data\) source is not allowed to create CIs of.|
    |Data source|Discovery \(data\) source that is not allowed to create CIs of the specified class.|
    |Insert Not Allowed|Disables the specified discovery \(data\) source from inserting new CIs from the specified class, to the CMDB.|

3.  Click **Submit**.


## Result

If a payload item with an insert request, and in which the discovery source and the CI class match the discovery source and the CI class specified in the IRE data source rule:

1.  The insert operation fails and IRE logs the following message:

    INSERT\_NOT\_ALLOWED\_FOR\_SOURCE Insert into \[xyz\] is blocked for data source \[xyz\] by IRE data source rule.

2.  If using [CreateOrUpdateCIEnhanced\(\)](https://www.servicenow.com/docs/access?context=IdentificationEngineScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US), then IRE stores the payload item as a partial payload in the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.

If later, a permitted discovery source successfully inserts a CI that matches the CI from a partial payload item:

1.  The current CI is merged with the matching CI from the partial payload, applying static reconciliation rules as needed.
2.  The respective partial payload in the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table is deleted.
3.  Later payloads in which the non-permitted discovery source updates the respective CI, run successfully.
4.  IRE allows the discovery source, that was previously prohibited from inserting the CI, to update that same CI which now exists in the CMDB.

**Parent Topic:**[Configuring CMDB Identification and Reconciliation](../concept/configuring-ire.md)

