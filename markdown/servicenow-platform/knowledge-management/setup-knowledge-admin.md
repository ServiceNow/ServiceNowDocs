---
title: Knowledge Management setup guide for admins
description: Before users in your organization can start creating knowledge bases and knowledge articles, you must set up Knowledge Management. Work with stakeholders to define requirements for setting up Knowledge Management effectively to meet the needs of users.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge Management setup guide for admins

Before users in your organization can start creating knowledge bases and knowledge articles, you must set up Knowledge Management. Work with stakeholders to define requirements for setting up Knowledge Management effectively to meet the needs of users.

## Requirements

Role required: admin.

## Before you begin

-   **Meet with the stakeholders**

    |Stakeholder|Responsibilities|
    |-----------|----------------|
    |Knowledge manager|Defines and oversees the knowledge management processes for day-to-day operations related to content publishing and usage.|
    |Knowledge admin|Configures advanced settings for specific Knowledge Management features|
    |Knowledge coach|Enables users to adhere to content standards.|
    |Knowledge domain expert|Provides domain knowledge expertise.|
    |Version author|Contributor to a particular version of an article.|
    |Content creators and reviewers|Create, review, and update articles in the knowledge bases.|
    |Community managers|Focus on the creation and curating of social content.|
    |Line managers|Manage teams that create and use knowledge articles|

-   **With stakeholders, determine the following requirements**
    -   Who are the consumers of the content in the knowledge bases?
    -   Who are the writers, editors, and managers for the knowledge base articles?
    -   What are the required workflows to publish and retire articles?
    -   What are the unique behaviors required for your knowledge management implementation? For example, should attachments appear in search results?
    -   Do you want to translate knowledge articles into other languages?

## What to do

-   **Assign knowledge roles to users and groups**

    Determine which [Knowledge Management roles](r_KnowledgeRoles.md#) are appropriate for each user, and then [assign those roles](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) .

-   **Create custom Knowledge workflows**

    If the default [knowledge workflows](r_KnowledgeWorkflows.md) for publishing and retiring knowledge articles are not appropriate for your knowledge bases, create custom [workflows](https://www.servicenow.com/docs/access?context=c_WorkflowOverview&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) for those knowledge bases.

-   **Configure Knowledge properties**

    If the default [knowledge properties](r_KnowledgeProperties.md#) do not fulfill the requirements of users, reconfigure the properties as necessary.

-   **Activate support for other languages besides English**

    If languages other than English must be supported, activate the [Knowledge Management Internationalization](../concept/c_I18NKMInternational.md) plugins.

-   **Coordinate with knowledge managers for knowledge base setup**

    Let knowledge managers and administrators know that they can start configuring their knowledge bases. For details, refer them to the [Knowledge base setup guide for knowledge admins and managers](set-up-knowledge-admin-user.md).


## Next steps

Depending on any other requirements for the knowledge bases, you may be asked to help with additional tasks, such as configuring knowledge landing pages.

## Using guided setup to implement Knowledge Management

Knowledge Management guided setup provides a sequence of tasks that help you configure Knowledge Management on your instance. To open Knowledge Management guided setup, navigate to **Knowledge** &gt; **Administration** &gt; **Guided Setup**.

For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

**Parent Topic:**[Configuring Knowledge Management](../concept/configuring-knowledge-management.md)

