---
title: Grouping attachment search results with their parent search results
description: Search application administrators can control whether attachment search results appear grouped with their parent search results or whether they display on their own. By default, AI Search displays attachments grouped with their parent search results.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Search application configurations, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Grouping attachment search results with their parent search results

Search application administrators can control whether attachment search results appear grouped with their parent search results or whether they display on their own. By default, AI Search displays attachments grouped with their parent search results.

By default, AI Search displays separate search results for the parent record and each of its attachments that matches the user's search. Search administrators can enable grouping of attachment search results with the results for their parent records. With this option enabled, search results for attachments that match a user's search display inline with the search results for their parent record.

The maximum number of attachments per parent search result is set by the **Attachment Limit** field in the search application's configuration record. For details on this field, see [Search Application Configuration form](../reference/search-app-config-form-ais.md).

## Grouped attachments in the search results UI

If the parent record itself or any of its attachments matches the user's search, the parent record appears in the search result list. Grouped attachments that match the search appear in collapsed form, in descending relevancy order within the search result for their parent record.

![Search results page showing incident search result with three grouped attachment results and Show more link indicating that two additional grouped attachments are hidden.](../image/group-attachments-show-more.png)

By default, a parent search result shows up to three attachments in collapsed format. If it has more than three attachments, a **Show more** link appears, with a number indicating how many attachments are hidden in the current view. When you select this link, the hidden attachments appear and the link name changes to **Show less**. Selecting this link hides the overflow attachments again.

![Search results page showing incident search result with five grouped attachment results and Show less link.](../image/group-attachments-show-less.png)

## Viewing or downloading attachment search results

Selecting an attachment search result downloads the original attachment to your web client, or opens the original attachment in Document Viewer if all of these conditions are met:

-   Document Viewer is active on your instance.
-   Document Viewer is enabled for the attachment's source table.
-   The **useAttachmentViewer** EVAM property is set to **true** for the parent search result.

For details on activating and enabling Document Viewer, see [Enable Document Viewer](https://www.servicenow.com/docs/access?context=enable-document-viewer&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US). To learn more about EVAM property settings for search results, see [Configure EVAM display settings for search results in AI Search applications](../task/configure-search-result-card-opts.md).

## Relevancy and click rank for grouped attachment search results

When attachment grouping is in use, AI Search computes relevancy scores for the parent record and each of its grouped attachments. The final relevancy score of the grouped search result is the highest of these individual relevancy scores.

**Note:** When you select a grouped attachment search result, AI Search logs click rank signal data for the parent record search result. All other search signal data is specific to the selected attachment record. For more details on search signal logging, see [Search signal tables](../../search-administration/reference/search-signal-tables.md).

-   **[Group attachment search results with their parent results](../task/group-attachment-srch-results-ais.md)**  
Configure your AI Search applications to display attachment search results grouped with the results for their parent records.

**Parent Topic:**[Search application configurations](defining-search-app-cfgs-ais.md)

