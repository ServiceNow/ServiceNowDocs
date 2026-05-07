---
title: Sharing of Outbound Intelligence Records from GUI
description: This section outlines the functionality that enables users to share intelligence records directly from the Threat Intelligence \(TI\) Library within the TISC application.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Administer, Threat Intelligence Security Center, Security Operations]
---

# Sharing of Outbound Intelligence Records from GUI

This section outlines the functionality that enables users to share intelligence records directly from the Threat Intelligence \(TI\) Library within the TISC application.

## Before you begin

Role required:

-   sn\_sec\_tisc.analyst
-   sn\_sec\_tisc.admin

## About this task

Access to the sharing templates is governed by multiple restrictions defined within each template. These restrictions specify whether a template is available to all the users or limited to specific users or user groups. Accordingly, only the templates allowed by these settings will be visible when users initiate the **Share Intelligence** process.

Only users with an analyst role can share the intelligence data from GUI to the external systems. Share intelligence feature also applies to the various other threat intelligence library entities including observables, indicators, and objects such as attack patterns, threat actors and so on.

Following is the procedure to share intelligence from the form view of observables records.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **Observables** &gt; **All Observables**.

2.  Open any observable\(s\) record.

3.  Click the **Share Intelligence** button.

    The Select outbound intelligence template dialog box is displayed.

4.  Select the required outbound intelligence template from the look up.

    **Note:** View default template inclusions\(tables and attributes\) hyperlink allows you to view all the included attributes.

5.  Select the check box **Automatically link related records of the selected intelligence as well** to automatically link the related records to the sharing record and save the details.

6.  Select **Submit**.

    After you submit the records for intelligence sharing, only the accessible templates will be displayed.

    1.  **Data exclusion rules configurations**: Records will be excluded if they match the criteria defined in your data exclusion rules. For more information, see [Configuring Outbound Intel Data Exclusion Rule](../task/tisc-outbound-data-exclusion.md).
    2.  **Selected sharing template controls**: Records are filtered according to the controls defined in the selected sharing templates. For more information see, [Configuring Outbound Intel Sharing Templates](../task/tisc-intel-sharing-templates.md).
    Based on these configuration criteria, the relevant records will be excluded from sharing.

7.  Click **Select** to create outbound intelligence sharing record.

    Make the necessary changes, if required.

8.  Click **Save** to save the modified values on the **Outbound Intelligence Data** form.

9.  Select **Submit** to submit the sharing record for submission.

    In the **Details** section of the sharing record, the application automatically populates the values that are configured in the **Prefilled Inputs** of the Outbound Intel Sharing Templates page. For more information, see [Configuring Outbound Intel Sharing Templates](../task/tisc-intel-sharing-templates.md).

    **Note:** The following are the system properties for the outbound intelligence record.

<table id="table_fxh_hcc_qfc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

shared\_intelligence\_entity\_threshold

</td><td>

Record threshold limit: This property controls the maximum number of individual records that can be included in a single outbound intelligence record.-   Default limit is 1000 records.
-   Maximum limit is 10000 records.


</td></tr><tr><td>

shared\_intelligence\_exclusion\_work\_notes\_count

</td><td>

Excluded records limit: This property controls how many rows are displayed per work note in the Activity Stream.-   Default: 10 rows per work note.
-   Maximum: 100 rows per work note.
If the number of rows exceeds the specified limit, the records will be split across multiple work notes to ensure readability and user experience.

</td></tr></tbody>
</table>10. Go to **Intelligence Records** section.

    This section displays all the intelligence records that are part of the selected sharing record.

11. **Viewing Intelligence Records section:**

    **Note:** Intelligence Sharing Records section is only visible when the sharing record is in the **Draft** state and not visible if the sharing record is in other states such as **Processed**, **Awaiting Approval** and so on.

    You can view the complete list of observables, objects, and related entities that are grouped and shared together as part of the record.

    When you access **Intelligence Sharing Records** section, you will see a structured view of all intelligence entities associated with that record, presented in the left side panel of the page.

    -   **Template Configuration**: The entity tables displayed in this view are based on the sharing controls defined in the sharing template associated with the sharing record.
    -   **Entity Grouping**: The first high level grouping is Observables. Also, you will see child level observables such as File, IP Address, and other relevant types. Indicators and objects are also listed after Observables.
    -   **Relationships**: Displays relationships between the shared entities. Six different types of relationships are represented, each organized into its corresponding relationship table for clarity and structure.
    **Note:** **Show lists at least with one record** is a toggle available to quickly filter and display only the entity tables that contain data.

12. Click **Edit Columns** to modify the list view columns.

    The **Select Columns** dialog box is displayed, allowing you to configure which columns are shown in the list view.

