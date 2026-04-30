---
title: Track collaboration activity via MSIM workspace
description: Track chat and file activities related to resolving major security incidents through the MSIM Workspace.The File Explorer displays the file system so you can view and interact with files and folders related to resolving the incident.The Chat Channel Manager displays Microsoft Teams with multiple channels created in the Microsoft Teams application based on a configuration template setup.The Chat Channel Manager displays Slack with multiple channels created in the Slack application based on a configuration template setup.Displays all the activities, logs, status that were performed on Microsoft SharePoint, File explorer, and Microsoft Teams.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Using Major Security Incident Management, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Track collaboration activity via MSIM workspace

Track chat and file activities related to resolving major security incidents through the MSIM Workspace.

Activities are coordinated using Microsoft Teams chat and Microsoft SharePoint files and folders and then posted back to the Major Security Incident via integrations.

Once Microsoft Teams and Microsoft SharePoint are integrated with Major Security Incident Management, you can use the MSIM Workspace to track collaboration between incident response users and other groups who are contributing to the resolution of a major security incident. Any updates to collaboration folders and files in Microsoft SharePoint are synchronized with the MSIM Workspace File Explorer and also reflected in the Activity stream components.

When a security incident is promoted as major security incident:

1.  A folder structure will be created in Microsoft SharePoint based on the folder template configuration. The same folder structure will be reflected on the File Explorer component of the workspace.
2.  A team with multiple channels is created under Microsoft Teams application and the same will be reflected on the Chat Management component of the workspace.

Role required: sn\_msi.workspace\_manager.

**Parent Topic:**[Using Major Security Incident Management](../../security-incident-response/concept/major-security-incident-setup.md)

**Related topics**  


[Propose, promote, and link incident records](../../security-incident-response/concept/promoting-sir-to-msim.md)

[Using MSI List view in the MSIM workspace](../../security-incident-response/task/list-view-in-msim.md)

[View Major Security Incident impact metrics](viewing-trend-charts-and-progress-of-msi.md)

[View Major Security Incident trend charts](viewing-msi-impact-metrics.md)

[Update Major Security Incident details](msim-details-tab.md)

[Link additional records to Major Security Incident](../task/linking-additional-records-to-major-security-incidents.md)

[Unlink records from Major Security Incident](../task/unlinking-msi-records.md)

[Manage tasks in a Major Security Incident](tasks-tab.md)

[Create and distribute MSIM Status Reports](../task/creating-and-distributing-major-security-incident-status-reports.md)

## Interact with files and folders

The File Explorer displays the file system so you can view and interact with files and folders related to resolving the incident.

Displays the file and folders which are captured at Microsoft SharePoint for a specific security incident. These folders will be automatically created on Microsoft SharePoint for that major security incident. You can use this default created folders to upload any supporting files, if required. You can rename, move, or delete these files and folders as required.

Also, whenever you upload a file to any of the folders, the activity corresponding to those folders will be automatically associated to the File Explorer folders in the Collaboration tab and the activity will be recorded and displayed in the Activity section of the Major Security Incident Management Workspace.

**Note:** On the **Collaboration** tab, the incident record is appended to the parent file on the sharepoint with a unique incident number and incident category.

1.  **Repository view**: Lists the files and folders which are listed in the Microsoft SharePoint for that specific security incident. For each file or folder the repository view displays the Name, Modified by, Last modified, and Size will be displayed.

    |Field|Description|
    |-----|-----------|
    |Open in SharePoint|Select this option available next to your major security incident. Click on the link to select and view the folder structure in Microsoft SharePoint.|
    |New Folder|Select this option to create a new folder as required. After you create a new folder, the same new folder is created and associated in your Microsoft SharePoint, by default.|

2.  **Recents**: Displays all the recent activity logs. These logs include both your SharePoint and File Explorer activities. The recent activities are usually your supporting files which are inclusive of the parent folder.

    Following is the procedure to **Locate Log file:**

    1.  Select the respective file to view the details.
    2.  Click **Locate File**.

        **Note:** The navigation and details of the parent file and the parent folders are displayed under the **Recents** list view section. You can open the same file in your SharePoint. Whenever you upload the related log files or any activities, all those files and activities are displayed both in SharePoint and File Explorer.


## Manage Chat Channels communications using Microsoft Teams

