---
title: Data Loss Prevention Incident Response Analyst Workspace
description: Use the Data Loss Prevention Incident Response \(DLP IR\) Analyst Workspace to view the DLP incidents. Assign the incidents to end users for resolution and more.Access the Data Loss Prevention Incident Response \(DLP IR\) Analyst Workspace so that you can review the DLP incidents and assign or resolve them. You can track trends on incidents by severity, top offenders, incidents by scan source, and incidents by policy.Preview Data Loss Prevention Incident Response evidence files in the DLP IR Analyst workspace.A Data Loss Prevention Incident Response Playbook is a step-by-step guide for addressing and mitigating data loss incidents, which can include unauthorized exposures, leaks, or breaches of sensitive information that can compromise your organization’s security.Add a Playbook in the Data Loss Prevention Incident Response Analyst workspace that can act as a guide for addressing and mitigating data loss incidents that can compromise your organization’s security.Cancel a Data Loss Prevention Incident Response Playbook to stop a business flow when it is no longer valid.Use the DLP Analyst workspace to view or reactivate the archived DLP incidents.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 15
keywords: [Preview Evidence Files, DLP analyst workspace, Data Loss Prevention Incident Response, add a new DLP Playbook]
breadcrumb: [Manage incidents, Data Loss Prevention Incident Response, Security Operations]
---

# Data Loss Prevention Incident Response Analyst Workspace

Use the Data Loss Prevention Incident Response \(DLP IR\) Analyst Workspace to view the DLP incidents. Assign the incidents to end users for resolution and more.

The DLP workspace consists of a home page with dashboards, list views, and form views that let you monitor DLP incidents.

![DLP Workspace Overview page.](../image/dlp-ops-homepage.png "DLP Workspace overview page")

**Parent Topic:**[Data Loss Prevention Incident Response Incident Management](../task/data-loss-prevention-incident-management.md)

**Related topics**  


[Data Loss Prevention Incident Response User Workspace](using-dlp-end-user-portal.md)

