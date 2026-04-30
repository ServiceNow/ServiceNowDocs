---
title: Configure a personalized greeting
description: Configure the greeting that your users see when they log in to the Now Mobile app. For example, you can add a hello message that includes the user's first and last name.
locale: en-US
release: yokohama
product: Now Mobile - Employee Experience
classification: now-mobile-employee-experience
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Now Mobile app, Unified Employee Experience, Employee Service Management]
---

# Configure a personalized greeting

Configure the greeting that your users see when they log in to the Now Mobile app. For example, you can add a hello message that includes the user's first and last name.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Mobile App** &gt; **Applet Launchers**.

2.  In the Applet Launchers \[sys\_sg\_applet\_launcher\] table, open the Homepage record.

3.  Add the **Header Titles** field to the form.

4.  In the **Header Titles** field, open the record.

5.  Update the **Text** field as required.

    This text displays in the Now Mobile app heading.

    This field uses the `{{sys_id}}` syntax to reference a variable for the first and last name of the currently logged-in user. Changing the variable is not supported.

6.  Click **Submit**.


## Result

When a user logs in to the Now Mobile app, they see your personalized greeting.

