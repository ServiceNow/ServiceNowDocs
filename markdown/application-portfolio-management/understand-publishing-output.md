---
title: Understanding the publishing results and knowledge base output
description: Understand what happens after you publish or republish a TRM catalog and how to interpret the results in the Publishing Center and the knowledge base.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/understand-publishing-output.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with the publishing center, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Understanding the publishing results and knowledge base output

Understand what happens after you publish or republish a TRM catalog and how to interpret the results in the Publishing Center and the knowledge base.

## Publishing results in the Publishing Center

When you publish or republish a TRM catalog, the Publishing Center tracks the outcome of the publishing operation. For more information, see [View publishing status and run log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/view-run-log.md).

## Knowledge base output

Publishing a TRM catalog generates knowledge base content that you can browse and search. After publishing, a catalog link is generated. For more information, see [Access the published TRM catalog knowledge base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/access-the-published-kb.md).

**Note:** The **Authored by** and **Revised by** fields on knowledge base articles reflect the account that triggered the update:

-   Articles created or updated through the **Publish** button in the Publishing Center show **System Administrator** in both fields, because publishing runs as a scheduled job.
-   Articles updated automatically when a TRM product or product lifecycle record changes show the logged-in user who made the change.

## How TRM content is structured in the knowledge base

Each TRM product is published as a Knowledge Base article with predefined sections. Common sections include:

-   General Information- This section presents high‑level product details, such as:
    -   Product name
    -   Product type \(for example, Software or Hardware\)
    -   TRM phase
    -   Category name
    -   Company or vendor name
    -   Category owner
    -   Investment direction
    -   Business justification
-   Product Lifecycles- This section presents the lifecycle‑specific information for the product, such as:
    -   Model or version details
    -   Lifecycle phase
    -   Phase start and end dates
    -   Descriptions or notes related to lifecycle phases

## Access and visibility

Access to the published TRM catalog depends on how the catalog and Knowledge Base are configured:

-   Internal catalogs require users to sign in to view the Knowledge Base content.
-   Public catalogs can be configured to allow guest access through a portal.

**Note:** The knowledge base content is always read‑only. To make changes, update TRM data or publishing configuration, and publish or republish the catalog.

**Parent Topic:**[Working with the publishing center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/working-with-publishing-center.md)

**Related topics**  


[Publish a TRM catalog to the knowledge base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/publish-trm-cat-to-kb.md)

[Create a configuration to publish TRM data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/config-trm-data-to-publish.md)

[Access the published TRM catalog knowledge base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/access-the-published-kb.md)

