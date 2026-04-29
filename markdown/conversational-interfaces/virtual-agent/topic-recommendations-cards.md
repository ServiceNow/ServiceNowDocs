---
title: Topic Recommendations cards
description: Recommended topic and intent cards display the status of the recommendation, allowing you to track them more easily over time.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Virtual Agent, Topic Recommendations, cards, intent, status, track]
breadcrumb: [Topic Recommendations interface reference, Using Virtual Agent Topic Recommendations, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Topic Recommendations cards

Recommended topic and intent cards display the status of the recommendation, allowing you to track them more easily over time.

## Card status

Topic and intent recommendations appear as cards. The status lets you know what action has been taken, if any, for each recommendation.

![Intent recommendations with various statuses.](../images/va-topic-recommendations-status.png "Example intent recommendation cards")

<table id="table_pcn_dbd_npb"><thead><tr><th>

Status

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New

</td><td>

Topic or intent has never been added to Virtual Agent.Cards with **New** status have a dark gray border.

</td></tr><tr><td>

Active

</td><td>

Topic or intent was added to Virtual Agent or [linked to an existing topic](../task/link-tr-existing-va-topic.md) and published.Cards with **Active** status have a green border.

 If you keep getting recommendations for an Active topic, it probably needs improvement.

</td></tr><tr><td>

Inactive

</td><td>

Topic or intent was added to Virtual Agent but never published, or it was linked to an existing, unpublished topic.Cards with **Inactive** status have a light gray border.

 If you keep getting recommendations for an Inactive topic, take steps to publish it and make it active.

</td></tr><tr><td>

Hidden

</td><td>

Topic or intent was not added to Virtual Agent, but it was marked as hidden from the aggregate view and has a status of **Hidden**.

</td></tr></tbody>
</table>## Overlay cards

To get more details about a pre-built topic or user intent, select the recommendation card, and then click the info icon to open an overlay card.

The overlay card includes a description of the pre-built topic or user intent and the following information, which can provide insight into why the topic or intent was recommended.

<table id="table_ark_zm1_mrb"><thead><tr><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Per contact, VA could save

</td><td>

How long it takes for Virtual Agent to resolve an intent \(displayed in minutes\).

</td></tr><tr><td>

How they contacted you

</td><td>

The way in which users engaged with support. For example, **phone** or **email**.

</td></tr><tr><td>

Who handled the ticket

</td><td>

The assignment group.

</td></tr><tr><td>

Language

</td><td>

The languages of users interacting with support for this issue.

</td></tr><tr><td>

Topic completion

</td><td>

Graph that shows a snapshot of topic completion over a window of time. This information displays for active topics only.

</td></tr><tr><td class="sub-head" colspan="2">

Status area

</td></tr><tr><td class="sub-head" colspan="2">

This section displays one of the following statuses.

</td></tr><tr><td>

How to apply this recommendation

</td><td>

Suggestions for an unused recommendation. You can do one of the following:

-   Select the card, and then click **Add to VA** to create a new topic.
-   [Link the recommendation](../task/link-tr-existing-va-topic.md) to an existing topic.

</td></tr><tr><td>

Added topic recommendation

</td><td>

Displays the name of the topic that was added for the recommendation, as well as the date when it was added.Click the open link icon ![Open link icon.](../images/icon-open-link.png) to view the topic in Assistant Designer.

</td></tr><tr><td>

Linked topic

</td><td>

Displays the name of the topic that was linked, as well as the date when the recommendation was linked. Click the open link icon ![Open link icon.](../images/icon-open-link.png) to view the associated topic in Assistant Designer. You can also [unlink the topic](../task/unlink-tr-va-topic.md) from the recommendation.

</td></tr></tbody>
</table>![An overlay card for a topic that has not been added but can be linked to an existing topic.](../images/tr-example-overlay-card.png "Example overlay card")

