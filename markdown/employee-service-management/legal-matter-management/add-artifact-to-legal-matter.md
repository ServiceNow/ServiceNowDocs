---
title: Create an artifact for a legal matter
description: Create an artifact for a legal matter to upload and store documents, emails, and files related to the matter.
locale: en-US
release: australia
product: Legal Matter Management
classification: legal-matter-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Work on a legal matter, Use, Legal Matter Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Create an artifact for a legal matter

Create an artifact for a legal matter to upload and store documents, emails, and files related to the matter.

## Before you begin

Role required: sn\_lg\_matter.matter\_fulfiller

## About this task

As a collaborator added to a legal matter, you can access and work on the legal matter just as matter owners can. However, you can't modify the **Matter owner**, **Assignment group**, and **Assignment group permission** fields.

Apart from the matter owner, a collaborator or a task fulfiller can also add an artifact to a matter task from the **Tasks** tab.

**Note:** If any files were attached to the request before it was promoted to a matter, a default artifact containing those files is created in that matter. If the external storage option is enabled, the documents in the artifact created from the requests are shared. So, the addition or deletion of any documents in this shared artifact is reflected in both request and matter. Also, the document permission for this shared artifact is managed at the legal request level and not at the legal matter level.

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  In the Legal Counsel Center tab, select the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, open a legal matter by selecting an option under **Matters**.

<table id="choicetable_qbl_2bj_gtb"><thead><tr><th align="left" id="d759015e108">

Option

</th><th align="left" id="d759015e111">

Steps

</th></tr></thead><tbody><tr><td id="d759015e117">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a legal matter to work on.
3.  If the legal matter is newly assigned to you, select **Start** to start working on it.

The state of the legal matter updates to Work in Progress.

</td></tr><tr><td id="d759015e146">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a legal matter to work on.


</td></tr></tbody>
</table>4.  To add an artifact, in the **Artifacts** tab, click **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|Unique number of the artifact.|
    |Parent matter|Matter with which the artifact is associated.|
    |Content type|Type of content the artifact can contain, such as emails, documents, or images.|
    |Short description|Short description for the artifact, for example, the name of the artifact.|
    |Description|Detailed description for the artifact, for example, the purpose and content of the artifact.|
    |Notes section|
    |Work notes|Comments or notes that only authorized users related to the artifact and parent matter can see.|

6.  Click **Save**.

    The artifact with the specified details is created.

7.  In the **External Links** tab, add the path or link to external files..

    1.  Click **New** to add a new storage path.

    2.  Enter a valid link to the storage folder and a short description.

    3.  Click **Save**.

8.  Associate the artifact with a matter task.

    **Note:** If you create an artifact from a matter task, the artifact is associated to the task by default.

    1.  In the **Matter Task** tab, select an artifact and click **Add**.

    2.  In the Add Legal Task dialog box, select a matter task and click **Add**.

    When the matter owner assigns this task to a group or a user, they get the access to the artifact automatically. Users who can access the artifact are listed in the **Artifact Users** tab.

9.  Revoke the access permission of users who were given default access through the associated matter task.

    1.  In the **Artifact Users** tab, select one or more users to whom you want to deny access to the artifact.

    2.  Click **Revoke permissions**.

    3.  Click **Save**.


## What to do next

[Attach files to a legal matter artifact](add-files-to-artifact.md).

-   **[Attach files to a legal matter artifact](add-files-to-artifact.md)**  
Upload supporting documentation, such as documents, email copies, images, or any other files into the artifact while you are working on a legal matter or matter task. You can also use these artifacts as a reference material to solve similar requests in future.
-   **[Document access in a legal matter](../concept/document-access-legal-matter.md)**  
Documents attached to legal matters are uploaded to the configured external storage system when the external storage option is enabled on an intake form with All or matter type selected. The access permission of these documents to various personas is controlled in real time, via a scheduled job, or on-demand.

**Parent Topic:**[Work on a legal matter](work-on-legal-matter-1.md)

