---
title: Map a missing custom application to a product subscription in Subscription Management
description: Map a custom application to a product subscription when that application isn't shown in the Unmapped custom applications tab of Subscription Management. To stay in compliance, you must map custom tables that belong to a custom application to a product subscription.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-03-11"
reading_time_minutes: 2
breadcrumb: [Managing custom tables and apps, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Map a missing custom application to a product subscription in Subscription Management

Map a custom application to a product subscription when that application isn't shown in the **Unmapped custom applications** tab of **Subscription Management**. To stay in compliance, you must map custom tables that belong to a custom application to a product subscription.

## Before you begin

Role required: usage\_admin, sn\_sub\_man.admin, or admin

## About this task

Subscription Management can't display product subscription recommendations for some unmapped custom applications, and those applications aren't shown in the **Unmapped custom applications** tab. As a result, you might see fewer applications in the **Unmapped custom applications** tab than the number shown on the Unmapped Custom Applications report in the Subscription Management Overview page. You can map any missing custom applications to product subscriptions from the Custom Application list.

## Procedure

1.  Navigate to the **Issues** tab in Subscription Management in one of the following ways.

    -   Navigate to **Admin** &gt; **Subscription Management** &gt; **Issues**.
    -   Navigate to **All** &gt; **Subscription Management** &gt; **Issues**.
2.  Select the **Unmapped custom applications** tab.

3.  Select **Map missing applications from the custom application list**.

4.  Select the personalize list icon \(![Personalize list icon](../../../common/image/List_PersonalizeListIcon.png)\).

    ![The personalize list icon can be found next to the New button.](../image/sm-personalized-list-missing-custom-apps.png)

5.  Adjust the columns shown on the Custom Application list by moving **Subscription\(subscription\_entitlement\)** from the **Available** column to the **Selected** column.

6.  Select **OK**.

    In the **Subscription** column, you can see which product subscriptions each of your custom applications are mapped to.

7.  Select an unmapped custom application.

    You can identify unmapped custom applications using the **Subscription** column. The **Subscription** column for unmapped custom applications is empty.

8.  On the header of the Custom Application form, select the form title.

9.  Change the view by selecting **Subscription**.

10. In the **Subscription** lookup list on the Custom Application form, select a product subscription.

    The lookup list doesn't include expired, grandfathered, or Store application subscriptions. If you have a Store application with custom tables that must be mapped to a subscription, select a subscription with a custom table entitlement.

11. Select **Update**.


## Result

One or more custom applications are mapped to a product subscription and your custom table entitlement count is updated. Updates made through the Custom Application form show in Subscription Management the next day.

**Parent Topic:**[Managing custom tables and applications in Subscription Management](../concept/allocating-custom-tables-subscr-apps-v2.md)

