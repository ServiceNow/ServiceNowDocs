---
title: Create integration account
description: Create a dedicated account with the evt\_mgmt\_integration role for third-party monitoring systems to push events to ServiceNow.
locale: en-US
release: australia
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [integration account, Event Management, evt\_mgmt\_integration, third-party monitoring, ITOM, AIOps, user account, authentication]
breadcrumb: [ITOM Configuration console for Event Management, Now Assist for Setup \(AIOps\), Now Assist for Setup \(ITOM\), IT Operations Management]
---

# Create integration account

Create a dedicated account with the evt\_mgmt\_integration role for third-party monitoring systems to push events to ServiceNow.

## Before you begin

Verify that the ITOM AIOps and Now Assist for IT Operations Management plugins are installed.

Ensure you're in the Configure IT Operations Management page.

Role required: admin

## About this task

A dedicated integration account ensures third-party monitoring systems have secure, stable, and appropriately scoped access to push events into ServiceNow without relying on personal user accounts.

**Note:** Create an integration account user only if you plan to use basic authentication. This step is not required if you're using API keys or OAuth. If you prefer those methods, refer to the corresponding documentation for setup instructions.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Event Management** &gt; **Platform foundations**.

2.  Expand **Platform foundations**.

3.  Select **Integration account**.

4.  Select **Create account**.

    The Create integration account page opens.

5.  In the **User ID** field, enter the account id or the name of the account.

6.  In the **Password** field, enter the password for the integration account.

7.  Select **Create account**.

    The integration account is created.

8.  To complete the setup, select **Mark as configured**.


