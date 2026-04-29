---
title: Set up AWS API configuration information in ServiceNow
description: The credentials provided by your AWS administrator are used in this procedure to create a suspension profile, enabling you to temporarily suspend or terminate AWS accounts as needed.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up AWS API configuration information in ServiceNow

The credentials provided by your AWS administrator are used in this procedure to create a suspension profile, enabling you to temporarily suspend or terminate AWS accounts as needed.

## Before you begin

The below procedure is only required if you're managing AWS accounts on Cloud Account Management.

Role required: ServiceNow AI Platform admin

## Procedure

1.  Log in to ServiceNow instance.

2.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

3.  Select **New**.

4.  In the **Name** field, enter the alias name.

    The format should be 'cloud org name-key' \(for example, org1-tfkey\).

5.  From the **Type** drop-down list, select **Credential**.

6.  Select **Submit**.

7.  Select the aliases name from the list that you entered earlier.

8.  Under the **Credentials** tab, select **New**.

9.  From the list, select **AWS Credentials** as your credential type.

10. In the **Name** field, enter the alias name.

11. In the **API Key** and **Secret Access Key** fields, enter the keys obtained from the admin.

12. Select **Submit**.


