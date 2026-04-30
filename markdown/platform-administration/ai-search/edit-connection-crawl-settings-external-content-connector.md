---
title: Edit connection or crawl settings for an external content connector
description: Connector administrators can modify the connection settings and crawl settings for an existing external content connector. If your changes to a connector's settings invalidate its current crawl results, the system prompts you to run a new content crawl.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-02"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Edit connection or crawl settings for an external content connector

Connector administrators can modify the connection settings and crawl settings for an existing external content connector. If your changes to a connector's settings invalidate its current crawl results, the system prompts you to run a new content crawl.

## Before you begin

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. Perform it only if you need to modify the connection settings or crawl settings specified for one of your existing external content connectors.

Modify a connector's connection settings to reflect changes made in your source system's configuration. As an example, if your source system administrator generates a new client secret for the OAuth 2.0 application that grants the connector access to your content, you can replace the old client secret with the new one in the connector's connection settings.

Modify a connector's crawl settings to alter the set of source system locations it crawls and the set of source system items it retrieves searchable content and metadata from. As an example, if you want to exclude content from items in a newly created Slack channel, you can add that channel to the channel exclusion list in your Slack external content connector's crawl settings.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, choose which settings you want to modify:

    -   To modify connection settings for the external content connector, select **Connection settings**.
    -   To modify crawl settings for the external content connector, select **Crawl settings**.
4.  On the selected settings page, make your desired changes.

    For details on connection settings, see the creation task for the external content connector type, as listed in [Creating external content connectors](creating-ext-cont-connectors.md).

    For details on crawl settings, see the crawl-settings configuration task for the external content connector type, as listed in [Configuring crawl settings for external content connectors](../concept/cfg-crawl-settings-ext-cont-connector.md).

5.  Select **Save and Validate**.


## Result

The external content connector you selected is updated with your modified connection settings or crawl settings.

If your modifications to the connector's connection or crawl settings invalidate its existing content crawl results, the connector status changes to indicate that a recrawl is required.

## What to do next

If the external content connector status indicates that a recrawl is required, run a new content crawl for it to update its search results using the modified settings. For details on running content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Configuring External Content Connectors](../concept/configuring-ext-cont-connectors.md)

