---
title: Set the time zone for availability results in Service Portfolio Management
description: By default, the time zone to calculate availability for services and commitments is set to the global \(system\) time zone. You can change the global time zone or you can set the time zone for service commitments. With either option, you can recalculate the availability results based on the time zone that you set.
locale: en-US
release: yokohama
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Service Portfolio Management, Service Portfolio Management, IT Service Management]
---

# Set the time zone for availability results in Service Portfolio Management

By default, the time zone to calculate availability for services and commitments is set to the global \(system\) time zone. You can change the global time zone or you can set the time zone for service commitments. With either option, you can recalculate the availability results based on the time zone that you set.

## Before you begin

Role required: portfolio\_admin or admin

## About this task

The following system properties work in the background for you to set the time zone for availability results:

-   spm.availability.global.tz — The default time zone, also called the system time zone. This system property enables you to select a time zone from a list to calculate availability results for all commitments using this global time zone.
-   spm.availability.commitment.tz — When set to true \(or to Yes in the interface\), this system property enables you to calculate availability results using the time zone that you select for a commitment record.

To set the time zone, the availability system property \[com.snc.availability.v2\] must be set to true.

1.  In the Filter navigator, enter `sys_properties.list`.
2.  Enter `*avail` in the **System Properties Name** search field, and then press **Enter**.
3.  Verify that the availability system property \[com.snc.availability.v2\] is set to true.

    **Note:** If the availability system property isn’t set to true, then select the system property name, set the Value field to true, and then select **Update**. A banner might display with a link to edit the record.


## Procedure

1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Administration** &gt; **Availability calculation settings**.

    ![Availability calculation settings page.](../image/spm2-avail-tz.png "Availability calculation settings page")

2.  Decide how you want to calculate availability.

    -   **Calculate availability with commitment time zone** or
    -   **Set the global availability time zone**.
    Refer to the **Availability calculations settings page** image for the next steps.

3.  **Calculate availability with commitment time zone**.

    1.  On the **Availability calculations settings** page, select **Yes** to **Calculate availability with commitment time zone**, and then **Save**.

        **Note:** Notice that the global availability time zone can't be set.

    2.  In the Core UI tab, navigate to the list of service commitments.

        **Tip:** To see a list of service commitments, enter `service_commitment.list` in the Filter navigator, and then press **Enter**.

    3.  Open a service commitment that you want to change the time zone. In the **Time zone** field, use the down arrow to select a different time zone, and then select **Update**.
    4.  The **Time zone** column of the Service commitment table shows the time zone that you updated.
4.  **Set the global availability time zone**.

    1.  On the **Availability calculations settings** page, select **No** to **Calculate availability with commitment time zone**.
    2.  Use the down arrow to **Set the global availability time zone**, and then **Save**.
    3.  In the Core UI tab, navigate to the service availability list.

        **Tip:** To see the service availability list, enter `service_availability.list` in the Filter navigator, and then press **Enter**.

    4.  Select **Recalculate results**, and then select **Recalculate** on the **Confirmation** page.
    5.  Select **Refresh** \(![Refresh icon](../image/spm2-refresh-screen.png)\) on the service availability list to see the updated time zone in the **Time zone** column.

        **Note:** It takes a few minutes for all the records to recalculate and show the updated time zone field.

5.  Configure the available time zones.

    1.  On the **Availability calculations settings** page, select **Configure available time zones** to open it in another tab.
    2.  In the opened tab, select the time zone from the **Available** field and move it to the **Selected** field.

        **Note:** You can also add a time zone to the **Available** field. Enter a time zone in the **Enter new item** field, and then select **Add**.

    3.  Select **Save**.
    4.  To return to the **Availability calculation settings** page, select its tab.
6.  Select **Save**.


**Parent Topic:**[Using Service Portfolio Management](../concept/SPM2-using.md)

**Related topics**  


[View availability results in Service Portfolio Management](../concept/SPM2-view-availability-results.md)

