---
title: Edit a published TRM catalog configuration
description: Edit a published TRM catalog configuration to update catalog name, article publishing rules for software and hardware records, or manage portal and knowledge base mappings.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with the publishing center, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Edit a published TRM catalog configuration

Edit a published TRM catalog configuration to update catalog name, article publishing rules for software and hardware records, or manage portal and knowledge base mappings.

## Before you begin

Role required: sn\_apm.apm\_admin and knowledge\_admin

## About this task

When you update and save changes to a published catalog configuration, the catalog status changes from Published to Draft. You must republish the catalog to apply updates to the knowledge base.

## Procedure

1.  Navigate to **Workspace** &gt; **Enterprise Architecture Workspace**.

2.  Open the Setup page by selecting the Setup icon ![Setup icon](../../image/eaw-image/setup-icon.png).

3.  Select the expand row icon \(![Expand Row icon](../../image/ExpandIcon.png)\) next to **Publishing Center**.

4.  Select **All**.

5.  Select an existing catalog to modify its configuration.

    You can modify the following details:

    -   Update catalog details- In the **Details** tab, modify the catalog name.
    -   Update article publishing rules- In the **Article configurations** tab, select a software or hardware record to open its configuration and update details and its content configuration.
        -   **Details** tab- Define the content structure using AND/OR operators, modify display fields, and select or clear the **Active** check box to make the record active or inactive.
        -   **Content configurations**- Select a related configuration \(for example, Product lifecycles\), define the content structureusing AND/OR operators, modify display fields, and select or clear the **Active** check box to make the record active or inactive.
    -   Manage portal–knowledge base mappings- In the **Portals** tab, create or update a portal mapping for your published catalog, set the order for the knowledge base, and select or clear the **Active** check box to make the record active or inactive.
6.  Select **Save**.


## Result

The publishing configuration is updated based on your changes.

## What to do next

You must republish to apply changes to the published knowledge base output. Use the Run logs to monitor the publishing job and confirm completion.

**Parent Topic:**[Working with the publishing center](../../concept/eaw-concept/working-with-publishing-center.md)

**Related topics**  


[Republish a TRM catalog after updates](republish-trm-cat.md)

[View publishing status and run log](view-run-log.md)

[Access the published TRM catalog knowledge base](access-the-published-kb.md)

[Understanding the publishing results and knowledge base output](../../reference/eaw-reference/understand-publishing-output.md)

