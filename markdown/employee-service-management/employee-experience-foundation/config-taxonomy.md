---
title: Unified Taxonomy for Employee Center
description: Unified Taxonomy is a collection of hierarchical topics that brings together different content types, such as requests, articles, quick links, learning content, and employee communications.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [taxonomy, employee center taxonomy]
breadcrumb: [Setup browse experience features, Configure, Employee Center, Employee Service Management]
---

# Unified Taxonomy for Employee Center

Unified Taxonomy is a collection of hierarchical topics that brings together different content types, such as requests, articles, quick links, learning content, and employee communications.

In the Employee Center portal, you can use this capability to span across departments to provide a single employee-centric taxonomy. Unified Taxonomy sits at the core of the Curated Experiences. Set up the Unified Taxonomy to leverage the full potential of the Curated Experiences.

![Curated experiences for Employee Center portal](../images/curated-exp.jpg)

The Unified Taxonomy is built on these models.

-   Content taxonomy \(Data model\): Provides the data model or the framework against which the content is mapped. This is the top-three levels of the topic. For example, **IT** &gt; **Hardware** &gt; **Printers**.
-   Content Authoring \(Taxonomy management\): Provides content managers and contributors the ability to tag content against the taxonomy and manage the taxonomy.
-   Taxonomy for employee content: Is the actual content mapped to the taxonomy. This provides the mapping to the default content shipped by IT, HRSD, and Legal into the content taxonomy.

![Representation of the taxonomy layer](../images/taxonomy-layer.jpg)

The Unified Taxonomy capability is delivered by ServiceNow AI Platform as two separate plugin and application.

-   **Content Taxonomy**

    The application that provides the data model or the topic hierarchy and the taxonomy management \(content authoring\) capabilities for the Unified Taxonomy.

    This application is available by default to all customers.

-   **Employee Experience Taxonomy**

    The plugin that provides the mapping of all the default content for IT, HR, Workplace, Legal, and Procurement into the default content taxonomy. The content types mapped by default are requests, articles, quick links, learning content, and employee communications. Once the plugin is downloaded, this mapping will be visible as part of the content taxonomy app in the platform.

    To get the default taxonomy for employee content, you must download it from ServiceNow Store. On installation, the default content taxonomy displays the available list of topics prescribed for the product or services based on what you are licensed to, such as IT, HR, WSD, PSM, or Legal.


After you complete the installation, perform the following to achieve a Unified Taxonomy experience.

-   Clone the employee content taxonomy and make appropriate additions or modifications to the provided topic structure. Taxonomy is updated to reflect the terminology and available services. For more information, see [Clone taxonomy for employee content](../task/clone-taxonomy-content.md).
-   Associate all the existing and new content to the cloned taxonomy topics. For more information, see [Create and associate topics](../task/create-topics-for-taxonomy.md).
-   Enable user criteria to configure topic-level security and visibility settings for topics. For more information, see [Enable user criteria for topics](../task/enable-user-criteria-topics.md).
-   Update the search configurations to filter based on the content associated to the cloned taxonomy.

**Related topics**  


[Taxonomy form](../reference/taxonomy-form.md)

