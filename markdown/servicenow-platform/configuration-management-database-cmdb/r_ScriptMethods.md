---
title: Script methods
description: ServiceNow provides four methods for creating the audit script.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Scripted audits, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Script methods

ServiceNow provides four methods for creating the audit script.

<table id="table_h1y_st3_5q"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Parameters

</th></tr></thead><tbody><tr><td>

getFilterRecords

</td><td>

public GlideRecord getFilterRecords\(String filterId\)

</td><td>

filterID: The sys\_id of the filter to use.

</td></tr><tr><td>

logAuditResultPass

</td><td>

public void logAuditResultPass\(String auditId, String auditedRecordId, boolean isCI, String domainToUse\)

</td><td>

auditId: Sys\_id of audit record executed

 auditedRecordId: Sys\_id of the record audited.

 isCI: True, if the audited record is a CI, false if otherwise.

 domainToUse: Sys\_domain of the cert\_audit record.

</td></tr><tr><td>

logAuditResultFail

</td><td>

public void logAuditResultFail\(String auditId, String auditedRecordId, String followOnTask, String columnDisplayName, String operatorLabel, String desiredValue, String discrepancyValue, boolean isCI, String domainToUse\)

</td><td>

auditId: Sys\_id of audit record executed.

 auditedRecordId: Sys\_id of the record audited.

 followOnTask: Sys\_id of the follow-on task associated with the audited record and can be an empty string.

 columnDisplayName: Label of the column audited. For example, Disk space \(GB\).

 operatorLabel: Label of the operator used to audit the column. For example, is not empty or greater than can be the label.

 desiredValue: Desired value of the column.

 discrepancyValue: Discrepancy value.

 isCI: True, if the audited record is a CI, false if otherwise.

 domainToUse: Sys\_domain of the cert\_audit record.

</td></tr><tr><td>

createFollowOnTask\(\)

</td><td>

public String createFollowOnTask\(String auditId, String ciId, String assignedTo, String assignmentGroup, String shortDescr\)

</td><td>

auditId: Sys\_id of the audit record executed.

 ciId: Sys\_id of the configuration item. This string is empty when the table is not extended from the cmdb\_ci table.

 assignedTo: Sys\_id of the assigned user of the task. This string can be empty.

 assignmentGroup: Sys\_id of the group the task is assigned to. This string can be empty.

 shortDescr: The text to use for the short description of the follow-on task.

</td></tr></tbody>
</table>