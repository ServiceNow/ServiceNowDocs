---
title: Resolve health issues for an external content connector
description: View and resolve connector health issues using the connector health dashboard in the external content connector editor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/resolve-health-issues-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-08-20"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Resolve health issues for an external content connector

View and resolve connector health issues using the connector health dashboard in the external content connector editor.

## Before you begin

Role required: sn\_ext\_conn.xcc\_admin

## About this task

External content connectors depend on a variety of configuration settings, permissions, and operations. Incorrect or outdated settings or permissions in the ServiceNow AI Platform® or the source system can prevent a connector from operating properly. Issues encountered during crawls may prevent specific content items from being retrieved and indexed for search.

Specific occurrences that can prevent proper function of an external content connector include:

-   Certificate expiration
-   Permission mismatches after a source system policy change
-   Connector plugin scope changes following an upgrade to External Content Connectors or the ServiceNow AI Platform
-   Quota exhaustion on the ServiceNow AI Platform side
-   User identity mapping gaps that silently conceal connector search results from users

When an external content connector has one or more of these health issues, its status changes to **Action required**. Perform the following steps to view and resolve health issues for the affected connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You must be in this scope to create or edit external content connectors.

3.  In the Connectors list, select the record for the external content connector that you want to check or resolve health issues for.

    **Note:** Connectors with health issues show **Action required** status.

4.  In the connector editor, select the Overview tab.

5.  Review the health category cards in the **Connector health** section.

    Each card includes a health category name, a status indicator, and a context label.

    -   **Health category name**

        The health category name describes which aspects of the external content connector's configuration and operations the card refers to.

        -   **Source connection**: Connection and authentication settings for the source system.
        -   **Internal connection**: ServiceNow AI Platform connectivity needed to run crawls.
        -   **Content Permissions**: Permissions needed to access content and metadata in the source system.
        -   **Content**: Status of crawled items and any crawl errors that need attention.
        -   **User permissions**: Status of user and group access permissions for secure search.
        -   **Search profile**: Assignment to at least one search profile.
    -   **Status indicator**

        The status indicator indicates the status of the health category for the external content connector. Typical values include **Ready**, **Not configured**, **Warning**, and **Error**.

    -   **Context label**

        The context label indicates whether the health category refers to settings in the ServiceNow AI Platform or settings in the external content connector's source system.

6.  For each health category card that shows a status other than **Ready**, perform the following steps.

    1.  Select the health category card.

        In the **Issues** section, actionable entries show all health issues associated with the selected health category.

    2.  Follow the provided action links or guidance to resolve all health issues for the selected health category.


## Result

The external content connector no longer shows **Action required** status.

**Parent Topic:**[Configuring External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configuring-ext-cont-connectors.md)

