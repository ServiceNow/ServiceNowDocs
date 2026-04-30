---
title: Customize ITOM Mobile Agent email recipients
description: Customize who receives emails about alerts to help reduce notification overload and efficiently delegate responsibilities.
locale: en-US
release: yokohama
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-03-26"
reading_time_minutes: 1
breadcrumb: [Configuring ITOM Mobile Agent, ITOM Mobile Agent, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Customize ITOM Mobile Agent email recipients

Customize who receives emails about alerts to help reduce notification overload and efficiently delegate responsibilities.

## Before you begin

Role required: srm\_admin or admin

## About this task

By default, ITOM Mobile Agent sends emails about alerts to everyone in a team's group email. You can customize the email recipients as follows:

-   Exclude managers from alert emails, reducing notification overload.
-   Include individual team members on alert emails, making sure that the right people stay informed.

## Procedure

1.  Navigate to **All** &gt; **Service Reliability Management** &gt; **Teams**.

2.  In the list, find the team that you want to customize.

3.  Choose one or more options to include or exclude certain recipients from email alerts.

    |Option|Instruction|
    |------|-----------|
    |**Exclude managers from alert emails**|In the **Exclude manager** column, set **false** to **true**.|
    |**Include individual team members on alert emails**|In the **Include members** column, set **false** to **true**.|

4.  Save your changes by selecting the check mark.

    Your updates appear in the **Teams** list, and ITOM Mobile Agent sends emails accordingly.


