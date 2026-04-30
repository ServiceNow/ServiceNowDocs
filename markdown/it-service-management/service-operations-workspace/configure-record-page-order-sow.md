---
title: Modify the Record Page in the Service Operations Workspace using the Standard Record Page
description: Configure the order number and screen conditions of a record page using the Standard Record Page \(SRP\) in the Service Operations Workspace.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Standard Record Page in Service Operations Workspace, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Modify the Record Page in the Service Operations Workspace using the Standard Record Page

Configure the order number and screen conditions of a record page using the Standard Record Page \(SRP\) in the Service Operations Workspace.

## Before you begin

Role required: admin

## About this task

Every record page contains an order number, which can be active or inactive. A default record page must be active and have the lowest order number. Service Operations Workspace displays the record with the lowest active order number as the default record page.

SRP also provides ways to add screen condition mappings when a page appears.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Under the Experiences list, select **Service Operations Workspace**.

3.  Under the **Pages and Variants** section, under **Record**, select **SRP Record**.

    **Note:** If you are on a version prior to 4.0, you can navigate from **Record SNC** in **UI Builder** to modify a record page.

4.  Under **Contents**, in the **Body** level, select **Main Tab**.

    ![Main Tab option in SRP record](../image/SRP_Main_tab_SOW_edit.png "Main tab")

5.  If the new copy is in a different application scope, select **Edit in original scope** before editing.

    ![Edit in original scope](../image/edit_in_original_scope.png)

6.  From the right of the page, navigate to **Config** &gt; **Tabs**.

    SRP record has four types of tabs for customization.

    -   Page Collection: Contains the pages and variants associated with the record page.
    -   Inline tabs: Inline tabs and the Page collection tab contain the code related to a page.
    -   Related List: Contains the details of the records associated with the record. The related list is a static tab, and you can’t modify the order of this tab.
    -   Repeater tabs: Contains the details of the tabs that recur throughout the page. The repeater tab is a static tab, and you can’t modify the order of this tab.
    These tabs help in changing of the page layout. For example, if you want to add a tab that appears before the **Details** tab, you can change the **SOW - Record tabs left**. Similarly, to add a tab after the **Details** tab, you can modify the **SOW - Record tabs middle**.

7.  To modify and view the pages and variants inside each tab, select the ![Edit content icon](../image/SRP_Edit_overviewpage_left_icon.png).

8.  Under the Pages and Variants list, select the required page.

    For example, inside the Page collection tab, select Incident Overview SNC.

    **Note:** The data, events, and mappings in the **Config** and **Events** tabs can’t be modified.

9.  From the top of the page, select the ![Menu icon](../../../reuse/icons/product-icons/menu-outline-24.svg) open menu icon.

10. To modify the order of the record, perform the following steps.

    1.  Select the **Settings** tab ![Editor and Settings](../image/editor-settings.png).

    2.  To modify the display order of the record, edit the **Order** value.

        The variant with the lowest order is considered the default configuration.

11. To modify the variant ordering, perform the following steps.

    1.  Navigate to **Developer** &gt; **Open variant collection record**.

    2.  Under the UX Screens list, modify the **Order** field.

        The default variant has the lowest order value.

    3.  Select **Update**.

12. To modify the **Screen Conditions** of the record page, perform the following steps.

    1.  Navigate to **Developer** &gt; **Open variant record**.

        The conditions of the screen appear in the **Screen Condition** field.

    2.  To modify or add a new UX Screen condition, navigate to the UX Screens conditions list.

    3.  Select the screen condition.

    4.  Enable the **Scripted Condition** field.

    5.  Modify the **Script** and **Parameter Mapping** fields to set the screen conditions according to your requirements.

    6.  Select **Update**.


**Parent Topic:**[Configure Standard Record Page in Service Operations Workspace](../concept/srp-service-operations-workspace.md)

