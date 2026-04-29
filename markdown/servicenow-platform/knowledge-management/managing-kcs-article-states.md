---
title: Managing KCS article states
description: Manage the readiness of KCS articles and comply with regulated information using KCS article states.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Managing KCS article states

Manage the readiness of KCS articles and comply with regulated information using KCS article states.

For information about the KCS article states, see [KCS v6 Practices Guide](https://library.serviceinnovation.org/KCS/KCS_v6/KCS_v6_Practices_Guide).

For information about all the KCS roles, see [Knowledge Management roles](../reference/r_KnowledgeRoles.md#).

## Activation information

Activate the Knowledge Management KCS Capabilities plugin \(com.snc.knowledge\_kcs\_capabilities\) to enable the use of KCS roles \(kcs\_contributor, kcs\_publisher, and kcs\_candidate\) and metadata fields for the KCS article state \(governance and confidence\). For more information, see [Activate Knowledge Management KCS Capabilities](../task/activate-kcs-capabilties-plugin.md).

**Note:** If you are not an admin and has either kcs\_contributor or kcs\_candidate roles, you cannot retire an article.

## Article confidence

The confidence state of an article indicates where the article is in its life cycle. Only users with the knowledge\_coach, knowledge\_admin, kcs\_contributor or kcs\_publisher role can modify the value of the **Confidence** field.

For articles existing before the Knowledge Management KCS Capabilities plugin \(com.snc.knowledge\_kcs\_capabilities\) was activated, the **Confidence** field is automatically set to **None**.

If an article is created after the Knowledge Management KCS Capabilities plugin \(com.snc.knowledge\_kcs\_capabilities\) is activated, the **Confidence** field is automatically set based on the workflow state of the article.

<table id="table_s5s_ghn_3lb"><thead><tr><th>

Workflow state

</th><th>

Confidence field value

</th></tr></thead><tbody><tr><td>

Draft, Review, or Scheduled for publish

</td><td>

Work in Progress

</td></tr><tr><td>

Published

</td><td>

-   Validated: For articles published by users with the knowledge\_coach, kcs\_contributor, or kcs\_publisher role.
-   Not Validated: For articles published by users with a role other than knowledge\_coach, kcs\_contributor, or kcs\_publisher.

</td></tr><tr><td>

Pending retirement or Outdated

</td><td>

Same as in the Published workflow state.

</td></tr><tr><td>

Retired

</td><td>

Archived

</td></tr></tbody>
</table>## Article governance

The governance state of an article indicates which users can manage articles specific to a regulatory requirement, either experience based or compliance based. Users with contribute access to a knowledge article can modify the value of the **Governance** field.

**Parent Topic:**[Using Knowledge Management](using-knowledge-management.md)

**Related topics**  


[Create a knowledge article from an incident in ITSM Agent Workspace](../task/create-knowledge-article.md)

[Create a knowledge article in Agent Workspace](../task/create-article-workspace.md)

