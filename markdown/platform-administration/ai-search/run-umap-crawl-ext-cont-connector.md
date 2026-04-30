---
title: Run a one-time user mapping crawl for an external content connector
description: Retrieve users and group access permissions from your external content connector's data source on demand. A user mapping crawl maps retrieved user and group permissions to your ServiceNow AI Platform users to facilitate content security in your AI Search applications.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-02-05"
reading_time_minutes: 2
breadcrumb: [Crawl, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Run a one-time user mapping crawl for an external content connector

Retrieve users and group access permissions from your external content connector's data source on demand. A user mapping crawl maps retrieved user and group permissions to your ServiceNow AI Platform® users to facilitate content security in your AI Search applications.

## Before you begin

Role required: ais\_admin

## About this task

Create a one-time user mapping crawl when you want to retrieve updated users and group access permissions from a source system without configuring a scheduled crawl.

**Note:** Some external content connectors don't retrieve user and group access permissions. You can't run user mapping crawls for these connectors.

-   Predefined web sources external content connector
-   ServiceNow documentation external content connector
-   Slack external content connector

The Atlassian Confluence Cloud external content connector only maps permissions for Confluence Cloud users who have made their email addresses visible to all users. To allow user mapping, each Confluence Cloud user must set their own email visibility to **Anyone** as explained in the [https://support.atlassian.com/confluence-cloud/docs/configure-user-email-visibility/](https://support.atlassian.com/confluence-cloud/docs/configure-user-email-visibility/) Atlassian support resource.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  Select the record for the external content connector that you want to run a one-time user mapping crawl for.

3.  Select **Create crawls**, then select **Create one-time crawl**.

4.  In the Crawl settings dialog box, select **User mapping crawl**.

5.  Select **Start**.


## Result

The one-time user mapping crawl task is added to the crawl queue and runs when the system has availability.

**Note:** To prevent excessive load on your instance, the External Content Connectors application only allows a maximum of five crawls to run simultaneously, no matter how many connectors you have created. Both content crawls and user permission crawls count against this limit. For best performance, run and schedule your external content connector crawls so that they don't overlap.

You can monitor the one-time crawl's state and results from the Connector list, or examine the external content connector's crawl history or its user mappings to see more details. For instructions for viewing an external content connector's crawl history, see [Review crawl history and analytics for an external content connector](review-crawl-ext-cont-connector.md). To learn how to view an external content connector's user mappings, see [Review user mappings for an external content connector](review-usr-maps-ext-cont-connector.md).

**Parent Topic:**[Crawling content with External Content Connectors](../concept/using-ext-cont-connectors.md)

