---
title: Form headers
description: Learn how workspace form headers function with CRM Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/migration-form-headers.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Migrate to CRM Workspace, Migrating to CRM Workspace, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Form headers

Learn how workspace form headers function with CRM Workspace.

Form headers provide an overview of the record.

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_aw\_form\_header|sys\_aw\_form\_header sys\_ux\_header\_config sys\_ux\_m2m\_workspace\_header\_ux\_header\_config|

To migrate your workspace form header to CRM Workspace, add an additional step in custom form headers to the CRM Workspace form header setup.

-   An additional form header configuration is provided out of box, CRM Workspace Header Config.
-   Legacy form headers function without modification, but may affect the functionality of CRM Workspace.
-   Add the Form header component to your CRM Workspace for additional functionality.

For additional information, see [Set up a form header in Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-form-header.md).

