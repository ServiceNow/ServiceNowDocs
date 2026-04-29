---
title: Set up AI Enhanced Recommended Actions for Operational Technology Service Management \(OTSM\)
description: Set up AI Enhanced Recommended Actions for Operational Technology Service Management \(OTSM\) so that you can contextualize external sources related to an Operational Technology \(OT\) incident.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, AI Enhanced Recommended Actions for OTSM, Operational Technology]
---

# Set up AI Enhanced Recommended Actions for Operational Technology Service Management \(OTSM\)

Set up AI Enhanced Recommended Actions for Operational Technology Service Management \(OTSM\) so that you can contextualize external sources related to an Operational Technology \(OT\) incident.

## Before you begin

Ensure you have Recommended Actions for OTSM installed and configured. For more information, see [Set up Recommended Actions for OTSM](../../operational-technology-recommended-actions/task/set-up-recommended-actions-for-otsm.md).

Role required: admin

## Procedure

1.  [Create a Microsoft SharePoint Online external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-mspo&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

2.  [Configure crawl settings for a Microsoft SharePoint Online external content connector](https://www.servicenow.com/docs/access?context=configure-crawl-settings-spo-ext-cont-connector&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

3.  Set up the search source.

    1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.
    2.  Find and select the **\[RA-OTSM AI\] Search Profile** record
    3.  In the search profile record, select the **Search Sources** tab.
    4.  Select **Create and link**.
    5.  In the **Indexed source** field, select **SharePoint Online**.

        For more information about the additional form fields, see [Search Source form](https://www.servicenow.com/docs/access?context=search-source-form-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

    6.  Select **Submit**.
4.  If needed, add or remove the OT incident record fields that are later used to produce search results.

    **Note:** If you edit the fields later, the search process restarts so you can view the updated search results.

    1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Context**.
    2.  Select the **OT incident context** record.
    3.  In the context record, select the **Rules** tab.
    4.  Select the **OT incident being active** rule.
    5.  In the rule record next to **Fields affecting this rule**, select the **Unlock fields affecting this rule** ![](../image/unlock-affecting-fields.png) icon.
    6.  Using the Add item and Remove item icons, add or remove fields as needed.
    7.  Select **Save**.

## What to do next

After you set up AI Enhanced Recommended Actions for OTSM, you can use the feature in the Industrial Workspace. For more information see, [Contextualize an external document](use-ai-enhanced-ra-otsm.md).

**Parent Topic:**[Configure AI Enhanced Recommended Actions for Operational Technology Service Management \(OTSM\)](../concept/configure-ai-enhanced-ra-otsm.md)

