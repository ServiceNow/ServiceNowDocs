---
title: Create a forum
description: Create a forum to provide a place for users to share content. You can configure forums for membership that registered community users request access to join. You can also configure forums to convert unstructured conversations to structured knowledge articles.
locale: en-US
release: xanadu
product: Communities
classification: communities
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure community forums, Configure a community, Communities, Customer Service Management]
---

# Create a forum

Create a forum to provide a place for users to share content. You can configure forums for membership that registered community users request access to join. You can also configure forums to convert unstructured conversations to structured knowledge articles.

## Before you begin

Role required: sn\_communities.admin

## About this task

A forum can be configured in the following ways.

<table id="table_my5_tjy_3bb"><tbody><tr><td>

Public

</td><td>

Visible to all users, including non-logged in users. All users have **content\_read** access to questions and answers in public forums. Configure public forms by adding a [forum user](add-user.md) of the type public.

</td></tr><tr><td>

Private

</td><td>

Visible only to users who have been assigned the required permissions in the forum. Configure private forums by adding a [forum user](add-user.md) of the type custom and adding specific users or user groups to that forum user.

</td></tr><tr><td>

Membership

</td><td>

The forum title is visible to registered community users. Community users must request membership to get full access to the content in the forum. Configure membership forums by selecting the **Enable Membership for this Forum** check box.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **Community** &gt; **Administration** &gt; **Forums**.

2.  In the Forums list, click **New**.

3.  Fill in the fields on the form as appropriate.

<table id="table_ysd_btl_xz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the forum.

</td></tr><tr><td>

Description

</td><td>

A short description that defines the forum.

</td></tr><tr><td>

Image

</td><td>

An image that provides a visual reference to describe the forum.

</td></tr><tr><td>

Order

</td><td>

The order that forums are displayed in. By default, the display is alphabetical. Enter a numerical value to set the order that forums are displayed in. You can combine both options.

</td></tr><tr><td>

Parent

</td><td>

The parent forum, if required. This lists the forum as a sub forum of the parent forum.

</td></tr><tr><td>

Enable Membership for this Forum

</td><td>

Check box to make the forum membership only, and enable registered forum users to request to join the forum. If you select this check box, the forum title is visible to all registered community users. Community users must request access to join the forum to see the content. **Note:** The **Approval Workflow for Membership** field appears when you select this check box.

</td></tr><tr><td>

Approval Workflow for Membership

</td><td>

The workflow for approving new members of a forum.

</td></tr><tr><td>

Knowledge Base used for harvesting

</td><td>

The knowledge base used for harvesting community discussions to knowledge articles.

</td></tr></tbody>
</table>4.  To allow registered forum users to view and request to join a forum, select the **Enable Membership for this Forum** check box and complete the following steps.

    1.  Right-click the form header and click **Save**.

        Two default permissions are added to the forum in the **Forum Permissions** related list.

        -   **Default Permission for Memberships**: Read and write access to questions and answers for users who are forum members.
        -   **Forum Visible**: Read access to the name and description of the forum for registered users. To access content, users must request forum membership.
    2.  If required, you can add a [new forum permission](create-forum-permission.md) and set it as the default using the sn\_communities.default\_permission\_for\_forum\_memberships property.

        If you want public users to view content in the forum to attract them to become members, create a forum permission as follows:

        -   **Forum User**: **Public**.
        -   **Permission**: **Question &amp; Answer Read**.
    3.  In the **Approval Workflow for Membership** field, perform one of the following options.

<table id="choicetable_qcd_dlc_t1b"><tbody><tr><td id="d132769e348">

**Leave the __Approval Workflow for Membership__ field blank.**

</td><td>

Membership requests to the forum are automatically approved.

</td></tr><tr><td id="d132769e360">

**Select the preconfigured approval workflow __Forum Membership Approval__.**

</td><td>

A task is created and sent to the community or forum administrator for approval.

</td></tr><tr><td id="d132769e372">

**Select a workflow that you have created.**

</td><td>

A task is created and sent to the users defined in your workflow for approval.

</td></tr></tbody>
</table>5.  Click **Update**.


**Parent Topic:**[Configure community forums](configure-forums-topics.md)

**Related topics**  


[Add a topic to a forum](add-topic-to-forum.md)

[Configure community content types](enable-content-types-for-community.md)

[Create a forum permission](create-forum-permission.md)

