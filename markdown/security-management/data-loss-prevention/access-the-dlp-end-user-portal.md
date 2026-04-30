---
title: Report or respond to DLP incidents
description: Access the Data Loss Prevention Incident Response \(DLP\) User workspace, review the assigned DLP incidents, and report or respond to the incidents.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Data Loss Prevention Incident Response User Workspace, Manage incidents, Data Loss Prevention Incident Response, Security Operations]
---

# Report or respond to DLP incidents

Access the Data Loss Prevention Incident Response \(DLP\) User workspace, review the assigned DLP incidents, and report or respond to the incidents.

## Before you begin

Role required:

-   Any valid user/employee

## Procedure

1.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP User Workspace**.

    The My DLP Incidents page opens in a new tab.

2.  Click a list view to review the incidents that are assigned to you.

    |List view|Description|
    |---------|-----------|
    |All|View all the assigned incidents.|
    |Due in the next 7 days|View all the incidents that are due in the next 7 days.|
    |Critical incidents|View all the incidents with the severity label critical.|
    |New incidents this week|View all the incidents that are assigned this week.|
    |Pending Assessments|View all the assessments that are still pending.|

3.  You can review the DLP incidents using two ways:

    1.  The first way is to locate and select one or more DLP incidents that you want to review, and click the check box next to the incidents.

    2.  Choose the option that is appropriate for you.

<table id="table_b3s_pvs_h5b"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Refresh List

</td><td>

Option to refresh the list of DLP incidents if you made an update.

</td></tr><tr><td>

List Actions

</td><td>

List of actions that you can perform. Choices are as follows:-   **Save as**
-   **Edit columns**
-   **Reset widths**
**Note:** When you have your own custom list which is created under **My Lists** section configured for your workspace, you will be able to perform the below additional list actions as well:

-   **Rename**
-   **Save**
-   **Delete**


</td></tr><tr><td>

Copy URL for All

</td><td>

Option to copy the URLs of all the DLP incidents.

</td></tr><tr><td>

Report Incident

</td><td>

Action to report the incident as false positive or wrong owner. For example, you can report a wrong owner and suggest another owner or report the incident as a false positive.

</td></tr><tr><td>

Respond

</td><td>

Respond to an incident by selecting an incident response option. For example, user delete a file violating a DLP policy, the user can choose the option **Deleted File** to submit manual acknowledgement that the file has been deleted and provide comments. From here you can also select advanced response options. For example, **Request email release from quarantine**.

</td></tr></tbody>
</table>        ![DLP User workspace landing page navigation](../image/dlp-user-workspace-landing.png "DLP User Portal homepage")

    3.  The second way is to click a particular DLP incident to open it.

        The **Details** tab displays the following sections:

        -   Details: You can view the details of the DLP incident such as incident number, severity, file name.
        -   Compose: To add comments about the DLP incident that is visible to everyone, enter the comments in the Comments tab. To add comments that are visible to certain people, enter the comments in the Work notes \(Private\) tab.
        -   Activity: You can view the details of the different activities on the DLP incident.
        -   Attachments: If you have any attachments related to the DLP incident, click **Browse** and select the attachment from your local drive.

            The **Additional Details** tab displays all the additional information about the DLP incident including custom fields.

            **Important:**

            -   Custom fields for DLP incidents are supported only on the San Diego version or later.
            -   If there are any custom fields data available for a particular DLP incident, you can view them under the **Additional Details** tab. If there are no custom fields for the DLP incident, you would see a blank page.
        -   **Detected Sensitive Information Type**: Displays the incident detected sensitive information.

            **Note:** This related list is visible only for the DLP Incidents created for Microsoft or Symantec integrations. Within the Microsoft or Symantec incident record, whenever the user accesses the detected sensitive information type record, the highlighted match content with respect to that integration is displayed.

    4.  Choose the option that is appropriate for you.

<table id="table_fx1_ztt_h5b"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Report False Positive

</td><td>

Action to report that the DLP incident has been wrongly triggered or created. You can mention the details of why you’ve marked the incident as false positive in the Comments field.

</td></tr><tr><td>

Report Wrong Owner

</td><td>

Action to report that the DLP incident has been assigned to the incorrect user. If you know the correct owner for the incident, you can select the owner's name in the Suggest Owner field. To add any additional details, use the Comments field.

</td></tr><tr><td>

Respond

</td><td>

Respond to an incident by selecting an incident response option. For example, user delete a file violating a DLP policy, the user can choose the option **Deleted File** to submit manual acknowledgement that the file has been deleted and provide comments. From here you can also select advanced response options. For example, **Request email release from quarantine**.

</td></tr></tbody>
</table>    5.  Select the **Respond** button after answering the analyst query.

        A pop-up to submit an incident response appears. Select the response from the drop-down menu and add comments.

    6.  Select **Submit**.

        A banner appears confirming that your response has been submitted successfully.

        **Note:** The incident is assigned to the corresponding approver or analyst and the end user will loose the access to the incident.

        ![DLP Performing DLP incident actions.](../image/dlp-enduser-incident.gif "DLP Incident Actions")

4.  To take assessments, select the **Pending Assessments** list view.

    1.  Click a particular assessment number to open it.

    2.  Answer the assessment questions, and click **Save** or **Submit** based on your requirements.

        ![DLP End user assessments.](../image/dlp-enduser-assessments.gif "DLP Assessments")

5.  Click on the **Instructions** card section which is displayed on top of all the fields in the DLP incident form view, to view the additional information about a particular incident.

    **Note:** This section on the workspace guides the users on the incident information, which helps in understanding the next steps of the incident resolution.

    The user instructions card displays two different headers which provides you more information about a specific incident on the form view. Click on any user instruction header to know the additional details.

    For more information, see [Create user instructions templates](create-and-manage-user-instructions-template-for-dlp-incidents.md) and [Configure DLP UI user instructions](configure-dlp-ui-user-instructions.md).


**Parent Topic:**[Data Loss Prevention Incident Response User Workspace](../concept/using-dlp-end-user-portal.md)

