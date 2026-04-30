---
title: SIR Workspace Related Records
description: This section consists of the related lists items that are grouped into sections such as associated observables and configuration items.You can add new related lists or new related list groups, and modify existing groups or related lists that appear in the SIR Workspace.Use this section to configure response tasks new related lists that appears on the Security Incident Response application.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# SIR Workspace Related Records

This section consists of the related lists items that are grouped into sections such as associated observables and configuration items.

The following related lists groups that are available as a part of the base system. You can modify these groups or create groups within the application and their respective actions.

You can modify these groups or create new groups. For more information, see [Configure Security Incident Related List](sir-records.md#) on how to configure and group the related list for security incidents and response tasks. Each related list is fully functional within the SIR Workspace.

<table id="table_dyj_zqv_x5b"><thead><tr><th>

Related list

</th><th>

Grouped item

</th></tr></thead><tbody><tr><td>

Business Impact

</td><td>

-   Configuration Items
-   Affected Users
-   Related Configuration Items
-   Related Users
-   Affected Services

</td></tr><tr><td>

Threat Intel

</td><td>

-   Associated Observables
-   Threat Lookup Results

</td></tr><tr><td>

Phishing

</td><td>

-   Associated Phish Emails
-   Associated Phish Headers

</td></tr><tr><td>

Related Security Incidents

</td><td>

-   Parent Security Incident
-   Child Security Incident
-   Similar Security Incident

</td></tr><tr><td>

SLA Records

</td><td>

Task SLAs

</td></tr><tr><td>

Source Events/Alerts

</td><td>

Source events or alerts are the SIEM integration enabled related list such as Source Email, LogRhythm Drill Down Logs, LogRhythm Events, Aggregated IBM QRadar Offense and so on.**Note:** This list is completely dependent on the integration that you have in your instance. To view the relevant SIEM integration related list, you must install the latest version.

</td></tr><tr><td>

Sighting Search

</td><td>

-   Sightings Search Results
-   Sightings Search Details
-   Sighting

</td></tr><tr><td>

Observable Enrichment

</td><td>

-   Observable Enrichment Results
-   Associated MISP Events
-   MISP Enrichment Results

</td></tr><tr><td>

Endpoint Detection and Response \(EDR\)

</td><td>

-   Host Details
-   Running Processes
-   Running Services
-   Logged On Users
-   Network Statistics
-   Get File
-   Isolate Host Entries
-   Additional Actions On Endpoint
-   Microsoft Defender for Endpoint-Related Machines Details

</td></tr></tbody>
</table>![Related Records](../image/sir-records.png)

**Note:** In general, you'd be able to create new records, link, or unlink existing records or new records against the related list group as applicable.

**Parent Topic:**[Configuring SIR Workspace](../reference/configuring-security-incident-response-workspace.md)

**Related topics**  


[Set up view of SIR Records](set-up-view-of-sir-records.md)

[Configure SI design time investigation](configure-investigation-canvas-records.md)

[Define the new Risk Score Calculator Rules](../task/define-risk-score-calculator-rules-sir.md)

[Configure Shift Handover](config-shift-handover.md)

[Security Incident Response conference call integration](sir-conf-call-capability.md)

[Configure report templates in Security Incident Response](daily-status-sir.md)

[On-Call scheduling in Security Incident Response](on-call-schedule-sir.md)

[Category management in Security Incident Response](category-management-sir.md)

[View and update Security Incident Response system properties](view-update-sirw-system-properties.md)

[Create quick filters for Security Incidents and Response Tasks lists](../task/create-quick-filters-for-security-incidents.md)

[Configure Security Incident Related List](sir-records.md#)

## Configure Security Incident Related List

You can add new related lists or new related list groups, and modify existing groups or related lists that appear in the SIR Workspace.

### Before you begin

The security incident related list are grouped and displayed as group related list items on the **Related Records** tab on the workspace.

Role required: sn\_si.admin

### Procedure

1.  In the classic UI, navigate to **All** &gt; **Security Incident** &gt; **Show Open Incidents**.

    ![Open incidents](../image/show-incidents.png)

2.  Select any incident record.

3.  Right click on the incident context menu.

4.  Go to **Configure** &gt; **Related List**.

    ![related list page](../image/configure-related-list.png)

    The **Configuring related lists on Security Incident form** is displayed.

5.  Go to **View name** and select **New**.

6.  Enter a name for the view.

7.  Select the newly created view.

    After you select the view, choose the required related list fields from the slush bucket.

    ![related list slush bucket view](../image/related-list-slushbucket.png)

    **Note:** If you want to modify anything, select the view and remove or add the items.

8.  Click **Save**.

9.  On the left navigation, navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences**.

10. Select **Security Incident Response Workspace**.

    ![configure related list new experience](../image/related-list-newexp.png)

    The **UX Application Security Incident Response Workspace** page is displayed.

11. Go to **UX Page Properties** tab and select **relatedListLayoutConfig** option in the list view.

    ![Related list](../image/related-list-config.png)

    ![Related List configuration section.](../image/related-list-ux-view.png)

12. Add the newly created view name separated by a comma to an already existing list of values in the **Value** text box under the **sn\_si\_incident.viewsUsedForGrouping** field.

    For example, if you had created a new view name as, **Business Impact** then in the **Value** text box you must specify it as **business\_impact** \(which is separated by underscore within the view name and separated by a comma after an existing value\) under the sn\_si\_incident:groups field.

    ![Related List Layout configuration.](../image/value-text-box-related-list.png)

    **Note:** If you add the new view name under **sn\_si\_incident.viewsUsedForGrouping** field then the entry will be created in the **Related Records** tab of the workspace.

    If you update the view name entry in **si\_other\_records.viewsUsedForGrouping** then the related list group will get added in the **Other Records** tab of the workspace.

    Below is an example view which shows the newly created views added.

    ![related list newly created view](../image/related-list-new-view-page.png)

    **Note:** **requiredRolesForGrouping** contains comma separated sys\_user\_role record names. SIR Workspace user should have at least one of these roles, to use the grouped related lists. When a user does not have any of these roles then related lists view configured for the current user role using view rule configuration will be represented vertically without grouping. This property is ignored when **isGrouped** property is set to false. If this property is empty any user can access the grouped related lists.

13. Click **Save**.

14. Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

15. Select any specific security incident.

16. Go to **Related Records** tab of the workspace.

    The grouped related lists are displayed.


## Configure Response Task Related List

Use this section to configure response tasks new related lists that appears on the Security Incident Response application.

### Before you begin

Role required: sn\_si.admin

### About this task

The response tasks related list is not grouped but displayed as individual related list items, as there are few default lists. View the response tasks related items from the **Response Tasks** tab of the security incident record of the workspace.

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Response Tasks** &gt; **Show All Tasks**.

    ![List of all Security Incident Response Tasks](../image/response-tasks-configure.png)

2.  Select any response task record.

3.  Right click on the Security Incident Response Task context menu.

4.  Navigate to **Configure** &gt; **Related List**.

    The **Configuring related lists on Security Response Task form** is displayed.

5.  Go to **View name** and select **sirw** view.

    ![sirw view name highlighted](../image/response-task-sirw-view.png)

6.  Select the desired related list fields from the slush bucket.

    For example, Affected Locations.

    ![related list slush bucket view](../image/response-tasks-selction.png)

7.  Click **Save**.

8.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace** &gt; **Response Tasks** &gt; **SIT Records**.

    The configured related lists \(For example, Affected locations as selected\) is listed within the SIT records list.

    ![configured related list](../image/aafected-locations-response-tasks.png)


