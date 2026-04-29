---
title: Configure flows
description: Review the flows that are available with Financial Services Operations applications to see if these flows meet your business needs. You might need to customize these flows or design new ones as needed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Financial Services Operations \(FSO\)]
---

# Configure flows

Review the flows that are available with Financial Services Operations applications to see if these flows meet your business needs. You might need to customize these flows or design new ones as needed.

## Before you begin

Ensure that the scope is selected for the application for which you are configuring a flow. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

Role required: Based on the application that you are configuring, you need the following roles:

-   Financial Services Business Deposit Operations: sn\_bom\_deposit\_b2b.admin and admin
-   Financial Services Business Loan Operations: sn\_bom\_loan\_b2b.admin and admin
-   Financial Services Card Operations: sn\_bom\_card.admin and admin
-   Financial Services Complaint Management: sn\_bom\_compl.admin and admin
-   Financial Services Payment Operations: sn\_bom\_payment.admin and admin
-   Financial Services Personal Deposit Operations: sn\_bom\_deposit\_b2c.admin and admin
-   Financial Services Personal Loan Operations: sn\_bom\_loan.b2c\_admin and admin
-   Financial Services Treasury Operations: sn\_bom\_treasury.admin and admin
-   Individual Life Claims: sn\_ins\_claim\_indl.admin and admin
-   Insurance claims: sn\_ins\_gen\_claim.admin and admin

## About this task

The flows are built using ServiceNow Workflow Studio, so make sure you’re familiar with [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=australia&pubname=australia-application-development&ft:locale=en-US) basics.

For information on flows that are installed with Financial Services Operations applications, see [Designer flows for Financial Services Operations applications](../reference/flow-designer-flows-fso-apps.md).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Create a new flow or modify an existing one.

    -   To create a flow, click **New**.
    -   To modify a predefined flow, filter the list to show the flows for the required application and open the desired flow.
    For information on how to create or modify flows, see [Create a flow](https://www.servicenow.com/docs/access?context=create-flow&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

3.  Click **Save**.

4.  Test your flow and click **Activate**.

    For more information, see [Test a flow](https://www.servicenow.com/docs/access?context=flow-test&version=australia&pubname=australia-build-workflows&ft:locale=en-US).


