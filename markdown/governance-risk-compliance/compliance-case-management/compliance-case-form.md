---
title: Compliance Case form
description: Use the Create Compliance Case form in the GRC: Compliance Case Management application to report a compliance case.
locale: en-US
release: australia
product: Compliance Case Management
classification: compliance-case-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Create compliance case form, Report compliance case, Use, Compliance Case Management, Governance, Risk, and Compliance]
---

# Compliance Case form

Use the Create Compliance Case form in the GRC: Compliance Case Management application to report a compliance case.

See the following table for a description of the field values.

<table id="table_uj1_q5x_nvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number of the case. This field is automatically set to a case number.

</td></tr><tr><td>

Name

</td><td>

Name of the case. For example, Verdict of a lawsuit leaked.

</td></tr><tr><td>

Type

</td><td>

Type of the case. This field is automatically set to **Compliance case**.

</td></tr><tr><td>

Sub-type

</td><td>

Sub-type of the case. For example, Fraud and Embezzlement.

</td></tr><tr><td>

State

</td><td>

Workflow state of the case. This field is automatically set to **New**.

</td></tr><tr><td>

Priority

</td><td>

Priority of the case:-   **1 - Critical**
-   **2- High**
-   **3 - Moderate**
-   **4 - Low**
-   **5 - Planning**

</td></tr><tr><td>

Requester

</td><td>

Person who reported the case.

</td></tr><tr><td>

Requested on behalf of

</td><td>

Name of the person you created the case for.

</td></tr><tr><td>

Primary entity

</td><td>

Entity that is affected by the case. This field is automatically set to the entity that is identified in the Impacted areas related list.

</td></tr><tr><td>

Entity owner

</td><td>

User who is the owner of the entity. This field is automatically set based on the entity that is selected in the Impacted areas related list.

</td></tr><tr><td>

Description

</td><td>

Brief description of the case.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Assignment group

</td><td>

Group that is assigned to the case.**Note:** The assignment group is preconfigured to the case type during the configuration setup.

</td></tr><tr><td>

Watch list

</td><td>

User who must be informed about the case.

</td></tr><tr><td>

Case analyst

</td><td>

Analyst who can analyze and work on the case. The case analyst is a part of the assignment group.

</td></tr><tr><td>

Accountable executive

</td><td>

Executive who is accountable for the case.

</td></tr><tr><td class="sub-head" colspan="2">

Primary origin

</td></tr><tr><td>

Location

</td><td>

Location where the case occurred. For example, Japan.

</td></tr><tr><td>

Sub-location

</td><td>

Sub-location of the case occurrence. For example, the sub location is Tokyo.

</td></tr><tr><td>

Impacted business unit

</td><td>

Business unit that is affected by the reported cases or events. For example, Finance.

</td></tr><tr><td>

Impacted department

</td><td>

Department that is affected by the case. For example, Customer support.

</td></tr><tr><td>

Source

</td><td>

Source from which the case is reported: -   **Manual**: When the case is created from the compliance workspace, the field displays the source as **Manual**.
-   **Employee Center**: When the case is reported from the Employee Center, the field displays the source as **Employee Center**.

</td></tr><tr><td>

Source record

</td><td>

Source record of the source object from where the case is created. For example, if the case is reported from risk events, then this field displays the name of the risk event from which the case is reported.

</td></tr><tr><td>

Additional source

</td><td>

Mode of how the case is reported when the case is created manually. This field is available only when **Manual** is selected from the **Source** field and the record is saved. The choices are as follows:-   **Email**: When you create the case from the information that you received in an email.
-   **Phone**: When you create the case from the information that you received in a phone call.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Date of occurrence

</td><td>

Date when the case occurred. For example, the case may have occurred on 18-02-2024.

</td></tr><tr><td>

Date of discovery

</td><td>

Date when the case was discovered. For example, the case may have occurred on 18-02-2024, but was discovered on 12-03-2024.

</td></tr><tr><td>

Case creation date

</td><td>

Date when the case was created. This field is automatically set to the current date and time.

</td></tr><tr><td>

Case closure SLA

</td><td>

Expected date of the case closure. This date is automatically calculated based on the case creation date.

</td></tr><tr><td>

Investigation planned start

</td><td>

Planned start date to investigate the case.

</td></tr><tr><td>

Investigation planned end

</td><td>

Planned end date to investigate the case.

</td></tr><tr><td>

Investigation actual start

</td><td>

Actual start date of the case investigation.

</td></tr><tr><td>

Investigation actual end

</td><td>

Actual end date of the case investigation.

</td></tr><tr><td>

Remediation planned start

</td><td>

Planned start date to remediate the case.

</td></tr><tr><td>

Remediation planned end

</td><td>

Planned end date of the case remediation.

</td></tr><tr><td>

Remediation actual start

</td><td>

Actual start date of the case remediation.

</td></tr><tr><td>

Remediation actual end

</td><td>

Actual end date of the case remediation.

</td></tr><tr><td class="sub-head" colspan="2">

Breach analysis

</td></tr><tr><td>

Breach status

</td><td>

Status to indicate if a breach has occurred or not:-   **To be determined**: When the breach isn’t determined yet.
-   **Breach detected**: When the breach is confirmed.
-   **Future potential**: When the breach hasn’t occurred but may occur in the future.
-   **Not a breach**: When no breach is detected.

</td></tr><tr><td>

Reporting status

</td><td>

Status of the case being reported to the regulators. This field is automatically set based on the reporting status of the regulations that are associated with the case. If a case has many regulations and even if one regulation is identified as **reportable**, then the reporting status of the case is set to reportable. The default value of this field is **To be determined**.

</td></tr><tr><td>

Breach start

</td><td>

Date that the breach started. This field only appears when **Breach detected** or **Future potential** is selected from **Breach status**.

</td></tr><tr><td>

Breach end

</td><td>

Date that the breach ended. This field only appears when **Breach detected** or **Future potential** is selected from **Breach status**.

</td></tr><tr><td>

Breach significance identified

</td><td>

Date when the user identifies that the breach is significant. This field only appears when **Breach detected** or **Future potential** is selected from **Breach status**.

</td></tr><tr><td class="sub-head" colspan="2">

Root cause analysis

</td></tr><tr><td>

Primary cause

</td><td>

Primary cause of the case reported. This field is automatically set to the primary cause that is selected in the Cause and consequences related list.

</td></tr><tr><td>

Consequences

</td><td>

Consequences from the primary cause of the case reported. For example, damage to physical assets.

</td></tr><tr><td>

Overall observations

</td><td>

Observations made regarding the case.

</td></tr><tr><td>

Remediation taken

</td><td>

Option to indicate if the remediation measures have been taken to address the case:-   **Yes**
-   **No**

</td></tr><tr><td>

Overall preventive measures

</td><td>

Preventive measures taken to re-mediate the case.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Notes or information about the case.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Additional information about the case that you want to share with the customers.

</td></tr><tr><td>

Save

</td><td>

Save the details of the compliance case.

</td></tr></tbody>
</table>**Parent Topic:**[Create a compliance case in the Compliance Workspace](../task/create-compliance-case.md)

