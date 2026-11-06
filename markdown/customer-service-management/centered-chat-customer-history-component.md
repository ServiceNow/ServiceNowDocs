---
title: Customer History component
description: The Customer History component displays customer, consumer, or account history information, depending on the field selections on the interaction record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/centered-chat-customer-history-component.html
release: australia
topic_type: reference
last_updated: "2026-10-19"
reading_time_minutes: 1
breadcrumb: [CSM centered chat interaction record page, Record pages, Record pages and page templates, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Customer History component

The Customer History component displays customer, consumer, or account history information, depending on the field selections on the interaction record.

The Customer History component appears after the Interaction Controls component. This component is included with the [Customer Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-central.md) plugin, which is activated as part of the CRM Workspace application.

The Customer History component includes the **Customer** tab. This tab displays customer, consumer, or account history information, depending on the customer information provided on the interaction record. This tab also includes a search field, filter, and date range selector that agents can use to find specific information in the history.

<table id="table_pyc_pgl_ydc"><thead><tr><th>

Interaction record information

</th><th>

Customer tab information

</th></tr></thead><tbody><tr><td>

Customer information is provided

</td><td>

When a customer is selected on the interaction record and customer history is available, the customer history is displayed in the Customer History tab.If customer history is not available, the Customer History tab displays a message that there is no activity yet.

</td></tr><tr><td>

Customer information is not provided

</td><td>

When a customer is not selected on the interaction record, the Customer History tab displays a message suggesting to link to a customer.

</td></tr><tr><td>

Account information is provided

</td><td>

When an account is selected on the interaction record, the account history is displayed in the Customer History tab.

</td></tr></tbody>
</table>Refreshing the customer history information:

-   When an agent selects a different customer on the interaction record and then saves the record: the agent must select **Refresh** on the Customer History component to update the information. The agent can also refresh the record page.
-   If there is new activity while the page is open: the agent must refresh the Customer History component or the record page to display the new activity in the Customer History tab. For example, this occurs when the agent selects **Create Case** on the interaction record.

