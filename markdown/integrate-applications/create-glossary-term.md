---
title: Create a glossary term
description: Create glossary terms to define business concepts and provide context for data assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/create-glossary-term.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [glossary term, business glossary, data catalog]
breadcrumb: [Managing glossary terms, Data Catalog, Workflow Data Fabric]
---

# Create a glossary term

Create glossary terms to define business concepts and provide context for data assets.

## Before you begin

Role required: Data Steward \(df\_data\_steward\)

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Data catalog icon in the left sidebar.

3.  Select **Create** &gt; **Glossary term**.

4.  Complete the general details:

    -   **Name**: The name of the business term. For example, Customer Lifetime Value.
    -   **Alternate name**: Alternative names for the same concept.
    -   **Description**: A clear explanation of what the term means. Use the rich text editor tools to format the content and add images, links, tables, and other elements.
5.  Complete the governance details:

    -   **Lifecycle status**: Current state of the glossary term. Possible values are: **Approved**, **Deprecated**, **Draft**, **In review**, **Rejected**.
    -   **Version**: Version number or label for the term.
    -   **Status message**: Description of why the glossary term is in its status. Use the rich text editor tools to format the content and add images, links, tables, and other elements.
    -   **Owner**: Person responsible for the term definition.
    -   **Reviewer**: Person responsible for reviewing the glossary term.
6.  Complete the classification details:

    -   **Domain**: Select from the list of available domains. Domains organize data assets into logical groupings based on business areas, departments, or data types. For details about creating domains, see [Create catalog domains](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-domains-dc.md).
    -   **Tags**: Select from the list of available tags. Catalog tags are metadata labels for classifying, categorizing, and discovering data assets. For details about creating tags, see [Create catalog tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-tags-dc.md).
7.  Complete the context details:

    -   **Related terms**: Other glossary terms connected to this concept.
    -   **Related assets**: Link the glossary term to a collected data asset \(non-glossary term\) to provide further context to the data asset.
    -   **Parent Term**: Relationship with a broader or more general term or concept that provides context and disambiguation of the child term.
    -   **Child Term**: Relationship with a narrower or more specific term or concept that provides context and helps disambiguate child terms.
    -   **Reference URL**: URLs where the term is defined or more context is accessed.
8.  Select **Save**. \[Omitted image "dc-glossary-create.png"\] Alt text: Create a glossary term


**Parent Topic:**[Managing glossary terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/managing-glossary-terms.md)

