---
title: Connect an existing document in Microsoft SharePoint
description: Connect a document that exists in your Microsoft SharePoint folder to a policy that you created. Use this existing document and enable redlining in the policy text instead of creating a document.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and associate policy document in Microsoft SharePoint, Create and associate policy texts, Policy authoring and redlining, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Connect an existing document in Microsoft SharePoint

Connect a document that exists in your Microsoft SharePoint folder to a policy that you created. Use this existing document and enable redlining in the policy text instead of creating a document.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst; mp\_document\_user

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, select the List icon \(![Lists icon.](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Navigate to **Compliance library** &gt; **My policies**.

4.  Select a policy.

    The policy must be in **Draft** state, only then the policy owner can associate a document from Microsoft SharePoint to enable the policy text for the approvers, reviewers, and contributors to edit.

5.  Select the Policy text related list to view the contents of the policy.

    If you already have a document on Microsoft SharePoint with relevant policy content, which you want to associate with the policy, then you can associate that document to the policy.

6.  To connect a document that is in your Microsoft SharePoint folder.

    1.  Log in to Microsoft SharePoint site.

    2.  Navigate to the document that you want to connect to the policy.

    3.  Select the **Share** list in the Home page and click the **Copy link to page** option.

7.  Navigate back to the Policy text related list of the policy record.

8.  Select the **Enable document editing** list and click the **Connect existing document** option.

9.  Paste the copied Microsoft SharePoint site URL in the **Site URL** field of the Connect existing Word document pop-up.

10. Enter the details in the **Folder path** and **Document name** fields.

11. Select **Connect**.

    A message appears stating that Microsoft Word editing is enabled. The policy record is connected to the document.

12. Select **Update**.

    The **Policy text** field displays the text from the Microsoft SharePoint document in the ServiceNow policy record.


