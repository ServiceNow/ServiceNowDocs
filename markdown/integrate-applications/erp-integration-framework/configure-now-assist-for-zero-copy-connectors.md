---
title: Configure Now Assist for Zero Copy Connector
description: If you have the admin role, you can configure the Now Assist for Zero Copy Connector application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/erp-integration-framework/configure-now-assist-for-zero-copy-connectors.html
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-11-04"
reading_time_minutes: 1
keywords: [Now Assist, agentic AI, generative AI, Gen AI, zero copy connector, erp]
breadcrumb: [Now Assist for Zero Copy Connector, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Configure Now Assist for Zero Copy Connector

If you have the admin role, you can configure the Now Assist for Zero Copy Connector application.

## Before you begin

Role required: admin and sn\_erp\_integration.erp\_ai\_user

## About this task

Use the Now Assist Admin console to configure Now Assist for Zero Copy Connector. For additional information, see [Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/configuring-now-assist.md).

The following skills are included in Now Assist for Zero Copy Connector:

-   ERP data discovery
-   ERP data query

## Procedure

1.  Install the Now Assist for Zero Copy Connector plugin \(sn\_erp\_ai\).

    For information about the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/install-now-assist-feature-plugins.md).

2.  View the skills by navigating to **All** &gt; **Now Assist admin** &gt; **Skills** and selecting **Other**.

3.  Edit skill access by selecting the options icon next to the **Last modified** column and selecting **Edit access**.

    \[Omitted image "erp-na-configure1.png"\] Alt text: Now Assist skills list with other skills displayed and two now assist for zero copy connector skills highlighted.

    1.  Select the edit \(pencil\) icon \[Omitted image "pencil-outline-24.svg"\] Alt text:.

        \[Omitted image "erp-edit-access1.png"\] Alt text: Edit access modal with pencil icon highlighted.

    2.  Select **Any authenticated user** or **Select roles**.

        \[Omitted image "erp-edit-access2.png"\] Alt text: Edit ACL modal with user access options highlighted.

        If you specified **Select roles**, add and delete roles as needed. To delete a role, select the X icon within the pill.

        To add a role, select inside the **Roles** text box and select a role from the list.

        \[Omitted image "erp-edit-access3.png"\] Alt text: Edit ACL modal with roles drop-down list displayed.

        **Note:** The sn\_erp\_integration.erp\_ai\_user role is required for users to work with generative and agentic AI in Now Assist for Zero Copy Connector.

    3.  When you're finished, select **Apply**.

4.  You can delete a skill at any time by selecting the icon next to **Last modified** and selecting **Deactivate skill**.


**Related topics**  


[Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/configuring-now-assist.md)

[Configuring Now Assist Admin features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/configuring-na-landing.md)

