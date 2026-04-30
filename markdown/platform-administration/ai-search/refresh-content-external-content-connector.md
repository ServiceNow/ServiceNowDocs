---
title: Refresh content for an external content connector
description: Refresh searchable content and metadata, including unchanged items, for an external content connector by running a one-time full or partial content crawl.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-11-07"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Crawl, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Refresh content for an external content connector

Refresh searchable content and metadata, including unchanged items, for an external content connector by running a one-time full or partial content crawl.

## Before you begin

To run crawls for external content connectors, your instance must have inbound mTLS support enabled. For details on verifying that this feature is enabled on your instance, see [Verify whether inbound mTLS support is enabled for your instance](verify-adcv2-inbound-mtls-enabled.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

You can force an external content connector to refresh some or all of its searchable content and metadata by performing a one-time content crawl. This crawl ignores the change history for crawl locations and retrieved items. As a result, unchanged items that would normally be skipped are instead retrieved and reindexed along with changed items.

**Warning:** Refreshing content for a connector may take hours or days to complete, depending on the scope and scale of the content crawl.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the external content connector that you want to refresh content searchable content and metadata for.

3.  In the connector editor's Settings tab, select **Index management**.

4.  In the Force reindex section, select **Force reindex all content**.

5.  Select **Start reindex crawl**.


## Result

The external content connector runs a one-time full content crawl to refresh its searchable content and metadata.

This one-time crawl appears in the connector's crawl history with name **Force reindex** so you can monitor its status. For details on monitoring crawl history, see [Review crawl history for an external content connector](review-crawl-ext-cont-connector.md).

**Parent Topic:**[Crawling content with External Content Connectors](../concept/using-ext-cont-connectors.md)

