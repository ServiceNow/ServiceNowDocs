---
title: Restore Recommended Actions on record page variants after upgrade
description: After upgrading to a newer release, Recommended Actions \(RA\) may no longer appear on certain record page variants \(CSM default record page or CSM Interaction record page\), even if it was visible before. This can occur if the RA page is inactive or if the record page uses a customized variant created before RA was introduced as a static tab. Use the following procedure if the RA page exists but is not active for the record page variant.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Restore Recommended Actions on record page variants after upgrade

After upgrading to a newer release, Recommended Actions \(RA\) may no longer appear on certain record page variants \(CSM default record page or CSM Interaction record page\), even if it was visible before. This can occur if the RA page is inactive or if the record page uses a customized variant created before RA was introduced as a static tab. Use the following procedure if the RA page exists but is not active for the record page variant.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  On the Experiences tab, select **CSM/FSM Configurable Workspace**.

3.  On the CSM/FSM Configurable Workspace page, scroll to the Records section and select one of the supported record pages:

    -   CSM default record page
    -   CSM Interaction record page
4.  In the content tree on the left, select **Tab Sidebar**.

5.  In the right panel, locate the Page Collection for the CSM default record mid-tabs and select the **Sub-pages &amp; pages** icon ![](../image/ra-page-collection-subpages-pages-icon.png) beside it.

6.  In the Page collection controller dialog, select the **Lookup window** icon ![](../image/ra-page-collection-lookup-window-icon.png)beside the Recommended Actions default option.

7.  On the Page Collection window, select **Settings** at the top.

8.  On the Variant: Recommended Actions for CSM Default Record Page, under Availability, enable the **Active** check box.

    **Note:** If RA still does not appear after completing this procedure, the record page variant may have been created before RA was introduced as a static tab. Static tab added in newer releases are not automatically included in existing customized variants during an upgrade. In this case, manually add RA as a static tab to the affected variant.


