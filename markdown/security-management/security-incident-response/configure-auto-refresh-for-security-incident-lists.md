---
title: Configure auto refresh interval for security incident lists
description: Configure the refresh interval for security incident lists for automatic update of the security incident list ensuring an updated list for the security analysts.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View and update Security Incident Response system properties, Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure auto refresh interval for security incident lists

Configure the refresh interval for security incident lists for automatic update of the security incident list ensuring an updated list for the security analysts.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Security Incident Response Workspaces** &gt; **Administration**.

2.  Select **SIR Workspace Properties**.

3.  On the SIR Workspace Properties page, select **sn\_si\_aw.security\_incidents\_list.refresh\_interval**.

4.  On the sn\_si\_aw.security\_incidents\_list.refresh\_interval page, update the **Value** field.

    **Note:** The auto refresh interval is in minutes. The default refresh rate is five minutes. To disable the auto refresh, set the value to 0.

5.  Select **Save** to save the updated refresh interval.


**Parent Topic:**[View and update Security Incident Response system properties](../concept/view-update-sirw-system-properties.md)

