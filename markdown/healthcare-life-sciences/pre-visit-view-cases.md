---
title: View a procedure request case in Workspace
description: View a procedure request case in Workspace to complete patient pre-visit activities for a procedure.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage procedure requests, Pre-Visit Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# View a procedure request case in Workspace

View a procedure request case in Workspace to complete patient pre-visit activities for a procedure.

## Before you begin

**Important:**

Starting with the Yokohama release, Pre-Visit Management is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

You must have access to procedure request cases.

Role required: sn\_hcls.manager or sn\_previsit.patient\_service\_agent

## Procedure

1.  Open your Workspace by navigating to **All** &gt; **Pre-Visit Management** &gt; **Workspace**.

2.  View procedure request cases assigned to you or your groups.

    -   View procedure request cases assigned to you by navigating to **Lists** &gt; **Procedure request** &gt; **My Cases**.
    -   View all open procedure request cases assigned to you by navigating to **Lists** &gt; **Procedure request** &gt; **My Open**.
    -   View procedure request cases that belong to your groups but have not been assigned to anyone by navigating to **Lists** &gt; **Procedure request** &gt; **Unassigned for my groups**.
    -   View all procedure request cases by navigating to **Lists** &gt; **Procedure request** &gt; **All**.
3.  Click the link to the case you want to view.


## Result

The selected procedure request case page opens in another tab within Workspace displaying the following components:

-   Playbook
-   Details
-   Patient information
-   Tasks
-   Appointments
-   Pre-authorization requests
-   Emails
-   Task SLAs

A procedure request case is based on a healthcare case that instead is based on a customer service case. Depending on the configurations made by your administrator and your role, additional tabs similar to a customer service case might appear for the procedure request case.

**Note:** The **Patient** field is mandatory for a procedure request case.

For more information on tabs available for a customer service case, see [Customer service case form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/r_CustomerServiceCaseForm.md).

## What to do next

You can select the **Patient information** tab in Workspace to view patient details. For more information, see [Viewing patient information for a procedure request in Workspace](../concept/pre-visit-viewing-patient-info.md).

