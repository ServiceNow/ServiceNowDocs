---
title: Email Composer and Email Viewer
description: Learn about how the Email Composer and Email Viewer function with CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/migration-compose-preview-email.html
release: zurich
topic_type: concept
last_updated: "2026-10-25"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Email Composer and Email Viewer

Learn about how the Email Composer and Email Viewer function with CSM Configurable Workspace.

In CSM Agent Workspace, email was handled through the legacy platform interface. CSM Configurable Workspace uses dedicated Email Composer and Email Viewer components that you configure in UI Builder. There's no configuration to carry over, so configure both components on the record pages where agents handle email, such as the case record page. Without these components, agents can't use email in CSM Configurable Workspace.

## Email Composer

The Email Composer component enables requestors and fulfillers to use email to communicate. The component is associated with a record to include conversations as part of the record. For example, an agent can compose an email to a customer to gather information about the customer's case.

|Legacy table name|UIB table name|
|-----------------|--------------|
|No corresponding table|sys\_ux\_screen|

Configure the Email Composer in [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/ui-builder-overview.md).

For more information about the Email Composer component, see [Next Experience Components documentation](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades).

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**. On the **Experiences** tab, select **CSM/FSM Configurable Workspace**.
2.  Open the record page where you want to add the Email Composer, such as the case record page.
3.  Add the Email Composer component from the component library and configure it for the record.
4.  Select **Save**.

## Email Viewer

The Email Viewer component enables customer service agents to preview emails in CSM Configurable Workspace before sending them to customers. The component is associated with a record to include emails as part of the record.

|Legacy table name|UIB table name|
|-----------------|--------------|
|No corresponding table|sys\_ux\_screen|

Configure the Email Viewer in [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/ui-builder-overview.md).

For more information about the Email Viewer component, see [Next Experience Components documentation](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades).

1.  In UI Builder, open the record page where you added the Email Composer.
2.  Add the Email Viewer component from the component library and configure it to associate with the record.
3.  Select **Save**.

