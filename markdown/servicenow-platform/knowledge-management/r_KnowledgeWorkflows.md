---
title: Knowledge workflows
description: The publishing and retirement processes for a knowledge article are controlled by workflows defined for the knowledge base that the article belongs to.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Knowledge Management reference, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge workflows

The publishing and retirement processes for a knowledge article are controlled by workflows defined for the knowledge base that the article belongs to.

You can assign different workflows to each Knowledge Base.

You can use one of the default workflows, or create your own workflows to define custom publishing and retirement processes for different types of knowledge.

For the workflows that require approval, you can configure which users can approve or reject by editing the getApprovers\(\) function in the KBWorkflow script include.

<table id="table_eqc_lfl_1r"><thead><tr><th>

Workflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge - Approval Publish

</td><td>

Requests approval from a manager of the knowledge base. Articles in approval are In Review state before moving to Published state once approved or to Scheduled for publish if set to publish later. If the manager rejects the request, the workflow is canceled and the article remains in Draft state. If ownership groups is enabled, email notifications with a link to the article are sent to the ownership group members for approval.

 If ownership groups is not enabled, email notifications with a link to the article are sent to knowledge base managers for approval.

 A notification is also sent to authors or revisers of articles to inform them that their article has been approved or rejected.

 To turn on approval email notifications, set the **glide.knowman.enable\_approval\_notification** property to `true`.

 **Note:** Only the active user receives the notifications.

</td></tr><tr><td>

Knowledge - Approval Retire

</td><td>

Requests approval from a manager of the knowledge base before moving the article to the retired state. The workflow is canceled and the article remains in the published state if any manager rejects the request.If ownership groups is enabled, email notifications with a link to the article are sent to the ownership group members for approval.

 If ownership groups is not enabled, email notifications with a link to the article are sent to knowledge base managers for approval.

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

A subflow that moves the knowledge article to the published state. You can use this subflow when defining your own workflow.

</td></tr><tr><td>

Knowledge - Retire Knowledge

</td><td>

A subflow that moves the knowledge article to the retired state. You can use this subflow when defining your own workflow.

</td></tr></tbody>
</table>**Note:**

-   Only administrators and knowledge administrators can view the retired knowledge articles. To reuse a retired article, administrators and knowledge administrators can republish the article. For more information, see [Republish a retired article](../task/republish-retired-article.md).
-   An article and its translations have a parent-child relationship. Retiring a parent article does not automatically retire all its translated child articles.

## Email notifications for approval workflows

You can send email notifications for approval workflows.

-   Notify approvers about knowledge articles submitted for their approvals.
-   Notify authors about the approval status of their knowledge articles.

To send email notifications for approval workflows, enable the **Send notification to approvers and authors in article approval workflow** property \(**glide.knowman.enable\_approval\_notification**\). Beginning with New York, the property is enabled by default. Existing customers on release versions prior to New York can enable this property to send email notifications. Disable any custom notifications for article approvals before enabling this property. If the **glide.knowman.enable\_approval\_notification** property is not available, an administrator can create the property and set its value to `true`. For more information, see [Knowledge Management properties](r_KnowledgeProperties.md#).

**Parent Topic:**[Knowledge Management reference](../../../knowledge-management-reference.md)

**Related topics**  


[Knowledge article states](../concept/knowledge-article-states.md)

[Approve an article that is being reviewed](../task/approve-article-in-review.md)

[Retire a versioned article](../task/retire-versioned-article.md)

