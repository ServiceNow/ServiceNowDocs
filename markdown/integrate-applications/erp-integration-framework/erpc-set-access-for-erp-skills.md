---
title: Set access controls for ERP skills
description: Choose whether any authenticated user or only users with specific roles can use the ERP data discovery and ERP data query skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erpc-set-access-for-erp-skills.html
release: brazil
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-11-03"
reading_time_minutes: 1
keywords: [erp, zero, copy, connector, ai, otto, skill, access, acl, role, erp\_ai\_user]
breadcrumb: [Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Set access controls for ERP skills

Choose whether any authenticated user or only users with specific roles can use the ERP data discovery and ERP data query skills.

## Before you begin

Role required: admin

The ServiceNow Otto for Zero Copy Connector plugin is installed. For more information, see [Install the ServiceNow Otto for Zero Copy Connector plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-install-the-erp-ai-plugin.md).

## About this task

The sn\_erp\_integration.erp\_ai\_user role is required to use generative AI and agentic AI in Zero Copy Connector for ERP.

## Procedure

1.  Navigate to **All** &gt; **Otto admin** &gt; **Skills** and select **Other**.

2.  For the skill that you want to update, select the options icon next to the **Last modified** column and select **Edit access**.

3.  Select the edit \(pencil\) icon \[Omitted image "pencil-outline-24.svg"\].

    \[Omitted image "erp-edit-access1.png"\] Alt text: Edit access modal with pencil highlighted.

4.  Select **Any authenticated user** or **Select roles**.

    \[Omitted image "erp-edit-access2.png"\] Alt text: Edit ACL modal with user access options highlighted.

5.  If you selected **Select roles**, add or remove roles.

    -   To add a role, select inside the **Roles** field and select a role from the list.
    -   To remove a role, select the X icon in its pill.
    \[Omitted image "erp-edit-access3.png"\] Alt text: Edit ACL modal with roles drop-down list displayed.

6.  Select **Apply**.


## Result

Only users who meet the access setting can use the skill.

**Parent Topic:**[Configuring Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-integration-configuration-overview.md)

**Related topics**  


[Requirements for using AI in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-prereqs-for-ai.md)

