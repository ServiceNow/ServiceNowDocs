---
title: Create a new configuration to publish TRM data
description: Define configuration for a Technology Reference Model \(TRM\) catalog that can be published to the knowledge base article.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with the publishing center, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Create a new configuration to publish TRM data

Define configuration for a Technology Reference Model \(TRM\) catalog that can be published to the knowledge base article.

## Before you begin

Role required: sn\_apm.apm\_admin and knowledge\_admin

## About this task

Publishing a TRM catalog involves creating a publishing configuration in the Publishing Center and executing it to generate knowledge base content.

**Note:** If you can’t republish the catalog due to permissions, contact a knowledge administrator to republish and apply the changes.

## Procedure

1.  Navigate to **Workspace** &gt; **Enterprise Architecture Workspace**.

2.  Open the Setup page by selecting the Setup icon ![Setup icon](../../image/eaw-image/setup-icon.png).

3.  Select the expand row icon \(![Expand Row icon](../../image/ExpandIcon.png)\) next to **Publishing Center**.

4.  Select **All**.

5.  Select **New**.

6.  On the form, fill in the fields.

    For field information, see [Create new publishing configuration form](../../reference/eaw-reference/create-pub-config-form.md).

7.  Select **Save**.

    The details are saved and the configuration is available in the Publishing Center list.

    After a publishing configuration is created, the **Catalog type** and **Access type** fields become read‑only.


## Result

When you create a new TRM publishing configuration, the system automatically creates default publishing components. The following related records are created automatically:

-   **Article configurations**- For TRM, this tab displays the Software and Hardware product links along with display fields to appear on the knowledge base. By default, system displays the article configuration and content configuration for the product to be published. You can open the links to modify the article configuration and life cycle configuration. For more details, see [Edit a published TRM catalog configuration](modify-trm-cat-pub-config.md).
-   **Portals**- displays associated portals, where the knowledge base is published. You can associate a new knowledge base to the service portal. For more details, see Associate a portal to the knowledge base.

    **Note:** You can see this tab only when you have the Service Portal admin \(sp\_admin\) role assigned to you.

-   **Run logs**- displays the publishing status. You can also open the run log link and article configuration links to see all details for the published catalog. For more details, see [View publishing status and run log](view-run-log.md).

**Parent Topic:**[Working with the publishing center](../../concept/eaw-concept/working-with-publishing-center.md)

**Related topics**  


[Edit a published TRM catalog configuration](modify-trm-cat-pub-config.md)

[Associate a portal with a knowledge base](associate-portal-to-trm-cat.md)

[Publish a TRM catalog to the knowledge base](publish-trm-cat-to-kb.md)

[View publishing status and run log](view-run-log.md)

[Access the published TRM catalog knowledge base](access-the-published-kb.md)

[Understanding the publishing results and knowledge base output](../../reference/eaw-reference/understand-publishing-output.md)

