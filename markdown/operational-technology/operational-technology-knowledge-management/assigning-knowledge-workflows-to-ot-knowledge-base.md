---
title: Assigning knowledge workflows to an OT knowledge base
description: You can assign different Knowledge Management workflows to each Operational Technology \(OT\) knowledge base for the publishing and retiring processes.
locale: en-US
release: australia
product: Operational Technology Knowledge Management
classification: operational-technology-knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Operational Technology Knowledge Management, Operational Technology]
---

# Assigning knowledge workflows to an OT knowledge base

You can assign different Knowledge Management workflows to each Operational Technology \(OT\) knowledge base for the publishing and retiring processes.

## Knowledge workflow overview

You can use the default Knowledge Management workflows in the following table for Operational Technology Knowledge Management and apply them to OT knowledge bases.

**Note:** For the workflows that require approval, you can configure which users can approve or reject by editing the `getApprovers()` function in the `KBWorkflow` script include.

<table id="table_cvl_3lh_lzb"><thead><tr><th>

Workflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge - Approval Publish

</td><td>

Requests approval from a manager of the knowledge base. Articles in approval have a state of **In Review** before moving to a **Published** state after approval. If they're set to publish later, they’re moved to a **Scheduled** state. If the manager rejects the request, the workflow is canceled and the article remains in the **Draft** state. If the**ownership groups** option is enabled, email notifications with a link to the article are sent to the ownership group members for approval.

 If the **ownership groups** option isn't enabled, email notifications with a link to the article are sent to the knowledge base managers for approval.

 A notification is also sent to the authors or the revisers of the articles to inform them that their article has been approved or rejected.

 To turn on the approval email notifications, set the **glide.knowman.enable\_approval\_notification** property to `true`.

 **Note:** Only the active user receives the notifications.

</td></tr><tr><td>

Knowledge - Approval Retire

</td><td>

Requests approval from a manager of the knowledge base before moving the article to the retired state. If any manager rejects the request, the workflow is canceled and the article remains in the **Published** state.If the **ownership groups** option is enabled, email notifications with a link to the article are sent to the ownership group members for approval.

If the **ownership groups** option isn’t enabled, email notifications with a link to the article are sent to the knowledge base managers for approval.

</td></tr><tr><td>

Knowledge - Instant Publish

</td><td>

Immediately publishes a draft article without requiring an approval, or publishes on the scheduled publish date if set to publish later.

</td></tr><tr><td>

Knowledge - Instant Retire

</td><td>

Immediately retires a published article without requiring an approval.

</td></tr><tr><td>

Knowledge - Publish Knowledge

</td><td>

Subflow that moves the knowledge article to the **Published** state. You can use this subflow when defining your own workflow.

</td></tr><tr><td>

Knowledge - Retire Knowledge

</td><td>

Subflow that moves the knowledge article to the **Retired** state. You can use this subflow when defining your own workflow.

</td></tr></tbody>
</table>## Email notifications for approval workflows

You can send email notifications for approval workflows.

-   Notify approvers about the knowledge articles submitted for their approvals.
-   Notify authors about the approval status of their knowledge articles

To send email notifications for approval workflows, enable the **Send notification to approvers and authors in article approval workflow** property \(**glide.knowman.enable\_approval\_notification**\). Beginning with the New York release, the property is enabled by default. Existing customers on release versions prior to the New York release can enable this property to send email notifications. Disable any custom notifications for article approvals before enabling this property. If the **glide.knowman.enable\_approval\_notification** property isn’t available, an administrator can create the property and set its value to true. For more information, see [Knowledge Management properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/r_KnowledgeProperties.md).

**Parent Topic:**[Configuring Operational Technology Knowledge Management](configuring-operational-technology-knowledge-management.md)

