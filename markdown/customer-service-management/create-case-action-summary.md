---
title: Create a case action summary
description: Create a case action summary for a customer service case.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer Service case digests, Configure case digests, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a case action summary

Create a case action summary for a customer service case.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice\_manager, or admin

## About this task

You can send case action summaries for customer service cases that are in any states other than **New** or **Closed**.

After creating a case action summary, the record is added to the Case form in the Related Records form section. Closing a case automatically closes the corresponding case action summary.

## Procedure

1.  Open a customer service case.

2.  To create a case action summary, do one of the following.

    -   Agent Workspace: Click the More UI Actions icon \(![More UI Actions icon.](../image/agent-workspace-more-ui-actions-icon.jpg)\) and select **Send Case Action Summary**.
    -   Platform interface: Click the form context menu icon and select **Send Case Action Summary**.
    This opens a new Case Action Summary form with a status of **In progress**. Depending on the table map configuration defined for the case action summary, some of the information from the case is copied to the Case Action Summary form. With the CAS Configuration, this includes the information from the **Short description** field.

    **Note:** The **Short description** field on the Case Action Summary form can be edited in the platform interface but cannot be edited in Agent Workspace.

3.  In the Case Action Summary form, enter any necessary information in the following fields.

    |Field|Description|
    |-----|-----------|
    |Additional internal recipients|Select a recipient list. When an agent clicks **Publish to Case &amp; Notify**, the system sends an email notification to the internal users in the selected list.|
    |Short description|The short description from the case.|
    |Case summary|A brief summary of the case.|
    |Actions taken|Details about actions taken so far to resolve the case.|
    |Next steps|The steps that the agent is planning to take in order to resolve the case. This field is not customer visible.|
    |Internal notes|Other internal information that the agent wants to share regarding the case. This field is not customer visible.|

4.  Click **Preview** to generate the case action summary and view it in the Preview Document pop-up window.

5.  Make any desired changes to the fields on the Case Action Summary form and click **Preview** again.

6.  Click **Update** to save the changes to the case action summary.

7.  Publish the case action summary using one of the following actions.

<table id="choicetable_dzr_w4v_d3b"><thead><tr><th align="left" id="d75208e238">

Action

</th><th align="left" id="d75208e241">

Description

</th></tr></thead><tbody><tr><td id="d75208e247">

**Publish to Case**

</td><td>

Updates the case with the case action summary. -   Information from the customer-visible fields on the case action summary is added to the **Additional comments** field on the Case form.
-   Information from the case action summary is added to the **Work notes** field on the Case form.


</td></tr><tr><td id="d75208e271">

**Publish to Case &amp; Notify**

</td><td>

Updates the case with the case action summary as described above and sends an email with the case action summary to the internal stakeholders in the recipient list selected in the **Additional internal recipients** field. **Note:** The **Publish to Case &amp; Notify** UI action is available when a list has been selected in the **Additional internal recipients** field.

</td></tr></tbody>
</table>