13. Additionally, if you want to modify the details of the records then select **Modify Records**.

    When you select this action, you can modify one or more records. Suppose if you are modifying one or more records or doing a bulk edit then you are allowed to only modify the optional fields of the record. When a bulk edit option is selected, all the values in the fields are cleared and when you provide any value and **Save** then those values are applicable to all the selected records.

    **Note:** Any modifications made to the entity records present in the intelligence records section are not applied to the corresponding library records. For example, if you are modifying the description for an attack pattern, then this change would have any impact to the corresponding attack pattern in the threat intelligence library.

14. Click **Add** to add records to the sharing record and a confirmation is displayed that the selected records are added successfully.

    **Note:** If exclusion rules are configured for sharing records, any selected records that meet exclusion rules criteria will be automatically skipped. These records will not be added to the intelligence records. An appropriate error message is displayed to notify the user and a detailed information about the excluded records will be recorded in the Activity Stream.

15. Click **Remove** to remove the records from the sharing record.

16. Select **Enable Redaction** button to activate redaction for the sharing records.

    ![Enable redaction](../image/tisc-enable-redaction.png)

    **Note:** To enable the Redaction Library, ensure to configure the redaction library. For more information see, [Working on the Redaction Library](../task/tisc-redaction-library.md).

    **Enable Redaction** option allows you to automatically remove or mask sensitive information by redacting sensitive content before sharing intelligence records. Enabling redaction ensures that confidential data is protected and not exposed during intelligence sharing.

    Once you enable this option, the **Redaction Library** icon appears on the right side contextual menu, providing access to a list of all available redaction categories and redaction category values that are defined in redaction library in the **Administration** section.

    **Example:** If you are redacting an organization name, such as **Service\_Now**, and **Service\_Now** is added as a redaction category value under the **Organization\_Name** category, then all occurrences of **Service\_Now** will be replaced using the following format:

    `#{Organization_Name}#`.

    By enabling the Redaction option, the system will automatically redact the organization name before sharing. The following screen shot depicts the redacted category value.

    ![Redaction category value](../image/tisc-redaction-category.png)

17. Go to **Review** section to review the intelligence record of the selected sharing record.

18. Select **Disable Redaction** to disable the redaction for the sharing records, if needed.

19. **Review Intelligence Records**
20. Navigate to **Review** section to review the records in the sharing record.

    The **Review** sections provides a snapshot view that summarizes all the entities that are included in the intelligence share. The records shows the quick summary of the following:

    -   **Details**: Displays the details of the sharing record in the read-only mode.
    -   **Sharing Entity Attributes**: Displays the sharing controls defined in the sharing template associated with a sharing record.
    -   **Exclusion Rules**: Displays the exclusion rules configured.
    -   **Redaction Library**: Displays the redaction library configured in the **Administration** section. For more information, see [Working on the Redaction Library](../task/tisc-redaction-library.md).
21. Make the necessary changes under the **Review** section and click **Submit** for submission.

    A confirmation message is displayed prompting if you want to submit the record for processing, if you wish to proceed then select **Submit**.

    Once you submit, the outbound intelligence sharing record’s **State** changes from **Draft** to **Awaiting Approval**. The **State** is changed to **Awaiting Approval** only when the approval rules are configured for the outbound intelligence. For more information, see [Defining Approval Rule for Outbound Intel](../task/tisc-approval-outbound-intel.md).

22. Select **Approve** button to approve the outbound intelligence record.

23. Add any comments, if required and select **Approve** on the **Approve Outbound Intelligence** dialog box.

24. Also, select **Reject** button to reject the outbound intelligence record.

25. Provide a reason and select **Reject** on the **Reject Outbound Intelligence** dialog box.

    Once you reject, the outbound intelligence sharing record’s **State** changes to **Rejected**.

    **Note:** Select **Edit** button and make the necessary changes based on the rejection comments. The **State** will move back to **Draft** when you choose to edit the records and resubmit.

    If no approval rule is defined or if the record is already approved, the outbound intelligence sharing record is moved to the **Awaiting Processing** state. At this stage, the intelligence data will be shared externally, after which the state is updated to **Processed**. For more information, see [Defining Approval Rule for Outbound Intel](../task/tisc-approval-outbound-intel.md).

26. Navigate to **Published Jobs** to view the published jobs for the sharing record.

    For each outbound intelligence profile, there will be a published job and the **Status** can be tracked through these published jobs.

    For further details, when you click on any of the published job then the details of the job will be displayed such as **Payload**, **Status**, and so on.

    If an issue occurs on the receiver side while sending data to the corresponding endpoint, the application will automatically retry up to 5 times by default. To change the number of retry attempts, you can modify the value using the following system property:

    `sn_sec_tisc.shared_intelligence_retry_count`


**Related topics**  


[Configuring Outbound Intel Sharing Controls](../task/tisc-outbound-sharing.md)

[Automated Sharing of Outbound Intelligence Records](tisc-automated-outbound-intel-share.md)

