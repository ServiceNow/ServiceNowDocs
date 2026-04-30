---
title: Comment on a knowledge article
description: Comment on a knowledge article or reply to a comment.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Comment on a knowledge article

Comment on a knowledge article or reply to a comment.

## Before you begin

You must activate the Knowledge Management V3 plugin \(com.snc.knowledge3\).

Role required: User with Can Read access. Unauthenticated users and users with only the snc\_external role can’t add or view attachments for comments.

**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in the future Y release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers on Madrid and later releases. For more information about the new experience, see [Knowledge Management Service Portal homepage features](../concept/knowledge-service-portal-pages.md).

## Procedure

1.  Navigate to the Knowledge Management Service Portal.

2.  Click the article you want to comment or reply to a comment on.

3.  Select **Post a comment**.

    If you want to reply to an existing comment, select **Reply**

    ![post a comment](../image/post-comment.png "Post a comment")

4.  Enter your comment or reply and add links, images, and attachments as required.

    **Note:** Attachments to comments posted in the Knowledge Management Service Portal are not displayed in the Live Feed. If attachments to comments are posted in Live Feed, they are displayed in the Knowledge Management Service Portal.

    If antivirus protection is enabled, all attachments are automatically scanned for viruses once the comment is posted. Attachments are only displayed once the scan is finished and successful.

    If you are the author of the comment, you can delete it. All comments and replies underneath are automatically deleted.

5.  Click **Submit**.

    **Note:** When the Use Live Feed for Knowledge Feedback property is enabled, you can only view comments in the Live Feed. By default, it is set to inactive.

    Comments posted in Live Feed before upgrading to release version New York are not shown hierarchically in the Knowledge Management Service Portal. Comments posted in Live Feed after upgrading to release version New York are shown hierarchically in the Knowledge Service Portal.

    The following table illustrates how comments and replies to comments are displayed depending on where you are viewing them.

    |Viewing from|HTML formatting|Hierarchy|Attachments|
    |------------|---------------|---------|-----------|
    |Knowledge Management Service Portal|Yes|Yes|Yes|
    |Live Feed|No|Yes|Yes|
    |Knowledge Management v3|No|No|No|


**Parent Topic:**[Creating and maintaining articles](../concept/creating-and-maintaining-articles.md)

