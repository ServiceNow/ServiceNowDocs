---
title: Query AD activity
description: The Query AD activity retrieves entries from the Windows Active Directory based on an LDAP search filter and stores the results as a JSON string that can be used in the data bus.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Active Directory activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Query AD activity

The Query AD activity retrieves entries from the Windows Active Directory based on an LDAP search filter and stores the results as a JSON string that can be used in the data bus.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory** &gt; **.**

**Note:** This activity replaces an AD activity by the same name available in releases prior to Geneva. If you have a workflow that uses the deprecated activity, your workflow will continue to work normally after upgrading to Instanbul and will continue to save query results to the scratchpad. However, all new workflows must use the custom version of this activity. This activity was built with the [Create a PowerShell activity](../../orchestration-activity-designer/task/t_CreateAPowershellActivity.md#), which stores input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#) instead of the scratchpad.

## Input variables

<table id="table_qjs_44h_dp"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DomainController

</td><td>

IP address of the domain controller machine.

</td></tr><tr><td>

Properties

</td><td>

A comma-separated list of Active Directory properties to return. For example, **givenName,SN,title**. If this field is blank, then all properties are returned.

</td></tr><tr><td>

SearchFilter

</td><td>

An LDAP filter string that defines the search parameters. Use any valid LDAP filtering criteria. For example, to find user accounts matching the ServiceNow input record, use:```
(samaccountname=${workflow.inputs.u_user.user_name})
```

</td></tr></tbody>
</table>## Output variables

|Variable|Description|
|--------|-----------|
|result|Either **success** or **failure**.|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#).|
|output|The query result.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The query completed as expected.|
|Failure|An error occurred while processing the query. Additional details may be available in the workflow log.|

**Parent Topic:**[Active Directory activity pack](../concept/c_OrchActiveDirectoryActivities.md)

