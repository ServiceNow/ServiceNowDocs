---
title: Integrating with Workday
description: Integrating your Software Asset Management application with the Workday applications enables you to track your software subscriptions.
locale: en-US
release: yokohama
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Workday

Integrating your Software Asset Management application with the Workday applications enables you to track your software subscriptions.

With this integration, you can track software subscriptions for the following Workday applications:

-   Workday Human Capital Management
-   Workday Financial Management

Use either of the following authentication methods to integrate your ServiceNow instance with Workday.

-   [Basic Authentication](integrate-with-workday-basicauth.md#)
-   [OAuth 2.0](integrate-with-workday-oauth.md#)

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the Workday application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

User having the following Domain Security Policy:-   Worker Data
    -   Public Worker Reports
    -   Workers
    -   Current Staffing Information
-   Person Data: Work Address
-   Workday Accounts
    -   WQL for Workday Extend
    -   Workday Query Language

</td><td>

None

</td></tr></tbody>
</table>