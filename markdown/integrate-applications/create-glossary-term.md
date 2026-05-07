---
title: Create a glossary term
description: Create glossary terms to define business concepts and provide context for data assets.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Governing the Data Catalog, Data Catalog, Workflow Data Fabric]
---

# Create a glossary term

Create glossary terms to define business concepts and provide context for data assets.

## Before you begin

Role required: Data Steward \(df\_data\_steward\)

## About this task

Business glossary terms define business concepts and can be linked to catalog assets to provide business context. Terms include definitions, synonyms, related concepts, and ownership information. Use glossary terms to bridge the gap between technical data structures and business understanding. ![List of glossary terms](../image/dc-glossary-list.png)

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Data catalog icon in the left sidebar.

3.  Select **Create** &gt; **Glossary term**.

4.  Complete the general details.

    -   Name: The name of the business term. For example, Customer Lifetime Value.
    -   Alternate name: Alternative names for the same concept.
    -   Description: A clear explanation of what the term means.
5.  Complete the governance details.

    -   Lifecycle status: Current state of the glossary term. Possible values are: Approved, Deprecated, Draft, In review, Rejected.
    -   Version: Provide a version number or label for the term.
    -   Status message: Description of why the data asset is in its status.
    -   Owner: Person responsible for the term definition.
    -   Reviewer: Person responsible for reviewing the glossary term.
6.  Complete the classification details.

    -   Domain: Terms that represent the logical grouping of related data assets \(like customer or product data\).
    -   Tags: A non-hierarchical label or keyword that provides context and descriptive metadata to a piece of data, making it easier to organize, locate, and manage.
7.  Complete the context details.

    -   Related terms: Other glossary terms connected to this concept.
    -   Related assets: Link the glossary term to a collected data asset \(non-glossary term\) to provide further context to the data asset.
    -   Parent Term: Relationship with a broader - or more general – term or concept giving important context and disambiguation of the child term
    -   Child Term: Relationship with a narrower - or more specific – term or concept giving important context and helping to disambiguate child terms
    -   Reference URL: URLs where the term is defined or more context is accessed.
8.  Select **Save**. ![Create a glossary term](../image/dc-glossary-create.png)


**Parent Topic:**[Governing the Data Catalog](../concept/manage-data-catalog.md)

