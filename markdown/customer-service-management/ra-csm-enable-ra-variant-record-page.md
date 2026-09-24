---
title: Recommended Actions tab not appearing on the CSM default record page
description: The Recommended Actions \(RA\) tab may not appear in the contextual side panel of the CSM default record page or the CSM Interaction record page. The cause determines the resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/ra-csm-enable-ra-variant-record-page.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [restore Recommended Actions on record page variants after upgrade, Recommended Actions tab not appearing, RA tab missing, record page variant inactive, extended case table]
breadcrumb: [Set up CRM Workspace, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Recommended Actions tab not appearing on the CSM default record page

The Recommended Actions \(RA\) tab may not appear in the contextual side panel of the CSM default record page or the CSM Interaction record page. The cause determines the resolution.

## Before you begin

Role required: admin

## About this task

The Recommended Actions tab may not appear in the contextual side panel for one of the following reasons:

-   **The Recommended Actions page variant is inactive.** The record page may use a customized variant created before RA was introduced as a static tab. This can occur after an upgrade, even if RA was visible before.
-   **The record is from a table that extends the Case table.** The Hide tab condition on the RA tab in the Tab sidebar component matches the base system Case \[sn\_customerservice\_case\] table name exactly, so the condition evaluates as true and the tab is hidden. Contexts, rules, and recommendations can still be created for any table. Only the visibility of the RA tab on the CSM default record page is affected.

The following procedure applies only when the Recommended Actions page variant is inactive.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  On the Experiences tab, select CRM Workspace.

3.  On the CRM Workspace page, scroll to the Records section and select one of the supported record pages:

    -   CSM default record page
    -   CSM Interaction record page
4.  In the content tree on the left, select **Tab Sidebar**.

5.  In the right panel, locate the Page Collection for the CSM default record mid-tabs and select the **Sub-pages &amp; pages** icon \[Omitted image "ra-page-collection-subpages-pages-icon.png"\] Alt text: beside it.

6.  In the Page collection controller dialog, select the **Lookup window** icon \[Omitted image "ra-page-collection-lookup-window-icon.png"\] Alt text:beside the Recommended Actions default option.

7.  On the Page Collection window, select **Settings** at the top.

8.  On the Variant: Recommended Actions for CSM Default Record Page, under Availability, enable the **Active** check box.

    **Note:** If RA still does not appear after completing this procedure, the record page variant may have been created before RA was introduced as a static tab. Static tabs added in newer releases aren't automatically included in existing customized variants during an upgrade. In this case, manually add RA as a static tab to the affected variant.


