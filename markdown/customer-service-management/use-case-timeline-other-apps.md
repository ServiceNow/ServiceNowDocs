---
title: Use the case timeline with other applications
description: You can use the Customer Service case timeline with other ServiceNow applications by creating a configuration for each application and adding the ResolutionShaper field to the desired form.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Case timeline, Case form, Customer Service forms, Customer Service Management reference, Customer Service Management]
---

# Use the case timeline with other applications

You can use the Customer Service case timeline with other ServiceNow applications by creating a configuration for each application and adding the **ResolutionShaper** field to the desired form.

## Before you begin

Role required: admin

## Procedure

1.  Ensure that the Customer Service plugin \(com.sn\_customerservice\) has been activated.

2.  Navigate to the Resolution Shaper Configs page \(`<instance>sys_resolutionshaper_config_list.do`\) and click **New**.

3.  Select a table in the **Task Table** field.

4.  Add the desired states in the **Requestor States** field using a comma-separated list.

    For example, `New,Active,Resolved,Closed`.

5.  Make any necessary changes to the remaining fields and click **Submit**.

6.  Navigate to the desired form.

7.  Right-click the form header and select **Configure** &gt; **Form Layout**.

8.  Using the slushbucket, select **ResolutionShaper** and move it to where you want the timeline to appear.

9.  Click **Save**.