The Chat Channel Manager displays Microsoft Teams with multiple channels created in the Microsoft Teams application based on a configuration template setup.

These configured channels are reflected in the Chat Management component along with the users and user groups assigned to them. The Chat Channel Manager enables you to perform the following:

-   **Manage Chat channels**
-   **Rename team**
-   **Manage team members**

The team and channels are created based on the Chat Channel configuration in Microsoft Teams.

### Manage Chat Channels

The Chat Channel Manager enables you to create, edit, or delete Chat Channels. To manage a Chat Channel in Microsoft Teams, perform the following steps:

1.  Select the **Collaboration** tab.
2.  Navigate to **Chat Channel Manager** &gt; **Create New Channel**.
3.  Add a new **Channel Name**, **Description**, and select the **Members** for the channel.
4.  Select **Create**.

    **Note:** A new channel record is created in the Microsoft Teams Channels section of the Microsoft Teams application and the same record will be reflected in MSIM.

5.  To edit a Chat Channel, select a Chat Channel in the Chat Channel Manager list.
6.  You can modify the Channel name, Members list, Group Members list based on your requirements.
7.  Select **Save**.
8.  To delete a Chat Channel, select a Chat Channel in the Chat Channel Manager list.
9.  Select **Delete Channel**.

### Rename Team

To rename a team in Microsoft Teams, perform the following steps:

1.  Select the **Collaboration** tab.
2.  Navigate to **Chat Channel Manager** &gt; **Rename team**.
3.  In the Team name field, rename the team according to your requirements.
4.  Select **Save**.

    **Note:** Renaming the team name will also rename the team name in Microsoft Teams.


### Manage team members

The Chat Channel Manager enables you to add or remove team members in Microsoft Teams. You can also add members through groups. To manage team members in Microsoft Teams, perform the following steps:

1.  Select the **Collaboration** tab.
2.  Navigate to **Chat Channel Manager** &gt; **Manage team members**.
3.  In the Members field, add or remove team members according to your requirements.
4.  In the Add members via Groups field, select the groups that you want to add in Microsoft Teams.

    **Note:** If the group members are already on the team, then those members won’t be added.

5.  Select **Save**.

    The Chat Channel Manager displays the details of the total team members and the number of new members who will be added.


## Manage Chat Channels communications using Slack

The Chat Channel Manager displays Slack with multiple channels created in the Slack application based on a configuration template setup.

These configured channels are reflected in the Chat Management component along with the users and user groups assigned to them. The Chat Channel Manager enables you to **Manage Chat channels**. The team and channels are created based on the Chat Channel configuration in Slack.

### Manage Chat Channels

The Chat Channel Manager enables you to create, edit, or delete Chat Channels in Slack. To manage a Chat Channel, perform the following steps:

1.  Select the **Collaboration** tab.
2.  Navigate to **Chat Channel Manager** &gt; **Create New Channel**.
3.  Add a new **Channel Name**, **Description**, and select the **Members** for the channel.
4.  Select **Create**.

    **Note:** A new channel record is created in the Slack Channels section of the Slack application and the same record will be reflected in MSIM.

5.  To edit a Chat Channel, select a Chat Channel in the Chat Channel Manager list.
6.  You can modify the Channel name, Members list, Group Members list based on your requirements.
7.  Select **Save**.
8.  To delete a Chat Channel, select a Chat Channel in the Chat Channel Manager list.
9.  Select **Delete Channel**.

## Manage activity stream conversations

Displays all the activities, logs, status that were performed on Microsoft SharePoint, File explorer, and Microsoft Teams.

If you want to view any specific activity or search the collaboration activity details which were interacted between various file and folders and also on Microsoft Teams, then you can use the filter capability which is displayed on top right of the Activity Stream section and locate the desired activity details.

Folders and chat conversations shared with Major Security Incident Management reflect as breadcrumbs with the structure:

connector application name &lt;incident number – category &gt; &lt;folder name&gt;\).![Activity details as per the selected filters](../image/activity-stream-breadcrumbs.png)

**Label the activities**:

1.  Click on the **Label** icon.
2.  Select the respective incident activity label check box as shown in the below screen shot.

    ![Assigning labels to incident activities.](../image/collab-labels.png)

3.  The labelled activities are color coded and depicted as progress trend graph on the **External Collaboration** section of the workspace.

