---
title: Create a client state parameter for Work scheduler
description: Add custom client state parameter values to add properties to the card components.
locale: en-US
release: xanadu
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a Work scheduler card using the Next Experience UI Builder, Setting up Work scheduler in Workforce Optimization for Customer Service, Configuring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Create a client state parameter for Work scheduler

Add custom client state parameter values to add properties to the card components.

## Before you begin

Role required: admin, workspace\_admin, or ui\_builder\_admin​

## Procedure

1.  Select the Client state icon \(![Client state icon](../image/client-state-icon.png)\).

2.  In the Client state parameters section, click **+Add**.

3.  Create the client state parameter.

    1.  In the **Name** field, enter **cardProps**.
    2.  From the **Type** menu, select **JSON**.
    3.  In the **Initial value** field, select **Edit**.
    4.  In the **Initial value** pop-up screen, enter the following code:

        ```
        {
            "tagline": {},
            "heading": {},
            "dropdowns": [],
            "content": [],
            "assignedTo": null,
            "aria": {}
          }
        ```

    5.  Select **Apply**.
    Here's a demo on how to create client state parameters.Create client state parameters


## What to do next

[Create page scripts for Work scheduler](https://www.servicenow.com/docs/access?context=work-sched-create-page-scripts&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)

**Parent Topic:**[Create a Work scheduler card using the Next Experience UI Builder](create-workscheduler-card-wfo-cs.md)

**Related topics**  


[Create and bind a client state parameter to a component](https://www.servicenow.com/docs/access?context=state-parameters&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

