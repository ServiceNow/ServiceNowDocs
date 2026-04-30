---
title: Optimize page loading performance \(Advanced Feature\)
description: Performance settings enhances leading speeds and user engagement by displaying high-priority content first, making key components interactive sooner for a faster perceived performance.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure components and repeaters \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Optimize page loading performance \(Advanced Feature\)

Performance settings enhances leading speeds and user engagement by displaying high-priority content first, making key components interactive sooner for a faster perceived performance.

## Before you begin

Role required: ui\_builder\_admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Create or open a page.

4.  Add a component to your page.

    You need a component on your page before you can adjust performance settings.

5.  Select the menu icon.

6.  Select **Manage performance settings**.

    The **Advanced performance settings** modal opens.

    ![Advanced performance settings modal showing the loading options.](../image/performance-settings-modal.png)

7.  Select how components load onto a page.

    |Choice|Description|
    |------|-----------|
    |**Progressive loading**|Enable quicker page access while components continue to load.|
    |**Full page loading**|Ensure a seamless experience by loading all content before you access the page. Enter the maximum time you want to wait before displaying content in the **Page loader threshold duration** field.|

8.  Select the priority in which components load on a page.

    1.  Select the **Priority** tab.

    2.  Select the component you want to give priorty to.

    3.  Check **Make high priority**.

9.  Select which data to cache when a page loads.

    1.  Select the **Cache and headers** tab.

    2.  Select a data resource from the list.

    3.  Check **Activate data policy**.

10. Select **Apply**.


**Parent Topic:**[Configure components and repeaters \(advanced feature\)](../concept/configure-comp-and-repeaters.md)