[Data Loss Prevention Incident Response Dashboard](using-dlp-dashboard.md#)

## Review and assign your DLP incidents

Access the Data Loss Prevention Incident Response \(DLP IR\) Analyst Workspace so that you can review the DLP incidents and assign or resolve them. You can track trends on incidents by severity, top offenders, incidents by scan source, and incidents by policy.

DLP Workspace homepage![DLP Workspace homepage]()

DLP Workspace Overview![DLP Workspace Overview]()

### Before you begin

Role required:

-   sn\_dlir.analyst - Edit and view DLP incidents.
-   sn\_dlir.analyst\_read and sn\_dlir.read - View DLP Incidents.

### Procedure

1.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

    The DLP Workspace My Incidents ops list page opens in a new tab.

2.  Click on the **DLP Workspace** home icon to view the workspace homepage view.

3.  Review the dashboard widgets to identify trends by incidents by severity, top offenders, incidents by scan source, and incidents by policy.

4.  Click the appropriate filters on the home page to view the widgets by their various categories.

    |Filters|Description|
    |-------|-----------|
    |Open incidents|View all open incidents.|
    |Overdue critical incidents|View the incidents that have the critical severity label and that are overdue.|
    |Incidents assigned to end users|View the incidents that are assigned to end users.|

5.  You can review and assign the DLP incidents using two ways:

    1.  The first way is to locate and select one or more DLP incidents that you want to review, and click the check box next to the incidents.

    2.  Choose the option that is appropriate for you.

<table id="table_x34_rk5_h5b"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Refresh List

</td><td>

Option to refresh the list of DLP incidents when you make an update.

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

Show filter panel

</td><td>

Option to drill down the required incidents using the filter option.1.  Click the filter on the top-left of the page, and select **Advanced view**.
2.  Use an existing filter or build your own by adding conditions that contain a field, operator, and values.
3.  To add more conditions, click **AND** or **OR**:
    -   If **AND** is selected, all conditions must be matched.
    -   If **OR** is selected, either condition can be matched.
4.  Click **Update**.


</td></tr><tr><td>

Assign Incident

</td><td>

Action to determine whom to assign the DLP incident to. Choices are as follows:-   **Assign incident to**: Option to assign the incident to an analyst, end user, or someone else.
-   **User**: Option to determine which user that the incident should be assigned to.
-   **Incident state pre-user response**: Option to determine which state that the incident should be in before the user responds. It can also be a custom state.
-   **Attach assessment**: Option to indicate whether you want to attach an assessment to the incident. If enabled, below options will be available:
    -   **Assessment template**: Option to select an assessment template for the DLP incident.
    -   **Incident state post user response** Option to select which state that the DLP incident should be in after the user responds.


</td></tr><tr><td>

Respond

</td><td>

Respond to an incident by selecting an incident response option. For example, user delete a file violating a DLP policy, the user can choose the option **Deleted File** to submit manual acknowledgement that the file has been deleted and provide comments. From here you can also select advanced response options. For example, **Request email release from quarantine**.

</td></tr><tr><td>

Escalate

</td><td>

Action to escalate the incident. You can escalate the incident by selecting the user that you want to escalate it to. You can also any additional information in the Comments field.

</td></tr><tr><td>

Update State

</td><td>

Action to update the state of the incident. You can update the state of the incident by select one of the states from the drop-down options. It can also be a custom state.

</td></tr><tr><td>

Close

</td><td>

Action to close the incidents. Select the corresponding **Closure code** from the drop down list and add closure comments.The **Close** feature in Data Loss Prevention Incident Response is done both asynchronously and synchronously from the list view.

1.  Synchronous closure: When closing incidents synchronously, it means that the closure action is performed immediately. When you select multiple incidents for closure and if the incident count is less than or equal to 100 then the incidents are closed foreground from the DLP incidents list view. Here 100 is the default value.
2.  Asynchronous closure: This implies that the closure request is submitted and the application runs the request in the background if the selected incidents count is greater than 100.

You need to refresh the DLP incidents list view to see the updated the incidents status.

**Note:**

    -   The selected incidents count for both asynchronous or synchronous closure is configured using the system property `sn_dlir.closure_sync_count_limit`.
    -   By default the incident count is set to 100.


</td></tr></tbody>
</table>    3.  The second way is to click a particular DLP incident to open it.

        -   **Details** tab: Displays the following sections:
            -   **Details**: You can view the details of the DLP incident such as Incident number, Severity, File name, and so on. You are also provided with the ability to modify the Severity, State, End user, and DLP Analyst group fields respectively and save them.
            -   **Compose**: To add comments about the DLP incident that is visible to everyone, enter the comments in the Comments tab. To add comments that are visible to certain people, enter the comments in the Work notes \(Private\) tab.
            -   **Activity**: You can view the details of the different activities on the DLP incident.
            -   **Attachments**: If you have any attachments related to the DLP incident, click **Browse** and select the attachment from your local drive.
        -   **Additional Details** tab: Displays all the additional information about the DLP incident including custom fields.

            **Important:**

            -   Custom fields for DLP incidents are supported only on the San Diego version or later.
            -   You can use the **Additional Details** tab to see if any custom fields have been created for a particular DLP incident or not.
        -   **Custom attributes** tab: Displays the list of custom attributes related to the DLP incident.
        -   **Other incidents from end user**: Displays the incident from the same end user. One can consolidate incidents by performing the **Add as child incident** action from this related list.
        -   **Detected Sensitive Information type**: Displays the incident detected sensitive information.

            **Note:** This related list is visible only for the DLP Incidents created for Microsoft or Symantec integrations. Within the Microsoft or Symantec incident record, whenever the user accesses the detected sensitive information type record, the highlighted match content with respect to that integration is displayed.

        -   **Child Incidents**: Displays the child incidents created manually \(by performing the ‘Add as child incident’ action\) or from the DLP consolidation rules. One can unlink the child incident by performing the ‘Unlink child incident’ from this related list.
        -   **Cloned incidents**: Displays the cloned incidents from the parent incident. By clicking on the **Clone incident** action of the form view, you can create a new cloned incident.
        -   **Assessments** tab: Displays the list of assessments that are assigned to the DLP incident.
    4.  Choose the option that is appropriate for you.

<table id="table_hlf_g45_h5b"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assign Incident

</td><td>

Action to determine whom to assign the DLP incident to. Choices are as follows:-   **Assign incident to**: Option to assign the incident to an analyst, end user, or someone else.
-   **User**: Option to select which user that the incident should be assigned to.
-   **Incident state pre-user response**: Option to select which state that the incident should be in before the user responds. It can also be a custom state.
-   **Attach assessment**: Option to indicate whether you want to attach an assessment to the incident. If enabled, below options will be available:
    -   **Assessment template**: Option to select an assessment template for the DLP incident.
    -   **Incident state post user response**: Option to select which state that the DLP incident should be in after the user responds.


</td></tr><tr><td>

Cancel Approval

</td><td>

Action to cancel the approval request. This action will be visible to analysts on the form view only when the DLP Incident is in **Pending Approval** state. The available options are:

-   **Assign incident to**: Option to assign the incident to no one, to an analyst, or to someone else.
-   **User**: Option to select which user that the incident should be assigned to.
-   **Post cancellation incident state**: Option to select which state that the incident should be in after canceling the request.
-   **Comments**: To provide additional details for cancellation.


</td></tr><tr><td>

Assign Assessment

</td><td>

Action to attach an assessment while assigning the incident. Choices are follows:-   **Assessment template**: Option to select an assessment template for the DLP incident.
-   **Incident state post user response**: Option to select which state that the DLP incident should be in after the user responds.


</td></tr><tr><td>

Download File

</td><td>

Action to download the file or email that has the violating content. This action can be performed for incidents created for Microsoft OneDrive, SharePoint Online, or Exchange Online.

</td></tr><tr><td>

Save

</td><td>

Action to save any changes that you made. You have an option to modify the Severity, State and End user fields of the DLP incident and save them.

</td></tr><tr><td>

Respond

</td><td>

Respond to an incident by selecting an incident response option. For example, user delete a file violating a DLP policy, the user can choose the option **Deleted File** to submit manual acknowledgement that the file has been deleted and provide comments. From here you can also select the advanced response options. **For example: Request email release from quarantine**.

</td></tr><tr><td>

Escalate

</td><td>

Action to escalate the incident. You can escalate the incident by selecting the user that you want to escalate it to. You can also any additional information in the Comments field.

</td></tr><tr><td>

Clone Incident

</td><td>

Action to create a clone incident if the incident record impacts multiple users. You can assign the cloned incidents to multiple stakeholders such as legal/IT.After you create a clone incident record, a new **Cloned Incidents** tab gets created under the parent DLP incident and all the cloned incidents are listed in this view.

**Note:**

-   If the parent DLP incident record is closed, then all the cloned incident records will close automatically.
-   If a DLP incident record contains a cloned incident, it cannot be assigned to end users. The Parent DLP incident records can be managed only by users with the Analyst role.
-   You also have an option to automatically update the parent state based on the state of the cloned incidents in the Default Configuration module. For example, if all the cloned incidents are moved to the Escalated state, then the parent incident will also be moved to the Escalated state.


</td></tr><tr><td>

Close

</td><td>

Action to close the incident. You must select the corresponding **Closure code** from the drop down list and add any closure comments, if required.

</td></tr><tr><td>

Close as false positive

</td><td>

Action to close the incident as false positive. You can also add any additional comments before closing the incident.

</td></tr></tbody>
</table>6.  You can see the List view from the homepage by going to the top-left of the page and clicking the **Lists** tab.

    The Lists category consists of the default and customized list pages for DLP incidents.

    -   **Lists** tab: Default lists for DLP incidents. The following are the default lists:
        -   All
        -   Open
        -   My Incidents
        -   Assigned to my group
        -   Escalated
        -   Overdue
        -   Pending Assessments
        -   User action pending
        -   Cloned Incidents
        -   Archived Incidents
    -   **My Lists** tab: Displays any lists that you’ve renamed and any lists that you created.

## Preview evidence files

Preview Data Loss Prevention Incident Response evidence files in the DLP IR Analyst workspace.

### Before you begin

**Important:** While using the Evidence files action in the DLP analyst workspace, the evidence files are temporarily stored in the ServiceNow database in an unencrypted format. If you don't want to store the evidence files, disable the Evidence Files preview feature. For more information, see [Configure advanced settings](../task/configure-advanced-settings-dlp.md).

Role required: sn\_dlir.analyst

### Procedure

1.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

2.  Open a DLP incident record.

3.  From the contextual sidebar, select the Evidence files icon \(![Evidence files icon.](../image/icon-evidence-files.png)\).

4.  On the **Evidence Files** tab, select the **Evidence File** card to preview the evidence files in the document viewer.

    The preview feature is different for each file type, as listed in the following table.

<table id="table_bfs_kyj_k2c"><thead><tr><th>

File Format

</th><th>

File Extension

</th></tr></thead><tbody><tr><td>

Image

</td><td>

.bmp, .gif, .ico, .jpeg, .jpg, .png, .svg, and .webp.Image files open in the document viewer mode.

</td></tr><tr><td>

Microsoft Office files

</td><td>

.doc, .docx, .ppt, .pptx, .xls, and .xlsx Office files open in the document viewer mode.

</td></tr><tr><td>

Text files

</td><td>

.txtText files open in text editor mode.

</td></tr><tr><td>

Mail files

</td><td>

.eml**Note:** The file size must be less than 5MB. You must first download the file to preview its content.

</td></tr><tr><td>

PDF files

</td><td>

.pdf -   Enter a keyword to search the document.
-   Zoom-in and zoom-out features to adjust the view for better readability.
-   Rotate the page clockwise or counterclockwise to view the content more clearly.


</td></tr></tbody>
</table>    **Note:**

    Binary files won’t be rendered and have to be downloaded to preview their content. The preview evidence file feature also works for archived incidents.


## Playbook for Data Loss Prevention Incident Response

A Data Loss Prevention Incident Response Playbook is a step-by-step guide for addressing and mitigating data loss incidents, which can include unauthorized exposures, leaks, or breaches of sensitive information that can compromise your organization’s security.

The following table lists the activities and stages available for creating a DLP Playbook. For more information, see [Add a DLP Playbook](using-dlp-ops-portal.md#):

|Activity|Description|
|--------|-----------|
|Detection|Identify and confirm unauthorized access or exposure of sensitive data.|
|Containment|Isolate affected systems or users to prevent further data leakage or unauthorized access.|
|Investigation|Investigate the breach to understand how it occurred, what data was affected, and the potential impact.|
|Notification|Notify internal teams, external stakeholders, and regulatory bodies as required by law or policy.|
|Remediation|Apply corrective measures to address vulnerabilities, update policies, and prevent future breaches.|
|Recovery|Restore systems from secure backups and validate the integrity of data post-incident.|
|Post-Incident Review|Analyze the incident to identify root causes, improve security controls, and strengthen policies.|

The following figure shows the workflow of activities and stages involved in the creation of the Sensitive Data Breach Playbook. Playbook steps vary depending on the workflow.

![Playbook design workflow](../image/sensitive-data.png "Playbook design workflow")

**Related topics**  


[Add a DLP Playbook](using-dlp-ops-portal.md#)

[Cancel a DLP Playbook](using-dlp-ops-portal.md#)

### Add a DLP Playbook

Add a Playbook in the Data Loss Prevention Incident Response Analyst workspace that can act as a guide for addressing and mitigating data loss incidents that can compromise your organization’s security.

#### Before you begin

Role required: sn\_dlir.analyst

#### Procedure

1.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

2.  On the DLP Analyst Workspace - My Incidents page, open any DLP incident.

3.  Add the Playbook.

    1.  Navigate to the **Playbooks** tab.

    2.  In the UI actions menu, select the **More actions** icon and select **Add Playbooks**.

    3.  In the dialog box, select a Playbook from the drop-down menu.

    4.  Select **Add Playbooks**.

4.  Select each lane to explore the tasks this Playbook performs.


### Cancel a DLP Playbook

Cancel a Data Loss Prevention Incident Response Playbook to stop a business flow when it is no longer valid.

#### Before you begin

**Note:** Playbooks are automatically canceled when the associated DLP incident is closed.

Role required: sn\_dlir.admin.

#### Procedure

1.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

2.  Open any DLP incident.

3.  Navigate to the **Playbooks** tab.

4.  In the header of the Playbook that you want to cancel, select the Playbook actions icon and then select **Cancel Playbook**.

5.  Provide a reason for canceling the Playbook.

6.  Select **Cancel Playbook**.


#### Result

A banner appears below the Playbook header confirming that the Playbook has been canceled.

## View archived DLP incidents

Use the DLP Analyst workspace to view or reactivate the archived DLP incidents.

### Before you begin

Role required:

-   sn\_dlir.analyst
-   sn\_dlir.analyst\_read and sn\_dlir.read

### Procedure

1.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

    By default, My Incidents section is displayed.

2.  Click **Archived Incidents**.

    The archived DLP incidents list is displayed.

3.  Click **Show Incidents Count** button to view the archived incidents count.

    **Note:**

    -   By default, the archived incidents count is hidden to improve the list loading time. Select the **Show Incident Count** button to view the incidents count. An information message is displayed that shows the incidents count.
    -   The system property glide.ui.list.seismic.omit.count is enabled in the base system for the archived incidents to hide the incidents list count.
4.  Select one or more DLP incidents that you want to view.

    The DLP incident displays the incident details section.

    **Note:**

    -   **Other incidents from end users** includes the archived incidents.
    -   **Match Content** is supported for all the archived incidents \(which will be supported in all the integrations as well\) but **Download file** is supported only for Microsoft integrations.
5.  To reactivate an incident, change the **State** field to an active state, such as Open or In Progress.


