---
title: Create a basic auth profile using the Automated Test Framework
description: Create basic auth profiles to specify basic authentication credentials for Send Request - Inbound test steps.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administering REST test step configurations, Administer, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Create a basic auth profile using the Automated Test Framework

Create basic auth profiles to specify basic authentication credentials for Send Request - Inbound test steps.

## Before you begin

Role required: web\_service\_admin

## About this task

The user name and password must be valid credentials on the instance where the tests using the profile are run.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Tests**.

2.  Select a test that uses a Send Request - Inbound step.

3.  Select a Send Request - Inbound step.

4.  In the **Basic authentication** field, select the hour glass to look up the available profiles.

5.  On the **Basic Auth Configurations** form, select **New**.

6.  In the **Name** field, enter a name for the profile.

7.  In the **Username** field, enter a user name.

8.  In the **Password** field, enter a password.

9.  Click **Submit**.


**Parent Topic:**[Administering REST test step configurations](../concept/atf-administer-rest.md)

