---
title: Create user instructions templates
description: Create and manage user instructions template for DLP incidents to help the users understand the instructions involved incident resolution and the next steps involved in the resolution process.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create user instructions templates

Create and manage user instructions template for DLP incidents to help the users understand the instructions involved incident resolution and the next steps involved in the resolution process.

## Before you begin

The user instructions card template displays two different headers which provides you more information about a specific incident on the form view.

Role required:

-   sn\_dlir.admin - Create, edit, and delete.
-   sn\_dlir.analyst and sn\_dlir.analyst\_read - View \(read-only\).

## About this task

When an incident is assigned to the end user then the user might be required to know the additional instructions on how to respond to the incidents, introduce the users to the terminology and provide any additional information about the incident. These templates can guide the users to provide the accurate response to the DLP incidents.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **User Instructions Templates**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_usk_rtj_g5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the user instruction template.

</td></tr><tr><td>

Short Description

</td><td>

Unique description of this user instruction template.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the user instruction template is active.

</td></tr><tr><td>

Execution Order

</td><td>

Priority of the incident user instruction template. This field indicates the order in which the order is executed to evaluate the user instruction template when an incident is created.The option with the lowest number has the highest priority.

To set the order of operation, enter a value. For example, 100, 200, or any other number.

The default is 100.

</td></tr><tr><td>

Incidents matching condition

</td><td>

Incidents that match the defined conditions in the condition builder will be displayed.These conditions are based on the DLP incident data. To build a condition for a user instruction, select any of the incident fields.

Use the lists and fields of the conditions builder to set the filters for the first row. To add more conditions, click AND or OR:

If AND is selected, all conditions must be matched. If OR is selected, either condition can be matched. To set a second filter condition, click **New Criteria**.**Note:** The conditions in the condition builder are case sensitive.

</td></tr><tr><td>

Applies to

</td><td>

Select the user or user groups that the template is applicable for. The other available options are:-   **All end users**: Select this check box if the instructions template applies to all the users.
-   **All reviewers of escalated incidents**: Select this check box if the template applies to all the reviewers of the escalated incidents.
-   **Specific users**: Click the icon to add a particular user from the list to whom the DLP incident conditions are applicable. You can also add a user by using their email address or search option. For example, Legal Manager.

To add yourself as the user to whom the DLP conditions are applicable, click the **Add me** icon.

-   **Specific user groups**: Click the icon to add a particular group from the list to whom the DLP incident conditions are applicable. You can also add a group by using the search option. For example, Survey creators.


</td></tr><tr><td>

Instructions Template: Instructions

</td><td>

Add instructions in the rich text editor with variables available at an incident level.

</td></tr></tbody>
</table>4.  Drill down to the **Instructions Template** section, enter the template instruction and add incident level information under this section, if required.

5.  Drag-and-drop the required variables to dynamically display certain fields.

6.  Click **Submit**.

    The user instructions templates are now created and you can click on any user instruction header to know the additional details of a DLP incident.

    For more information, see [Data Loss Prevention Incident Response User Workspace](../concept/using-dlp-end-user-portal.md).


-   **[Configure DLP UI user instructions](configure-dlp-ui-user-instructions.md)**  
Configure the system UI messages to add detailed user instruction headers as required.

**Parent Topic:**[DLP Incident Response Administration](../concept/data-loss-prevention-administration.md)

**Related topics**  


[DLP default configuration settings](configure-data-loss-prevention.md)

[Create end user lookup rules](configure-enduser-lookup-rules.md)

[Create assignment rules](create-assignment-rules.md)

[Create incident consolidation rules](configure-incident-consolidation-rules-to-consolidate-your-dlp-incidents.md)

[Create response due date rules](setup-response-due-date-rules.md)

[Create Approval Rules](configure-approval-rules.md)

[Create email templates](create-and-manage-email-templates.md)

[Create a Data Loss Prevention Incident Response SLA trigger](sla-records.md)

[Create a Data Loss Prevention Incident Response SLA definition](dlp-sla-definitions.md)

[Create assessments](create-and-manage-assessments-for-dlp-incidents.md)

[Configure response option for your DLP incidents](configure-response-option-mapping.md)

[Create incident response option rules](configure-end-user-action.md)

[Create age chart configurations](configure-age-chart.md)

[Create user delegate configurations](configure-delegation.md)

[Create repeat offender identification rules](repeat-offender-identification-rules.md)

[Create Additional Incident Data Fields](create-custom-fields-dlp.md)

[DLP SLA Definition form](../reference/dlp-sla-def-properties.md)

[Configure advanced settings](configure-advanced-settings-dlp.md)

[Monitor DLP Integration Run process](../../dlp-microsoft/concept/configure-microsoft-dlp-integration-run-process.md)

[DLP Incident Access Restrictions](../concept/dlp-incident-access-restrictions.md)

[DLP Incidents Archival](dlp-archiving-rule.md)

