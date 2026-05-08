---
title: Configure AI Search for mobile devices
description: Configure the Now Mobile search bar to use the AI Search search engine.
locale: en-US
release: australia
product: Now Mobile - Employee Experience
classification: now-mobile-employee-experience
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [AI Search in mobile, Configuring Now Mobile, Unified Employee Experience, Employee Service Management]
---

# Configure AI Search for mobile devices

Configure the Now Mobile search bar to use the AI Search search engine.

## Before you begin

To enable the AI Search capability to search for people and customers, ensure that you have the Employee Center Pro plugin \[com.snc.employee\_center\_pro\] installed. For more information, see [Install Employee Center Pro](../../../product/employee-center/task/install-ec-pro.md). You must purchase a subscription before activating the plugin. For more details, see ServiceNow plugins.

Make sure you are working in a scoped application where you can add new item configurations.

Role required: admin

## Procedure

1.  Change the search engine from Zing to AI Search and select the relevant profile.

    1.  In the web-based UI, enter `sys_sg_global_search.list` in the filter navigator, to open a list of global search configurations.

    2.  Select the record **Homepage Search - Catalog, Knowledge, People**.

    3.  Select **click here** at the top of the page to edit the record.

    4.  Select the reference lookup icon \(![Information icon.](../../tablet-mobile-ui/image/gac-info-icon.png)\) in the **Search Application Configuration** field, and select **Open Record** to open the Search Context Configuration form.

    5.  Select AI Search in the **Search Engine** field.

    6.  Select the information icon \(![Information icon.](../../tablet-mobile-ui/image/gac-info-icon.png)\) in the **Search Profile** field and select the NowMobile Default Search profile.

    7.  Select **Yes** in the confirmation message.

    8.  Select the form header \(![Form header icon.](../../tablet-mobile-ui/image/context-menu-icon.png)\) and select **Save**.

2.  Remove the item configuration, Catalog Item Main item.

    1.  In the web-based UI, enter `sys_sg_global_search.list` in the filter navigator to reopen the list of global search configurations.

    2.  Select the record **Homepage Search - Catalog, Knowledge, People**.

    3.  In the **Catalog Item Main Item** row, right-click the information icon \(![Information icon.](../../tablet-mobile-ui/image/gac-info-icon.png)\) and select **Open Link in New Tab**.

    4.  Select **Delete** in the top-right of the page and select **Delete** in the subsequent confirmation message.

3.  In the Global Search M2M Item Configurations related list, add the new catalog item to be the main item.

    1.  Select **New**.

    2.  Select the reference lookup icon \(![Reference lookup icon.](../../tablet-mobile-ui/image/reference-lookup-icon.png)\) in the **Item Configuration** field.

    3.  In the Item Configuration form search bar, search for `Catalog Item Search Result Main Item` and then select the entry

    4.  Select **Submit**.

4.  In the Global Search M2M Item Configurations related list, remove the two existing knowledge item configuration records.

    1.  Select the **Knowledge article search main item** row and the **Knowledge article search main item \(viewcount1\)** row.

    2.  Select **Actions on selected rows**, and then select **Delete**.

    3.  Select **Delete** in the subsequent confirmation message.

5.  In the Global Search M2M Item Configurations related list, add the new knowledge item as the main item.

    1.  Select **New**.

    2.  Select the reference lookup icon \(![Reference lookup icon.](../../tablet-mobile-ui/image/reference-lookup-icon.png)\) in the **Item Configuration** field.

    3.  In the Item Configuration form search bar, search for `Knowledge AIS Search Main Item` and then select the entry.

    4.  Select **Submit**.

6.  Activate the view configuration for the people-based records.

    1.  In the web-based UI, enter `sys_sg_master_item.list` in the filter navigator, to open a list of item configurations.

    2.  In the Name search bar, search for `People Search Main Item`.

    3.  Select the information icon \(![Information icon.](../../tablet-mobile-ui/image/gac-info-icon.png)\) next to People Search Main Item and select Open Record.

    4.  In the Item Configuration form, select **Use card**.

    5.  Select the menu icon \(![Form context menu icon.](../../tablet-mobile-ui/image/context-menu-icon.png)\) and select **Save**.


## Result

The Global Search Configuration page should contain the items shown in the following figure.

![Global search item configuration page with all listed items after successful configuration.](../../tablet-mobile-ui/image/ais-search-final-config-screen.jpg)

**Parent Topic:**[AI Search in mobile](../concept/text-search-advanced-now.md)

