---
title: Configure Financial Services Operations Integration with Jack Henry jXchange
description: Configure the Financial Services Operations Integration with Jack Henry jXchange application by using the Jack Henry jXchange connection and credential record to authenticate ServiceNow requests.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Jack Henry jXchange, Integrate, Financial Services Operations \(FSO\)]
---

# Configure Financial Services Operations Integration with Jack Henry jXchange

Configure the Financial Services Operations Integration with Jack Henry jXchange application by using the Jack Henry jXchange connection and credential record to authenticate ServiceNow requests.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  To customize the connection configuration, access the connection settings in **Flow Designer** &gt; **Connections** and select **JHA**.

    For more information on how to update the connection configuration, see [Set up Jack Henry jXchange Spoke](https://www.servicenow.com/docs/access?context=jha-spk-setup&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

3.  To update other attributes, navigate to **Integration Hub** &gt; **Connection &amp; Credential Aliases** and edit the required information.

4.  Navigate to **Flow Designer** &gt; **Designer** &gt; **Actions** tab and select the **Look up Financial Accounts Stream** action that you want to test.

5.  Click **Test**.

    The system displays the Test Action dialog box.

6.  Fill in the fields for the action.

    **Note:** Complete all required fields in the Test Action dialog box.

7.  Click **Run Test**.

    **Note:** Select the **Run test in background** option to test an action asynchronously in the background.

    If you select the **Run test in background** option, the execution details are displayed only after the execution is completed asynchronously in the background.


## What to do next

To view the action execution details, click **Your test has finished running. View the Action execution details.**

**Parent Topic:**[Financial Services Operations Integration with Jack Henry jXchange](../concept/fso-integration-with-jha-integthub-landing-page.md)

