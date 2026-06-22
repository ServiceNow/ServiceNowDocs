---
title: Create a client state parameter for Work scheduler
description: Add custom client state parameter values to add properties to the card components.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/work-sched-create-client-state-params-wfo-cs.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a Work scheduler card using the Next Experience UI Builder, Setting up Work scheduler, Optimize workforce operations, Extend capabilities, Configure, Customer Service Management]
---

# Create a client state parameter for Work scheduler

Add custom client state parameter values to add properties to the card components.

## Before you begin

Role required: admin, workspace\_admin, or ui\_builder\_admin​

## Procedure

1.  Select the Client state icon \(\[Omitted image "client-state-icon.png"\] Alt text: Client state icon\).

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
    Here's a demo on how to create client state parameters.


## What to do next

[Create page scripts for Work scheduler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/workforce-optimization-for-it-service-management/work-sched-create-page-scripts.md)

**Parent Topic:**[Create a Work scheduler card using the Next Experience UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/create-workscheduler-card-wfo-cs.md)

**Related topics**  


[Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/state-parameters.md)

