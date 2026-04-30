---
title: Configure jobs for email notifications dashboard
description: Configure data collection jobs for the email notification dashboard.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Email notifications dashboard, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure jobs for email notifications dashboard

Configure data collection jobs for the email notification dashboard.

## Before you begin

Data collection is triggered by configuring and executing jobs, except **Run as** field all other fields are preconfigured.

Role required: admin or notification\_dashboard\_admin

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **Indicators** &gt; **Automated Indicators**.

2.  From Indicators, search for **Email Notifications Sent**.

3.  Select and open **Email Notifications Sent**.

4.  Scroll down and select the **Jobs** tab.

5.  Select and open **Daily job to fetch Email Indicator Data and Email Notifications created**.

    1.  From the **Run as** field, select the user that has the access to run this job.

    2.  Select and hold \(or right-click\) the form header and select **Save**.

    3.  Select **Execute Now**

6.  Go back to the **Jobs** tab.

7.  Select and open **Job to fetch Historical Email Indicator Data**.

    1.  From the **Run as** field, select the user that has the access to run this job.

    2.  Select and hold \(or right-click\) the form header and select **Save**.

    3.  Select **Execute Now**

8.  Go back to Indicators, search and select **Email Notifications Created**.

9.  Scroll down and select the **Jobs** tab.

10. Select and open **temporary job for collecting Email Notifications Created**.

    1.  From the **Run as** field, select the user that has the access to run this job.

    2.  Select and hold \(or right-click\) the form header and select **Save**.

    3.  Select **Execute Now**

    Once the jobs are completed and the data is collected, the data is visible in the email notifications dashboard.


**Parent Topic:**[Email notifications dashboard](../concept/email-notifications-dashboard.md)

