---
title: Configure Walk-up Experience locations for guest users
description: Configure walk-up locations for guest-users so they can select a location while making appointments.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Walk-up Experience for Customer Service Management, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Configure Walk-up Experience locations for guest users

Configure walk-up locations for guest-users so they can select a location while making appointments.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **CSM Walk-up Experience** &gt; **Administration** &gt; **Appointment Configurations**.

2.  Select a location that the guest user needs access to.

3.  Click the Preview this record icon \( ![Preview this record icon.](../image/preview-record.png)\) next to the **Catalog item** field.

4.  In the Record Producer window, click **Open Record**.

5.  Under Related Links, click the Available For tab.

6.  Click **Edit**.

7.  Move **Any Guest User** from the **Collection** list to the **Available For** list and click **Save**.

8.  Under **Related Links**, click the Variable Sets tab.

9.  Select **sn\_appointment\_variable\_set** and set permissions for each of its variables.

    1.  In the notice at the top of the form about the current application, click **here** to access the CSM Walkup Experience application record.

    2.  Select the **sn\_appointment** variable.

    3.  Click the Permission tab.

    4.  For the **Read roles** and **Write roles**, move the public, snc\_internal, and snc\_external roles from the **Available** list to the **Selected** list.

        **Note:** **Create roles** is also required for the correct auto-population of the information in the guest records.

    5.  Click **Done**.

    6.  Repeat these actions for the **sn\_appointment\_macro** variable.

10. Repeat step 9 to set permissions for the **sn\_walkup\_variable\_set** variable set.


## Result

The configured walk-up locations are now available for guest users.

