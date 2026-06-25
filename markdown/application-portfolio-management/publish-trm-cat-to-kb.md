---
title: Publish a TRM catalog to the knowledge base
description: Publish a Technology Reference Model \(TRM\) catalog to the ServiceNow Knowledge Base, making approved technology standards available for broader discovery and consumption.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/publish-trm-cat-to-kb.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with the publishing center, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Publish a TRM catalog to the knowledge base

Publish a Technology Reference Model \(TRM\) catalog to the ServiceNow Knowledge Base, making approved technology standards available for broader discovery and consumption.

## Before you begin

Role required: sn\_apm.apm\_admin and knowledge\_admin

## About this task

When you publish a TRM catalog, the details such as products, lifecycle phases, and standards are transformed into structured Knowledge Base articles that can be searched, browsed, and consumed across the organization. This allows technology standards maintained by enterprise architects to be accessed by a much broader audience, including application owners, developers, and solution architects.

**Note:** You can create only one publishing configuration for a specific combination of catalog type and access type within the same domain.

## Procedure

1.  Navigate to **Workspace** &gt; **Enterprise Architecture Workspace**.

2.  Open the Setup page by selecting the Setup icon \[Omitted image "setup-icon.png"\] Alt text: Setup icon.

3.  Select the expand row icon \(\[Omitted image "ExpandIcon.png"\] Alt text: Expand Row icon\) next to **Publishing Center**.

4.  Select **All**.

5.  Open the catalog that you want to publish or create a new configuration to publish.

    For instructions to create a new configuration,see [Create a configuration to publish TRM data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/config-trm-data-to-publish.md).

    **Note:** If you plan to publish a public catalog for guest users, ensure that your knowledge portal is configured to allow public access. Publishing applies knowledge base access settings based on the access type selected for the catalog.

6.  Select **Publish**.


## Result

After publishing, you can see the following changes on the **Details** tab:

-   A message appears on the banner with a link to the published knowledge base article. You can select the **View catalog** link to navigate to the knowledge base article.
-   The **Status** field value is changed to **Published**.
-   The **Catalog link** field displays a URL to the published catalog.

**Parent Topic:**[Working with the publishing center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/working-with-publishing-center.md)

**Related topics**  


[Working with the publishing center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/working-with-publishing-center.md)

[Create a configuration to publish TRM data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/config-trm-data-to-publish.md)

[Edit a published TRM catalog configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/modify-trm-cat-pub-config.md)

[Associate a portal with a knowledge base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/associate-portal-to-trm-cat.md)

[Republish a TRM catalog after updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/republish-trm-cat.md)

[Understanding the publishing results and knowledge base output](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/understand-publishing-output.md)

