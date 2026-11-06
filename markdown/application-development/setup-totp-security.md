---
title: Set up TOTP authorization for sensitive actions
description: Set up TOTP authorization to add another layer of security check before performing any sensitive action, such as changing records, deleting files, or sending messages on your behalf.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/setup-totp-security.html
release: australia
topic_type: task
last_updated: "2026-09-27"
reading_time_minutes: 1
keywords: [TOTP, authenticator app, security, action approvals]
breadcrumb: [Use, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Set up TOTP authorization for sensitive actions

Set up TOTP authorization to add another layer of security check before performing any sensitive action, such as changing records, deleting files, or sending messages on your behalf.

## Before you begin

Install and set up an authenticator app on your mobile device.

Role required: sn\_app\_arc.user

## Procedure

1.  Navigate to **Settings** &gt; **Security**.

2.  Under **TOTP Authorization**, select **Set Up TOTP**.

    A QR code and a secret code appear.

3.  Add Arc to your authenticator app.

    -   To use the QR code, scan it with your authenticator app.
    -   To enter the secret code manually, copy the value in the **Secret** field and enter it in your authenticator app.
4.  In the **Verify** field, enter the six-digit code from your authenticator app.

5.  Select **Verify**.

6.  Select the **Require TOTP for action approvals** check box.


## Result

Arc prompts you for a code from your authenticator app before approving sensitive actions.

**Parent Topic:**[Using ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-using.md)

