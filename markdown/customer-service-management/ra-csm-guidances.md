---
title: Guidances in Recommended Actions
description: A guidance is an action that an agent can take or information that an agent can share as they work to resolve tasks, such as customer service cases.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Recommended Actions, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Guidances in Recommended Actions

A guidance is an action that an agent can take or information that an agent can share as they work to resolve tasks, such as customer service cases.

Guidances appear as cards in the contextual side panel in a workspace. Agents can access these guidance cards by selecting the Recommended Actions icon in the contextual side panel. Agents can then perform the actions by selecting a button on a card.

![Guidance cards recommending the agent to view and attach a knowledge article or attach and add the link in comment as primary action](../image/ra-attach-types.png "Recommended actions guidance cards")

Guidances include actions such as sharing a knowledge article, creating a case task or a work order, or copying the resolution notes from a similar case. For a detailed list of guidances, see the following table.

<table id="table_myy_ymj_cdc"><thead><tr><th>

Guidance

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Apply resolution from a solved case

</td><td>

Applies the resolution from an existing solved case.

</td></tr><tr><td>

Attach and share article

</td><td>

Enables the agent to attach a knowledge article to a case and share the article with the customer.

</td></tr><tr><td>

Communicate workaround

</td><td>

Communicates a workaround to the customer.

</td></tr><tr><td>

Copy resolution notes

</td><td>

Copies the resolution notes from the recommended case to the current case.

</td></tr><tr><td>

Create work order

</td><td>

Creates a work order for a case.

</td></tr><tr><td>

Default guidance for search results

</td><td>

Default guidance that can be used for any search sources that don't have dedicated mapped guidances. For more information, see the following topics:

-   [Automatically map AI search results with guidance inputs](ra-configuring-ai-search-automatically.md)
-   [Default guidance for search results](ra-csm-guidances-default-guidance-search.md)

.

</td></tr><tr><td>

Link case

</td><td>

Links the current case as a child of the recommended case.

</td></tr><tr><td>

Link case to existing defect

</td><td>

Links a case to an existing defect.

</td></tr><tr><td>

Open collab chat

</td><td>

Opens the collaboration chat modal.

</td></tr><tr><td>

Propose major issue

</td><td>

Proposes the current case as a major case.

</td></tr><tr><td>

Propose resolution

</td><td>

Proposes a resolution for a case.

</td></tr><tr><td>

Read message to customer

</td><td>

Directs the agent to read a message to the customer.

</td></tr><tr><td>

Reassign case

</td><td>

Reassigns the case to a different assignment group.

</td></tr><tr><td>

Review and attach article

</td><td>

Enables the agent to review and attach a knowledge article to a case.

</td></tr><tr><td>

Share KB in chat interactions

</td><td>

Shares a knowledge article in the chat window in an interaction record.

</td></tr><tr><td>

Similar major case

</td><td>

Displays similar major cases.

</td></tr></tbody>
</table>## Attaching and sharing knowledge articles

Agents can use two different guidances to view and attach knowledge articles to task records and chat interaction records and share articles with customers.

<table id="table_pj1_rlv_bdc"><thead><tr><th>

Guidance

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Attach and share article](ra-csm-guidances-attach-share-article.md)

</td><td>

This guidance recommends knowledge articles to an agent who is working on a task, such as a case record. The guidance displays relevant articles and enables the agent to select an article and share it in a comment, a work note, or an email:-   Attach and add link in comment
-   Add link in work note
-   Attach and add link in email

</td></tr><tr><td>

[Share KB in chat interactions](ra-csm-guidances-share-kb-chat.md)

</td><td>

This guidance recommends knowledge articles to an agent who is working on a chat interaction. The guidance displays relevant articles and enables the agent to select an article and share it in the chat conversation using Add link in message feature.

</td></tr></tbody>
</table>## Configuring Recommended Actions guidances

Recommended Actions is a component that you can add to a record page in UI Builder. You can find information about configuring the Recommended Actions component, including the properties and events, in the [Next Experience Components](https://developer.servicenow.com/dev.do#!/reference/now-experience/rome/components) documentation.

The Recommended Actions component includes two views: a preview view \(card view\) and a detail view \(full article view\). How these views are displayed is determined by the Recommended Actions configuration. For more information, see the following topics:

-   [Create a guidance in Recommended Actions](../task/ra-csm-guidances-create.md)
-   [Configure a guidance preview experience](../task/ra-csm-guidance-configure-preview.md)
-   [Customize a guidance preview experience in UI Builder](../task/customize-ra-preview-experience.md)
-   [Customize a guidance detail view in U Builder](../task/customize-ra-detail-experience.md)

The Recommended Actions component includes **Recommended Action Specific Configuration** property. Users with the administrator role can use this property to configure the following settings:

-   Select which type of experience to uptake on a record page: modal or modeless dialog.
-   Select which of the guidance actions to show or hide.
-   Order the guidance actions to determine the primary action \(displayed as a button on the guidance card\) and secondary actions \(displayed on the overflow menu\).

The **Recommended Action Specific Configuration** property is available in the Configure tab of the Recommended Actions component and includes expandable sections for each guidance.

## Access to internal field values for predicted records

When accessing data for a predicted record within the Recommended Actions framework, the system provides the internal field values, in addition to display values, through standard guidance inputs. The system does so without requiring data brokers or custom scripts. By enabling direct access to internal values, the framework can support more complex logic, reduce performance bottlenecks, and verify consistent UI behavior across languages.

For catalog items:

-   When the catalog item type field is used in a catalog item prediction, the system returns the internal value \(for example, the catalog item or order guide\) along with the sys\_id.
-   When the catalog item type field is accessed in a translated environment, the system relies on the internal field value instead of the display value to verify the language settings do not affect condition fulfillment.

For custom guidances based on the incident state:

-   When custom guidance logic is applied to a predicted incident with a specified state, the system accesses the internal value of the incident’s state field directly.
-   When the state field is required for custom actions like linking an incident as a parent or copying resolution notes, the internal value should be accessible without causing UI performance issues or delays.

