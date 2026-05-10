---
title: Set up AI Enhanced recommended actions for Industrial Connected Workforce
description: Set up AI Enhanced recommended actions for ICW so that you can contextualize external sources related to a deviation.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, AI Enhanced recommended actions for ICW, Industrial Connected Workforce]
---

# Set up AI Enhanced recommended actions for Industrial Connected Workforce

Set up AI Enhanced recommended actions for ICW so that you can contextualize external sources related to a deviation.

## Before you begin

You must have Recommended Actions for ICW installed and configured. For more information, see [Recommended Actions for the Industrial Connected Workforce](../../icw-industrial-connected-workforce/concept/recommended-actions-icw.md).

Role required: admin

## Procedure

1.  [Create a Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/create-ext-cont-connector-mspo.md).

2.  [Configure crawl settings for a Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configure-crawl-settings-spo-ext-cont-connector.md).

3.  Set up the search source.

    1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.
    2.  Find and select the **\[RA-ICW AI\] Search Profile** record
    3.  In the search profile record, select the **Search Sources** tab.
    4.  Select **Create and link**.
    5.  In the **Indexed source** field, select **SharePoint Online**.

        For more information about the additional form fields, see [Search Source form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/search-source-form-ais.md).

    6.  Select **Submit**.
4.  If needed, add or remove the deviation record fields that are later used to produce search results.

    **Note:** If you edit the fields later, the search process restarts so you can view the updated search results.

    1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Context**.
    2.  Select the **Deviation context** record.
    3.  In the context record, select the **Rules** tab.
    4.  Select the **Deviation being active** rule.
    5.  In the rule record next to **Fields affecting this rule**, select the **Unlock fields affecting this rule** ![](../image/unlock-affecting-fields.png) icon.
    6.  Using the Add item and Remove item icons, add or remove fields as needed.
    7.  Select **Save**.
    **Important:** Removing the predefined fields might impact the output of the contextualized document and the generated action plan.


## What to do next

After you set up AI Enhanced recommended actions for ICW, you can use the feature in the Digital Factory Workspace. For more information see, [Contextualize an external document for a Deviation in the Digital Factory Workspace](use-ai-enhanced-ra-icw.md).

**Parent Topic:**[Configure AI Enhanced recommended actions for Industrial Connected Workforce](../concept/configure-ai-enhanced-ra-icw.md)

