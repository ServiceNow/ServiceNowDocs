---
title: Configure ServiceNow Otto for Zero Copy Connector
description: If you have the admin role, you can configure the ServiceNow Otto for Zero Copy Connector application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/configure-now-assist-for-zero-copy-connectors.html
release: australia
topic_type: task
last_updated: "2026-07-22"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [ServiceNow Otto for Zero Copy Connector, Workflow Data Fabric]
---

# Configure ServiceNow Otto for Zero Copy Connector

If you have the admin role, you can configure the ServiceNow Otto for Zero Copy Connector application.

## Before you begin

Role required: admin and sn\_erp\_integration.erp\_ai\_user

## About this task

Use the AI Admin Hub console to configure ServiceNow Otto for ZCC. For additional information, see [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).

The following skills are included in ServiceNow Otto for ZCC:

-   ERP data discovery
-   ERP data query

## Procedure

1.  Install the ServiceNow Otto for Zero Copy Connector plugin \(sn\_erp\_ai\).

    For information about the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

2.  View the skills by navigating to **All** &gt; **Otto admin** &gt; **Skills** and selecting **Other**.

3.  Edit skill access by selecting the options icon next to the **Last modified** column and selecting **Edit access**.

    1.  Select the edit \(pencil\) icon \[Omitted image "pencil-outline-24.svg"\].

        \[Omitted image "erp-edit-access1.png"\] Alt text: Edit access modal with pencil highlighted.

    2.  Select **Any authenticated user** or **Select roles**.

        \[Omitted image "erp-edit-access2.png"\] Alt text: Edit ACL modal with user access options highlighted.

        If you specified **Select roles**, add and delete roles as needed. To add a role, select inside the **Roles** text box and select a role from the list.

        To delete a role, select the X icon within the pill.

        \[Omitted image "erp-edit-access3.png"\] Alt text: Edit ACL modal with roles drop-down list displayed.

        **Note:** The sn\_erp\_integration.erp\_ai\_user role is required for users to work with generative and agentic AI in ServiceNow Otto for ZCC.

    3.  When you're finished, select **Apply**.

4.  You can delete a skill at any time by selecting the icon next to **Last modified** and selecting **Deactivate skill**.


**Related topics**  


[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md)

[Configuring AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-na-landing.md)

