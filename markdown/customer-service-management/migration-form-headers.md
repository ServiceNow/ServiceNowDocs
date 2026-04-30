---
title: Form headers
description: Learn how Workspace form headers function with Configurable Workspace.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Form headers

Learn how Workspace form headers function with Configurable Workspace.

Form headers provide an overview of the record.

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_aw\_form\_header|sys\_aw\_form\_header sys\_ux\_header\_config sys\_ux\_m2m\_workspace\_header\_ux\_header\_config|

To migrate your Workspace form header to Configurable Workspace, add an additional step in custom form headers to the Configurable Workspace form header setup.

-   An additional form header configuration is provided out of box, CSM/FSM Configurable Workspace Header Config.
-   Legacy form headers function without modification, but may affect the functionality of Configurable Workspace.
-   Add the Form header component to your Configurable Workspace for additional functionality.

For additional information, see [Set up a form header in Configurable Workspace](../task/config-csm-config-ws-form-header.md).

