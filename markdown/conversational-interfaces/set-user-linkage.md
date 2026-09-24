---
title: Redirect user authentication to a Service Portal
description: After installing a pre-built Conversational Integration, you can specify a Service Portal in which unauthenticated end users complete the user authentication step \(user account linking\), instead of in their ServiceNow instance. Users who do not have linked accounts complete authentication before continuing with Virtual Agent in the messaging application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/set-user-linkage.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Integrate VA with messaging apps, Conversational Integration apps for Virtual Agent, Conversational Interfaces]
---

# Redirect user authentication to a Service Portal

After installing a pre-built Conversational Integration, you can specify a Service Portal in which unauthenticated end users complete the user authentication step \(user account linking\), instead of in their ServiceNow instance. Users who do not have linked accounts complete authentication before continuing with Virtual Agent in the messaging application.

## Before you begin

Install the Virtual Agent messaging integrations for your instance. The system creates a record in the Provider Auth \[provider\_auth\] table for each integration that you install. You use the Provider Auth table to specify the Service Portal in which user authentication occurs.

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `provider_auth.list` in the filter.

2.  In the Provider Auth table, open the record for the messaging integration you installed.

3.  In the **Service Portal** field, select the Service Portal in which user authentication occurs.

4.  Click **Update**.


## Result

When unauthenticated users start a conversation with Virtual Agent for the first time in the messaging integration, they are redirected to the Service Portal specified for the provider in the Provider Auth table. After they log in to the Service Portal, they are prompted to [link their ServiceNow account to the messaging application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/link-accounts-with-virtual-agent.md).

**Parent Topic:**[Integrating Virtual Agent with messaging apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-integration-messaging-apps.md)

