---
title: Use Location Filter in MFA Context
description: Use the location filter criteria created in MFA Context.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Tutorial: Use Location Filter criteria, Location Filter, Filter criteria, Adaptive authentication, Authentication, Access Management]
---

# Use Location Filter in MFA Context

Use the location filter criteria created in MFA Context.

## Before you begin

Role required: admin

Plugin required: **Zero Trust - Location Based Access** \(`com.snc.zero_trust_location_access`\).

The following procedure describes on how to create a Location Filter with the countries that you want to configure MFA as a second factor for authentication to the users based on the location.

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Auth Policy Context** &gt; **MFA Context**.

2.  Select the **Step-Up MFA Policy** information icon and then select **Open Record** to open the **MFA Context**.

3.  On the Step-Up MFA Policy page, under the Policy Inputs tab, select **New**.

4.  Add the Location Filter input and **Submit**.

    For example, you want to display MFA for users logging in to the instance outside Australia.

    ![Location Filter for MFA](../images/location-based-mfa.png)

5.  On the Step-Up MFA Policy page, select the Policy Conditions tab and select **New**.

6.  In the Conditions page, provide the label, conditions, and set it to true.

    ![Condition for MFA](../images/conditions-mfa.png)

7.  Select **Submit**.

8.  On the Step-Up MFA Policy page, activate the MFA Policy if it’s **Deactivated**.

9.  Select **Update** to update the configuration.

    The users outside the configured country \(Australia\) selecting the instance link, specifying their credential; will be shown with the MFA screen to provide the second factor credentials to log in to the instance.


