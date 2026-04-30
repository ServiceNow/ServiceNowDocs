---
title: Create and associate a policy document in Microsoft SharePoint
description: Enable redlining in a policy document that exists in your Microsoft SharePoint location instead of creating a document in Microsoft SharePoint and associating the document with the policy record.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Creating and associating policy texts from Cloud documents, Policy authoring and redlining in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create and associate a policy document in Microsoft SharePoint

Enable redlining in a policy document that exists in your Microsoft SharePoint location instead of creating a document in Microsoft SharePoint and associating the document with the policy record.

## Before you begin

Role required: Role required: sn\_compliance\_ws.corporate\_compliance\_analyst; mp\_document\_user

**Important:** Policy redlining integration with Microsoft SharePoint is available from Washington DC ServiceNow AI Platform version. The feature is not available even if you are on 19.x version of Vancouver.

## About this task

Apart from associating documents that reside in Microsoft OneDrive and Google Drive, you can now associate documents that are in Microsoft SharePoint site to your policy record.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, select the List icon \(![Lists icon.](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Navigate to **Compliance library** &gt; **My policies**.

    You can [create a new policy](../../grc-workspace-compliance/task/create-policy-ws.md) or open a policy record to associate a document.

4.  Select a policy to associate a policy document from the Microsoft SharePoint site.

    You can create a document in the Microsoft SharePoint site and associate to the policy record when the policy is in Draft state.

5.  From the Policy text related list of the policy record, select the **Enable document editing** UI action list and click the **Create new document** option.

6.  Enter the URL to the site in the **Site URL** field of the Create a Word document pop-up.

    You can get the site URL location information if you hover over the Site URL ![Site URL icon](../../grc-risk/image/icon-information.png) icon.

    1.  To get the site URL, log in to the Microsoft SharePoint site.

    2.  Select the **Share** list and click the **Copy link to page** option.

7.  Enter the path of the folder that you copied in the **Folder location** field.

    This path is the location where the document will reside.

8.  Enter the name of the document in the **Document name** field.

9.  Select **Create**.

    On selecting create, the document is created in the folder of the Microsoft SharePoint account that you provided. If you're providing a link to a shared folder, then you must have edit access to create a file within that folder.

    After the document is created, the contributors and policy owners who have access to the policy in the Draft state can edit the document in Microsoft SharePoint to add content.

10. To update the content in the **Policy text** field of the policy record, select the Update link below the document link.

    Alternatively, you can also select the **Open in Word** button.

    The content that is present in the specified document of the Microsoft SharePoint location is copied to the **Policy text** field. A message stating that **Policy text is updated with the latest content from policy document in the cloud** confirms that the content in the policy text and the document are in sync.

11. To view the users that have read or write access to the document, navigate to the Document access related list.

    After the document is associated with the policy record, the access for the policy users to the document is also established. The access to the policy document varies with users depending on their roles and the state of the policy.

    -   **Draft**

        If the policy is in Draft state, the Owner and Contributors have edit access.

    -   **Review**

        If the policy is in Review state, the Reviewers and Owners have edit access. However, the Contributors and Approvers have only read access.

    -   **Approved**

        If the policy moves to the Approved state, all the stakeholders of the policy have only read access.

    You can also verify the users' access rights by navigating to the Microsoft SharePoint document, selecting the **Share** list in the Microsoft SharePoint document and clicking **Manage Access**. Sometimes the access rights that users have on the ServiceNow policy document may not be the same as the rights that users have when they collaborate on the document in the Microsoft SharePoint site. This is because of the root permissions that are set in Microsoft SharePoint site, which get inherited to the folders within the site. The users of the folders within the site inherit those permissions. You can override the permissions.

    1.  To override the Microsoft SharePoint site permission, select the settings icon \(![Settings icon.](../../../reuse/icons/product-icons/gear-outline-24.svg)\).

    2.  Select **Site permissions** option in the **Settings** list.

    3.  Right-click the folder where the document resides and select **Manage Access**.

    4.  Select **Advanced settings** and click **Stop Inheriting Permissions**.

        This folder will no longer inherit permissions from the parent or from the Microsoft SharePoint site level. Now, when you provide access to the document from ServiceNow, then the same level of access that you see in the Document access related list will be available to the users collaborating on the Microsoft SharePoint document also.

12. If the policy has been drafted and is complete, the policy owner can request a review by selecting the **Request review** button.

    1.  Enter a message for the reviewers in the Request review pop-up.

    2.  Select **Request**.

        As a reviewer, you can view the policy when you log in to **My pending tasks** in the Tasks view, if it is ready for review.

    3.  Select the **Submit review** button.

        You can review the policy text, add a comment in the Submit review pop-up, and submit it.

13. To preview the document and to get the latest update after your reviewers have reviewed, select the Update link in the **Policy text** tab.

    Reviewers can add suggestions and comments in the document by selecting **Review** &gt; **Track Changes** &gt; **For everyone** in the Microsoft SharePoint.

    As a policy owner, you can fetch the updated content of the document from Microsoft SharePoint by clicking the **Update** link. This action maintains a sync between the content present in the Cloud document and the content in the policy text field of the policy.

    **Note:** Updates done frequently are not captured in the version history records of Microsoft SharePoint and the content may not be available in real time. Therefore, there can be a delay in fetching the latest updated content from Microsoft SharePoint to the policy text field.

    All activities between the policy owner and the reviewers are captured in the **Activity** tab of the **Details** related list. If all reviewers have completed the review, then the policy owner can complete the publishing checklist.

14. Select the **Complete publishing checklist** button.

    If all reviews are complete, then as a policy owner you can complete the publishing process. This action creates a playbook. The policy owner must go through the publishing checklist before requesting approval. See, [Complete publishing checklist for the policy and request approval](complete-publishing-checklist-redlining.md).

    After the publishing process is complete, you can either attach the policy as a PDF to the policy record or generate a Knowledge Base article when the policy moves to the Published state.

15. Select the attachments icon \(![Attachment icon.](../../../common/image/Form_Attachment.png)\) in the sidebar of the policy's Overview related list to see the PDF version of the Knowledge Base article.

16. To view the history of the policy, select the Policy history related list.

    For more information, see [View the history of a redlining-enabled policy](view-history-policy-redlining.md).


