---
title: Legacy - Migrate completed update set history to Source Control
description: When linking to Source Control, this feature allows application developers the choice of migrating the information in completed update sets to Source Control history.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Migrate completed update set history to Source Control

When linking to Source Control, this feature allows application developers the choice of migrating the information in completed update sets to Source Control history.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

## Before migrating

Make sure that you have fulfilled these criteria before attempting to migrate your update sets:

-   Role required: admin
-   Read the [Legacy - Link an application or application-customization to source control](../task/t_LinkAnApplicationToSourceControl.md) topic
-   Complete any update sets for your application that you want to export as Source Control history.
-   Export the completed update set if you want to preserve it.

When you link an application to Source Control, the update sets and customer update records are deleted. After you link to Source Control, if the application has any completed update sets, you will be asked to make a choice in the dialog box below.

-   If you select “Yes, do retain update set history as commits”, the update set history is preserved as Source Control commits.
-   If you select “No, do not retain update set history as commits,” they are not preserved as commits.

Regardless of which option you select, if you select **Continue**, the **Link to Source Control** operation starts, and all completed update sets and all Customer Update records are deleted. If you need to complete any additional update sets or choose not to continue, select **Cancel**. ![Dialog box requesting your choices for selecting your update set history](../image/link-to-source-control-update-set.png)

For every completed update set with updates to the application that you are linking to Source Control, commits are generated automatically by the system based on the sys\_update\_xml records in the update sets. The commits are ordered by the **sys\_recorded\_at** timestamp. For Global applications: Any **sys\_update\_xml** records that belong to the application and are part of a completed Global update set are captured as historical commits.

When the Link to Source Control operation is complete, the most recent commit is the current state of your application in its entirety. You can view historical commits in your Git repository or by clicking the Source Control menu option and selecting **View History**. Updates are separated into multiple commits:

-   If there are updates for a file that are out of order between different update sets.
-   If an update set contains multiple update records for a single file.

The commits for an update set are split into multiple commits \(\[Historical Commit 1\], \[Historical Commit 2\]...\) to represent each update. This is done so that each file has an ordered history of updates.

**Warning:** Any commit prefixed by \[Historical Commit\] is generated solely to display its history. Do not attempt to check out these commits in the development process as they do not necessarily represent a stable snapshot of the application.

The **author\_elective\_update** folder is not created until the initial commit. That means that in the initial commit you might see files such as **sys\_choice** files being renamed and moved from the update folder to the **author\_elective\_update** folder. Any files that are deleted from update sets in historical commits are deleted, and not moved to the **author\_elective\_update** folder as they would be for actual commits. During the initial commit, DELETE payloads are also created for any DELETE sys\_update\_xml records that were deleted as part of completed update sets.

Example commit message:

```
[Historical Commit 1] <Name of update set that this commit belongs to>
Description: <Description of update set that this commit belongs to>
Update Set was completed on / installed on <date>
Update Set was completed by <sys_user user_name > <sys_user email>
{
```

Additional values from sys\_update\_set record \(see **Customization** section below\)

```
}
{
```

Batch update set information: See the **Batch update sets** section below.

## Batch update sets

If an update set is part of a batch update set, that information is appended to the commit message in the following format, with the highest number being the Batch Base:

```
{
"1": {
"parent": "<name of parent update set>",
"description": "<description of parent update set>"
},
"2": {
"parent": " <name of parent 1’s parent update set> ",
"description": " <description of parent 1’s parent update set> "
}
}

```

## Customization

You can add additional fields to include in the commit message by adding a **glide.source\_control.historical\_commit\_fields** property. The value is a comma-separated list of fields the user wants to include from sys\_update\_set XML fields. Spaces and invalid or misspelled field names are ignored. This property is used for all applications that are linked to Source Control from the instance if the committer chooses to retain update set history.

**Note:** If the value of a field references another table or sys\_id, only the value of the field is added. For example: sys\_id for a user instead of the name of the user.

![Sample XML](../image/link-update-set-xml-example.png "XML example")

![Value of the property](../image/link-update-set-property-value.png "Value of the property")

![The result displaying in the commit message](../image/link-update-set-historical-commit.png "Result in commit message")

**Parent Topic:**[Legacy - Source Control integration](c_SourceControlIntegration.md)

