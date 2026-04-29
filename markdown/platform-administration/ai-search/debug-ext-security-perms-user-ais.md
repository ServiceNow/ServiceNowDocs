---
title: Debug external content security filters for a ServiceNow AI Platform user
description: Use the Session Log to view the set of externally defined user and group access permission filters associated with the current ServiceNow AI Platform user. Administrators can use this approach to verify that the proper user mappings exist for the current user.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Debug external content security filters for a ServiceNow AI Platform user

Use the Session Log to view the set of externally defined user and group access permission filters associated with the current ServiceNow AI Platform user. Administrators can use this approach to verify that the proper user mappings exist for the current user.

## Before you begin

Role required: admin

## About this task

Enable session debugging for AI Search to view debug log messages for external content security. Each debug log message shows the external content security filter that AI Search applies to determine whether the current ServiceNow AI Platform user can see a search result for an external document.

## Procedure

1.  To enable session debugging for AI Search, navigate to **All** &gt; **System Diagnostics** &gt; **Session Debug** &gt; **Debug AI Search**.

2.  Navigate to **All** &gt; **System Diagnostics** &gt; **Session Debug** &gt; **Debug Log**.

    The Session Log opens.

3.  Use the [Search Preview UI for AI Search](../../../use/dashboards/application-content-packs/ai-search-preview.md#) to submit the external content search query of interest.

    **Note:** To debug external content security access permissions for another user, specify their name in the Search Preview UI's user impersonation tool.

4.  In the Session Log, filter for `AIS:External Content Security Filter` to see the external content security filters applied when evaluating access to an external document search result for the current \(or impersonated\) ServiceNow AI Platform user.

    ![Sample external content security filter message.](../image/debug-ext-cont-security-filter.png)


## What to do next

If the external content security filters don't include the desired external user or group access permissions, a search administrator can import an updated and corrected user mapping for the relevant ServiceNow AI Platform user. For more details on defining and importing user mappings, see [Mapping external users and groups to ServiceNow AI Platform users](../concept/user-mappings-ais.md#).

**Parent Topic:**[Administering AI Search](../concept/administer-ais.md)

