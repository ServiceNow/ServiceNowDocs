---
title: Knowledge flows
description: The publishing and retirement processes for a knowledge article are controlled by flows defined for the knowledge base that the article belongs to.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2025-08-20"
reading_time_minutes: 3
breadcrumb: [Knowledge Management reference, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge flows

The publishing and retirement processes for a knowledge article are controlled by flows defined for the knowledge base that the article belongs to.

Beginning with Zurich, Knowledge Flow is available to all new users of Knowledge Management.

The **Publish flow** and **Retire flow** fields are mandatory in the Knowledge Base form.

You can use the Out-of-Box \(OOB\) flows, or create your own to define custom publishing and retirement processes for different types of knowledge. For more information see, [https://www.servicenow.com/docs/bundle/vancouver-build-workflows/page/administer/flow-designer/concept/flow-designer.html](https://www.servicenow.com/docs/bundle/vancouver-build-workflows/page/administer/flow-designer/concept/flow-designer.html)

For the flows that require approval, you can configure which users can approve or reject by editing the getApprovers\(\) function in the KBWorkflow script include.

You cannot delete the approval records for knowledge flows. You can only approve or reject the records.

<table id="table_eqc_lfl_1r"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge - Approval Publish

</td><td>

Requests approval from a manager of the knowledge base. Articles in approval are In Review state before moving to Published state once approved or to Scheduled for publish if set to publish later. If the manager rejects the request, the flow is canceled and the article remains in Draft state. If ownership groups is enabled, email notifications with a link to the article are sent to the ownership group members for approval.

 If ownership groups is not enabled, email notifications with a link to the article are sent to knowledge base managers for approval.

 A notification is also sent to authors or revisers of articles to inform them that their article has been approved or rejected.

 To turn on approval email notifications, set the **glide.knowman.enable\_approval\_notification** property to `true`.

 **Note:** Only the active user receives the notifications.

</td></tr><tr><td>

Knowledge - Approval Retire

</td><td>

Requests approval from a manager of the knowledge base before moving the article to the retired state. The flow is canceled and the article remains in the published state if any manager rejects the request.If ownership groups is enabled, email notifications with a link to the article are sent to the ownership group members for approval.

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

Action for publishing an article.

</td></tr><tr><td>

Knowledge - Retire Knowledge

</td><td>

Action for retiring an article.

</td></tr></tbody>
</table>**Note:**

-   Only administrators and knowledge administrators can view the retired knowledge articles. To reuse a retired article, administrators and knowledge administrators can republish the article. For more information, see [Republish a retired article](../task/republish-retired-article.md).
-   An article and its translations have a parent-child relationship. Retiring a parent article does not automatically retire all its translated child articles.

## Email notifications for approval flows

You can send email notifications for approval flows.

-   Notify approvers about knowledge articles submitted for their approvals.
-   Notify authors about the approval status of their knowledge articles.

To send email notifications for approval flows, enable the **Send notification to approvers and authors in article approval flow** property \(**glide.knowman.enable\_approval\_notification**\). The property is enabled by default. If the **glide.knowman.enable\_approval\_notification** property is not available, an administrator can create the property and set its value to `true`. For more information, see [Knowledge Management properties](r_KnowledgeProperties.md#).

**Parent Topic:**[Knowledge Management reference](knowledge-management-reference.md)

