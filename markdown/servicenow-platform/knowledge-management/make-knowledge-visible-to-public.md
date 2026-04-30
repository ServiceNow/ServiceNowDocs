---
title: Enable external or public users to view knowledge articles from the Knowledge Management Service Portal
description: Enable knowledge articles on the Knowledge Management Service Portal to be visible to external or public users.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable external or public users to view knowledge articles from the Knowledge Management Service Portal

Enable knowledge articles on the Knowledge Management Service Portal to be visible to external or public users.

## Before you begin

The Knowledge Management Service Portal plugin \(com.snc.knowledge\_serviceportal\) must be enabled.

Role required: admin

## About this task

If you are using Knowledge Management within the Customer Service Management \(CSM\) application, you can automatically make knowledge articles public by activating and running the Make KM Service Portal Pages Public fix script after you install the Customer Service Management plugin \(com.sn\_customerservice\).

If you are using Knowledge Management as a standalone application, perform the steps in this procedure.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Pages**.

2.  In the Pages list, search for and select **kb\_home**.

    **Note:** If the application scope isn't set to Knowledge Management - Service Portal, you cannot edit the form and a warning message appears. To make the form editable, click the word **here** at the end of the message.

3.  Enable public or external users to view knowledge articles from the Knowledge Management Service Portal.

<table id="table_k1y_dw4_tdb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Make knowledge service portal pages visible to public users

</td><td>

1.  On the Page form, select the **Public** check box.
2.  Click **Update**.


</td></tr><tr><td>

Make knowledge service portal pages visible to external users

</td><td>

1.  On the Page form, in the **Roles** field, click the edit user roles icon ![Edit User Roles icon.](../image/edit-user-roles.png).
2.  On the Roles form, move **snc\_external** from the available roles in the **Available** column to the **Selected** column.
3.  On the Roles form, click **Done**.
4.  On the Page form, click **Update**.


</td></tr></tbody>
</table>4.  Repeat the steps 2 and 3 for **kb\_article\_view** and **kb\_search** pages.

5.  Manage access to the articles for the Knowledge Management Service Portal pages.

    |Action|Description|
    |------|-----------|
    |Enable access to the knowledge base for public.|After you set the page to public as described in step 3, ensure that the Cannot Read and Can Read user criteria are not set and the **glide.knowman.block\_access\_with\_no\_user\_criteria** property is set to false for the knowledge bases you want to give access to public users.|
    |Enable access to the knowledge base for external users.|After you add the snc\_external role to the page as described in step 3, ensure that external users have read access to the knowledge bases for which you want to give access.|

    For more information about providing access to knowledge bases, see [Managing access to knowledge bases and knowledge articles](../concept/user-access-knowledge.md).


**Parent Topic:**[Configure the Knowledge Management Service Portal](../concept/knowledge-management-service-portal.md)

