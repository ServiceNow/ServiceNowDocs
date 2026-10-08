---
title: Modify risk and Request risk modification form fields
description: The following table shows the fields on the Modify risk and Request risk modification dialogs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/sem-modify-risk-form.html
release: australia
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [Modify risk, Request risk modification]
breadcrumb: [Modify the risk rating for a finding or remediation task, Use, Unified Security Exposure Management, Security Operations]
---

# Modify risk and Request risk modification form fields

The following table shows the fields on the **Modify risk** and **Request risk modification** dialogs.

<table id="table_smrf"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New risk rating

</td><td>

Risk rating to apply to the record.

</td></tr><tr><td>

Compensating control \(Optional\)

</td><td>

A compensating control to associate with the risk modification.Only controls associated with the affected findings appear in the list. If no controls are associated with the vulnerability, all active controls from the library will appear.

</td></tr><tr><td>

Justification

</td><td>

Reason for the risk modification.

</td></tr><tr><td>

Risk adjusted until

</td><td>

Date on which the risk rating expires and the record reverts to its calculated risk rating.-   Remediation Owner: Required.
-   Vulnerability Admin/Analyst: Optional. If you leave this field empty, the adjusted risk rating applies indefinitely.

You can't select a past date. The maximum number of days you can select is determined by the **Maximum duration for exception \(days\)** field in the Exception Management form.

</td></tr></tbody>
</table>**Parent Topic:**[Modify the risk rating for a finding or remediation task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/sem-modify-risk.md)

**Related topics**  


[Modify the risk rating for a finding or remediation task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/sem-modify-risk.md)

