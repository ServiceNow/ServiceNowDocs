---
title: Attach and share article guidance
description: The Attach and share article guidance recommends relevant knowledge articles to customer service agents and enables them to share the selected articles in comments, work notes, or email.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Guidances, Recommended Actions, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Attach and share article guidance

The Attach and share article guidance recommends relevant knowledge articles to customer service agents and enables them to share the selected articles in comments, work notes, or email.

The Attach and share article guidance recommends relevant knowledge articles based on the text in the case short description. Agents can view the recommended articles and share a selected article with the customer.

The agent can view the knowledge articles in a card format in the contextual side panel or expand a selected card to see an article in a detail view. The card view provides a condensed view of articles for quick scanning. The detail view provides the full content of the selected article for further reading.

Each card contains a primary action. The default primary action is [Attach and add link in comment](ra-csm-guidances-attach-share-article.md#section_yvx_rm4_cdc). Secondary actions are available in the More actions menu in the upper right corner of the card:

-   [Add link in work notes](ra-csm-guidances-attach-share-article.md#section_qll_xm4_cdc)
-   [Attach and add link in email](ra-csm-guidances-attach-share-article.md#section_bfj_1n4_cdc)

The same primary and secondary actions are available in the expanded detail view. The system administrator can configure the primary and secondary actions in the **Recommended action specific configuration** property. For more information, see [Configuring guidances in UI Builder](ra-csm-guidances.md#section_d5n_l2f_ddc).

The relevancy score displays on the Attach and share article guidance in the Search tab of the Recommended Actions contextual side panel. It indicates how well a search result matches the agent’s query.

## Modal and modeless dialog experiences

The agent can share the article in a comment, a work note, or an email using the primary and secondary actions. Two different experiences are available for this guidance depending on the [record page](csm-config-workspace-record-pages.md) you are using in the CSM Configurable Workspace:

-   **Modeless dialogs**: This experience is available for record pages that support [modeless dialogs](csm-front-line-case-page-modeless-dialogs.md) \(for example, the [Front-line case page](csm-front-line-case-page.md)\). Modeless dialogs are windows that overlay the main window content. Agents can move modeless dialogs around the window so they can interact with the window content and overlay content at the same time.
-   **Modals**: This experience is available for record pages that support modals \(for example, the [CSM default record page](csm-default-record-page.md)\). With modals, agents must complete the action within a modal before continuing to interact with the window content, which is the default experience.

The system administrator can configure the modal and modeless dialog experiences in the **Recommended Action Specific Configuration** property. For more information, see [Configuring guidances in UI Builder](ra-csm-guidances.md#section_d5n_l2f_ddc).

If a record page supports the modeless dialog experience, selecting an action on a guidance card opens the corresponding modeless dialog. If a record page does not support the modeless dialog experience, the guidance uses the modal experience.

**Note:** The result of guidance actions is the same in the modeless dialog and modal experiences, but when the actions are completed differs.

## Public and private knowledge articles recommendations for case records

Some knowledge articles that appear in the search results display a lock icon in the upper left corner. The presence or absence of the lock icon determines the audience for the article and how an agent can share the article.

The **KnowledgeGuidanceUserResolver** extension point is shipped with the base system. This extension point allows business units \(BUs\) to return the requester and primary action based on their logic by creating the implementation in this extension point. You can create an implementation by selecting the **Create Implementation** link in the **KnowledgeGuidanceUserResolver** extension point. The `CSMKnowledgeGuidanceUserResolver` implementation for the Case table and its extended tables is shipped with the base system. This implementation identifies the primary requesters for a case record based on the Contact, Partner Contact, Consumer and Internal user fields in the Case table. The primary action is determined based on the channel type of the case record.

**Note:** The Internal user field is checked only when the Service Organization \(com.snc.service\_organization\) plugin is installed.

-   **Lock icon**

    Agents can’t share locked articles with customers as the customers do not have access to these locked article. The **Attach and add link in email** and **Attach and add link in comment** actions are not available when a lock icon is present on a guidance card. The following table shows the primary and secondary actions in preview and detail view on the guidance card:

<table id="table_uzp_5tr_1gc"><thead><tr><th>

Action type

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Preview

</td></tr><tr><td>

Primary actions

</td><td>

The default primary action is **Read article**.

</td></tr><tr><td>

Secondary actions

</td><td>

-   Share in work notes
-   Copy Link


</td></tr><tr><td colspan="2">

Detail view

</td></tr><tr><td>

Primary actions

</td><td>

The default primary action on the guidance card is **Read article in full view**.

</td></tr><tr><td>

Secondary actions

</td><td>

-   Share in work note
-   Copy Link
-   Flag article
-   Mark as helpful


</td></tr></tbody>
</table>-   **No lock icon**

    Agents can share these articles with both customers and internal users. The following table shows the primary and secondary actions in preview and detail view on the guidance card:

<table id="table_lfw_nvr_1gc"><thead><tr><th>

Action type

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Preview

</td></tr><tr><td>

Primary action

</td><td>

The default primary action by channel:-   Email channel: [Attach and add link in email](ra-csm-guidances-attach-share-article.md#section_bfj_1n4_cdc)
-   Other channels: [Attach and add link in comment](ra-csm-guidances-attach-share-article.md#section_yvx_rm4_cdc)


</td></tr><tr><td>

Secondary actions \(available in the more options menu\)

</td><td>

-   Read article
-   Attach and share in work notes
-   Share in email
-   Flag article
-   Mark as helpful


</td></tr><tr><td colspan="2">

Detail view

</td></tr><tr><td>

Primary action

</td><td>

The default primary action:-   Email channel: [Attach and add link in email](ra-csm-guidances-attach-share-article.md#section_bfj_1n4_cdc)
-   Other channels: [Attach and add link in comment](ra-csm-guidances-attach-share-article.md#section_yvx_rm4_cdc)


</td></tr><tr><td>

Secondary actions \(available in the more options menu\)

</td><td>

-   Read article
-   Attach and share in work notes
-   Share in email
-   Flag article
-   Mark as helpful
-   Read article in full view


</td></tr></tbody>
</table>
## Attach and add links in comments

Use this action to attach a knowledge article to a case record and share the link in the activity stream. The behavior of the action depends on the modal or modeless dialog experience.

<table id="table_s3n_nvk_ddc"><thead><tr><th>

Experience

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Modal

</td><td>

This action does the following:-   Opens the Compose a comment modal.
-   Inserts the article link in the **Comments** field.

The agent can add information to the **Comments** field and select **Post Comments**.

-   The knowledge article is attached to the case record.
-   The activity stream is updated with the article attachment \(as an internal post\).
-   The comment and the link are posted to the activity stream \(as an external post\).
-   The guidance is marked as complete and moved to the Recommended Actions History tab.

This action is available as the primary action on the knowledge article card.

**Note:** This guidance is available by default.

</td></tr><tr><td>

Modeless dialog

</td><td>

This action does the following:-   Attaches the article to the case record. The article is available in the Attached Knowledge related list.
-   Updates the activity stream with the article attachment as an internal post.
-   Marks the guidance as complete and moves it to the History tab.
-   Opens the Compose a comment modeless dialog.
-   Inserts the article link in the **Comments** field.

The agent can add information to the **Comments** field and select **Post Comments**. The comment is posted to the activity stream as an external post.

</td></tr></tbody>
</table>## Add link in work note

Use this action to attach a knowledge article to a case record in the work notes. The behavior of the action depends on the modal or modeless dialog experience.

<table id="table_qxv_xpl_ddc"><thead><tr><th>

Experience

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Modal

</td><td>

This action does the following:-   Opens the Compose a work note modal.
-   Inserts the article link in the **Work notes** field.

The agent can add information to the **Work notes** field and select **Post work notes \(private\)** to post the work note and the link to the activity stream as an internal post.

-   The activity stream is updated with the article attachment as an internal post.
-   The guidance is marked as complete and moved to the Recommended Actions History tab.

This action is available as a secondary action in the More actions menu.

**Note:** This guidance is available by default.

</td></tr><tr><td>

Modeless dialog

</td><td>

This action does the following:-   Opens the Compose a work note modeless dialog.
-   Inserts the article link in the **Work notes** field.

The agent can add information to the **Work notes** field and select **Post work notes \(private\)** to post the work note and the link to the activity stream as an internal post. The guidance is marked as complete and moved to the History tab.

</td></tr></tbody>
</table>## Attach and add links in emails

Use this action to attach a knowledge article to a case record and share the link in an email. The behavior of the action depends on the modal or modeless dialog experience.

<table id="table_bt5_wql_ddc"><thead><tr><th>

Experience

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Modal

</td><td>

This action does the following:-   Opens the Email compose modal.
-   Inserts the article link in the body of the email.
-   If available, an email template auto-fills modal fields.

The agent can add information to the email and select **Send email**.

-   The email is sent.
-   The knowledge article is attached to the case and is available in the Attached Knowledge related list.
-   The activity stream is updated with the article attachment \(as an internal post\).
-   The guidance is marked as complete and moved to the Recommended Actions History tab.

This action is available as a secondary action in the More actions menu.

**Note:** This guidance is available by default with the modeless dialog experience. For the modal experience, it must be configured by the system administrator.

</td></tr><tr><td>

Modeless dialog

</td><td>

This action does the following:-   Attaches the article to the case record. The article is available in the Attached Knowledge related list.
-   Updates the activity stream with the article attachment as an internal post.
-   Marks the guidance as complete and moves it to the History tab.
-   Opens the Email compose modeless dialog.
-   Inserts the article link in the body of the email.
-   If available, an email template auto-fills email fields.

The agent can add information to the email and select **Send email**.

</td></tr></tbody>
</table>## More actions menu

The More actions menu on a guidance card includes several actions in addition to **Add link in work notes** and **Attach and add link in email**.

In the card view, these actions include:

-   Read article
-   Copy link

In the detail view, these actions include:

-   Read article in full view
-   Copy link
-   Mark article as helpful
-   Flag article

