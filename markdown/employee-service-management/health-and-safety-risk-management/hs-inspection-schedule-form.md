---
title: Inspection schedule form
description: Safety inspection manager can use the inspection schedule form to set up a recurring workplace safety inspection.
locale: en-US
release: xanadu
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reference, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Inspection schedule form

Safety inspection manager can use the inspection schedule form to set up a recurring workplace safety inspection.

For information on setting up an inspection schedule, see [Set up a safety inspection schedule](../task/hs-schedule-recurring-safety-inspection.md).

<table id="table_qm2_t21_gbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Brief description about this safety inspection.

</td></tr><tr><td>

Active

</td><td>

Option for marking the inspection schedule available for use. An inspection schedule must be active to be used.

</td></tr><tr><td>

Inspection format

</td><td>

Format in which this inspection is carried out.-   **Digital**: Triggers the survey selected in the **Inspection survey** field.
-   **Paper**: The assigned person completes the survey on paper and uploads a photo or document of the completed inspection as an attachment to the inspection record.

</td></tr><tr><td>

Inspection survey

</td><td>

Inspection survey to be completed for this inspection. Select the survey to use.Only the surveys with the **Source table** field set to Inspection \[sn\_hs\_rm\_inspection\] table are available in this list. Use surveys available with the application or build new ones with the Survey designer. You can also associate any of your pre-built surveys with inspection records in Health and Safety Risk Management. For more information, see [Configure a safety inspection or audit survey](../task/hs-configure-safety-inspection-surveys.md).

This field appears only when **Inspection format** is set as **Digital**.

</td></tr><tr><td>

Assignment group

</td><td>

User group this inspection survey is assigned to. Only members of this group can view and take this survey.

</td></tr><tr><td>

Assigned to

</td><td>

User this inspection survey is assigned to.

</td></tr><tr><td>

Location

</td><td>

Location that this safety inspection applies to.

</td></tr><tr><td>

Assets

</td><td>

Assets that this inspection is related to. For example, the inspection needs to be conducted on these assets.**Note:** The assets field appears only when Expanded Model and Asset Classes \[sn\_ent\] application is installed. For more information, see [Additional features in Health and Safety](../../ohs-incident-management/task/install-hs-incident-mgmt.md#table_ix1_bff_gxb)

</td></tr></tbody>
</table><table id="table_cv5_521_gbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start date

</td><td>

Date when an inspection record is first created for this schedule.

</td></tr><tr><td>

End date

</td><td>

Date when the last inspection record is created for this schedule.

</td></tr><tr><td>

Frequency

</td><td>

Frequency between the start and end date at which the system generates an inspection record such as daily, weekly, or monthly.

</td></tr><tr><td>

Months to generate

</td><td>

Months when the recurring inspection records should be generated. When you enter a date range covering an entire year with a monthly frequency, you can select which particular months to generate inspection records for—The inspection doesn't have to happen every month.

This field appears only when **Frequency** is set as **Monthly**.

</td></tr><tr><td>

Survey expiration period

</td><td>

Number of days for the survey to expire after its start date.

</td></tr></tbody>
</table>**Parent Topic:**[Health and Safety Risk Management reference](../concept/hs-risk-mgmt-reference.md)

