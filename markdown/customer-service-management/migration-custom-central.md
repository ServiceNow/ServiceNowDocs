---
title: Customer Central
description: Learn about how CSM Agent Workspace Customer Central functions with CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/migration-custom-central.html
release: australia
topic_type: concept
last_updated: "2026-10-25"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Customer Central

Learn about how CSM Agent Workspace Customer Central functions with CSM Configurable Workspace.

Customer Central displays all the touch points that a customer has had with a contact center in the form of information cards. CSM Agent Workspace Customer Central configurations function in CSM Configurable Workspace. Configuration changes at the sn\_customercentral\_cust\_info\_config and sys\_declarative\_action\_assignment and their related lists, however, can be configured in CSM Configurable Workspace.

In CSM Agent Workspace, Customer Central was available on interaction records only. CSM Configurable Workspace extends it to case, account, contact, and consumer records, so agents can see the same customer context, including interaction history, open cases, and related records, before they act. Your existing configuration carries over and continues to work on interaction records.

-   Set up the Customer Information view in CSM Configurable Workspace using [Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/cust-central-configure-info-tab.md).
-   Set up the Customer Information view in CSM Agent Workspace using [Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/configure-information-tab.md).

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_declarative\_action\_assignment|sys\_ux\_screen|

## Verify and extend Customer Central after migration

Role required: admin

1.  Open an interaction record in CSM Configurable Workspace and confirm that the Customer Central panel displays the customer information cards correctly.
2.  Open a case record and check whether the Customer Central tabs appear.

    If they don't appear, extend the configuration to case records in the next step.

3.  Navigate to **Customer Service** &gt; **Administration** &gt; **Guided Setup** &gt; **CSM Configurable Workspace** and use the Customer Central configuration category to set up Customer Central on case, account, contact, and consumer record pages.
4.  Verify that Customer Central appears correctly on each record type that your agents use.

## Tips for Customer Central

Customer Central shows customer data in two views: Customer Information and Customer History.

-   In the Customer Information view, include only the critical customer information that agents need quick access to, such as specific reports, lists, and records.
-   To keep both views up to date, set the number of days of data to display. Navigate to **All** &gt; **Customer Central** &gt; **Administration** &gt; **Properties** and enter the number of days. The default is 30, and the setting applies to both the Customer Information and Customer History views.
-   When you configure the Customer History view, set the application scope to Customer Central.

