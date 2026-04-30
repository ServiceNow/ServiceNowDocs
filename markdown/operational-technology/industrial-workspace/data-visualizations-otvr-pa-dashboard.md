---
title: Data visualizations used in the Operational Technology Vulnerability Response \(PA\) dashboard
description: The Operational Technology Vulnerability Response \(PA\) dashboard uses data visualizations to display your OT vulnerability data.
locale: en-US
release: yokohama
product: Industrial Workspace
classification: industrial-workspace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Use, Industrial Workspace, Operational Technology]
---

# Data visualizations used in the Operational Technology Vulnerability Response \(PA\) dashboard

The Operational Technology Vulnerability Response \(PA\) dashboard uses data visualizations to display your OT vulnerability data.

The following tables describe the data visualizations shown in the Operational Technology Vulnerability Response \(PA\) dashboard.

<table id="table_phw_wcb_vzb"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total OT Vulnerable Items

</td><td>

Bar

</td><td>

Bar chart that displays the active \(non-closed\) OT vulnerable items grouped by device type.

</td></tr><tr><td>

New OT Vulnerable Items

</td><td>

Pie

</td><td>

Pie chart that displays the new OT vulnerable items that were found in your system grouped by device type.

</td></tr><tr><td>

OT Unassigned Vulnerable Items

</td><td>

Pie

</td><td>

Pie chart that displays the OT vulnerable items grouped by device type that are open and haven't been assigned to a user.

</td></tr><tr><td>

OT Vulnerable Items by State

</td><td>

Bar

</td><td>

Bar chart that displays all the vulnerable items by state. You can interpret how many vulnerabilities are being addressed and how many need further investigation. For example, if the **Under Investigation** category is relatively high, you can prioritize these items by addressing those vulnerable items first.

</td></tr><tr><td>

OT Vulnerable Items by Risk Rating

</td><td>

Bar

</td><td>

Number of the active OT vulnerable items that are grouped by the risk rating over the selected time span.

</td></tr><tr><td>

OT VIs Met Remediation Target

</td><td>

Singe score

</td><td>

Percentage of the closed OT vulnerable items that have met their remediation target dates in the current and previous quarters.Remediation targets are calculated from the Last Opened date plus the number of days since the Last Opened date \(measured as 24-hour increments\).

</td></tr><tr><td>

OT VI Mean Time to Remediate \(MTTR\)

</td><td>

Single score

</td><td>

Mean time to remediate \(close\) an OT vulnerable item, displayed as a 30-day running average. **Note:** The value for Age Closed is calculated when the data is collected. The value is the difference between the last\_opened date and the date and time of the collection job.

</td></tr><tr><td>

OT VI by age

</td><td>

Bar

</td><td>

Bar chart that displays the OT active vulnerable items grouped by age \(in days\).

</td></tr><tr><td>

OT Closed Vulnerable Items by Remediation Target Status

</td><td>

Bar

</td><td>

Number of the closed OT vulnerable items that are grouped by the remediation target status over the selected time span. **Note:** The value for Age Closed is calculated when the data is collected. The value is the difference between the last\_opened date and the date and time of the collection job.

</td></tr><tr><td>

OT Critical Vulnerable Item by Assignment Group

</td><td>

Indicator scorecard

</td><td>

Critical VIs organized by assignment group.

</td></tr><tr><td>

OT Overdue Critical Vulnerable Items by Assignment Group

</td><td>

Indicator scorecard

</td><td>

Critical VIs that are overdue organized by assignment group.

</td></tr></tbody>
</table><table id="table_etw_xcb_vzb"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OT Remediation Tasks

</td><td>

Single score

</td><td>

Number of the active \(non-closed\) OT remediation tasks.

</td></tr><tr><td>

OT Critical Remediation Tasks Near Due

</td><td>

Single score

</td><td>

Number of the active OT remediation tasks that are approaching their remediation target date.

 The remediation target date of an OT remediation task is set to the closest due date that belongs to an active vulnerable item in the group.

 The remediation targets are calculated from the Last Opened date plus the number of days \(measured as 24-hour increments\).

 This report excludes the deferred OT remediation tasks.

</td></tr><tr><td>

OT Remediation Task by Risk rating

</td><td>

Bar

</td><td>

Bar chart that displays the active OT remediation tasks grouped by the risk rating.

</td></tr><tr><td>

OT Remediation Task by Target Status

</td><td>

Bar

</td><td>

Bar chart that displays the active OT remediation tasks grouped by the remediation target status.This report excludes the deferred OT vulnerable items.

</td></tr><tr><td>

OT Remediation Task by State

</td><td>

Bar

</td><td>

Bar chart that displays all the remediation tasks by state. You can interpret the progress of your remediation tasks.

</td></tr><tr><td>

OT Unassigned Remediation Tasks

</td><td>

Single score

</td><td>

Number of the active OT remediation tasks without an assignee or assignment group.

</td></tr><tr><td>

OT Critical Remediation Task by Assignment Group

</td><td>

Indicator scorecard

</td><td>

Critical remediation tasks organized by assignment group.

</td></tr><tr><td>

OT Overdue Critical Remediation Task by Assignment Group

</td><td>

Indicator scorecard

</td><td>

Critical remediation tasks that are overdue organized by assignment group.

</td></tr></tbody>
</table>|Name|Type|Description|
|----|----|-----------|
|OT Deferred Vulnerable Items by Reason|Bar|Number of the deferred OT vulnerable items that are grouped by the deferral reason.|
|OT Exceptions for Critical Vulnerable Items by Assignment Group|Indicator scorecard|Exceptions for critical VIs organized by assignment group.|

**Parent Topic:**[Using the Industrial Workspace](../../operational-technology-management/concept/using-industrial-workspace.md)

