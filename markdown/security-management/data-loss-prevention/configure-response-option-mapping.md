---
title: Configure response option for your DLP incidents
description: Use this feature to configure the type of response that an end user or analyst should perform.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Configure response option for your DLP incidents

Use this feature to configure the type of response that an end user or analyst should perform.

## Before you begin

The base system DLP Incident Response application provides the following response options:

1.  Assessment Complete
2.  Deleted Content
3.  Deleted File
4.  Encrypted File
5.  Masked Content
6.  Report false positive
7.  Report wrong owner
8.  Request email release from quarantine

    **Note:** This option is available for the DLP Microsoft Exchange records.

9.  Required for Business Process
10. Reviewed Entitlements

Role required:

-   sn\_dlir.admin
-   sn\_dlir.analyst and sn\_dlir.analyst\_read

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **Response Options**.

    By default, the base system provides two types of response option:

    1.  **Basic**: A manual response option submitted by the user.
    2.  **Advanced**: An automated response option triggers a flow designer sub flow when the user submits the response option.
2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter the name of the incident response option.|
    |Type|Option to select the response option type.|

<table id="table_jnq_3wd_cyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the name of the incident response option.

</td></tr><tr><td>

Type

</td><td>

Option to select the response option. By default, this field displays the following two types of options:-   **Basic**: When you select this option while creating a new response option, you may have to add a response option name and the type.
-   **Advanced**: When you select this option, the following fields will be available for you to select:
    -   **Flow**: Select the flow designer sub flow.
    -   **Requires MID Server**: Select this check box if the selected flow uses the MID Server.


</td></tr><tr><td>

Flow

</td><td>

Select the required flow designer flow to activate the MID Application and MID Capability.When you are creating a sub flow for the response option, add the following sub flow inputs:

1.  **Name**:
    -   dlp\_incident
    -   mid\_server\_capability
    -   mid\_server\_application
2.  **Type**:
    -   Reference \(to DLP incident table\)
    -   Sys ID for both MID Server application and MID Server Capability


</td></tr><tr><td>

Requires MID Server

</td><td>

Option to determine that MID server configuration. By enabling the **Requires MID Server** checkbox **MID Server Application** and **MID Server Capability** fields you can configure the MID Application and MID Capability.**Note:** Based on the MID Server Application and MID Server Capability configuration and if any MID is up and running then only the Response Option will be visible in the workspace.

</td></tr><tr><td>

MID Server Application

</td><td>

Select the required MID Server Application from the drop down list.

</td></tr><tr><td>

MID Server Capability

</td><td>

Select the required MID Server Capability from the drop down list.

</td></tr></tbody>
</table>    **Note:** If there is no MID server available for the selected MID Server Capability, the response option will not be visible. If you want a specific MID server from the list then you have to configure the MID app and make it visible in the list, and then at least one MID server which is configured should be up and running from the selected mid applications and should have the selected MID Server Capability.

4.  Click **Submit**.

    **Note:** If you are creating an **Advanced** type of response option, then the **Approval Rules** related list will be populated for you to configure the approval rule for that new response option. For more information, see [Create Approval Rules](configure-approval-rules.md).

    ![Configure Response Option](../image/dlp-msft-default-response-option.png "Configure Response Option of Type: Advanced")


**Parent Topic:**[DLP Incident Response Administration](../concept/data-loss-prevention-administration.md)

**Related topics**  


[DLP default configuration settings](configure-data-loss-prevention.md)

[Create end user lookup rules](configure-enduser-lookup-rules.md)

[Create assignment rules](create-assignment-rules.md)

[Create incident consolidation rules](configure-incident-consolidation-rules-to-consolidate-your-dlp-incidents.md)

[Create response due date rules](setup-response-due-date-rules.md)

[Create Approval Rules](configure-approval-rules.md)

[Create user instructions templates](create-and-manage-user-instructions-template-for-dlp-incidents.md)

[Create email templates](create-and-manage-email-templates.md)

[Create a Data Loss Prevention Incident Response SLA trigger](sla-records.md)

[Create a Data Loss Prevention Incident Response SLA definition](dlp-sla-definitions.md)

[Create assessments](create-and-manage-assessments-for-dlp-incidents.md)

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

