---
title: Verify your connection settings and source system permissions for an external content connector
description: Check that connection settings and source system permissions are correctly specified for your external content connector. Perform this task to verify whether permission changes or revocations affect the connector's ongoing or scheduled crawls.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-09-18"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Verify your connection settings and source system permissions for an external content connector

Check that connection settings and source system permissions are correctly specified for your external content connector. Perform this task to verify whether permission changes or revocations affect the connector's ongoing or scheduled crawls.

## Before you begin

Role required: sn\_ext\_conn.xcc\_admin

## About this task

When you create a new external content connector, the system offers the option to validate your connection settings and verify that source system permissions are properly set to allow access by the connector.

Permission changes and revocations that occur after the connector is created can affect its ability to complete ongoing crawls or to run scheduled crawls. You can verify that the connector still has valid connection settings and source system permissions by running a one-time test crawl that only refreshes a small portion of the source system's searchable content and metadata. Success on this crawl indicates that your connection settings and source system permissions are valid. Failure may indicate that these settings should be double-checked.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the external content connector that you want to verify the connection settings and source system permissions for.

3.  In the connector editor's Settings tab, select **Index management**.

4.  In the Trigger test crawl section, select **Trigger test crawl**.


## Result

The external content connector runs a one-time test crawl. This crawl checks whether the connector's current connection settings and source system permissions enable it to refresh a small portion of its source system's searchable content and metadata.

The test crawl appears in the connector's crawl history with name **Test crawl** so you can monitor its status. For details on monitoring crawl history, see [Review crawl history for an external content connector](review-crawl-ext-cont-connector.md).

When the test crawl finishes its run, an alert message indicates whether it completed successfully or encountered errors. If it completed successfully, its connection settings and source system permissions are valid.

## What to do next

If the test crawl encountered errors, review its crawl history entries to see whether it experienced connection issues or source system permissions issues. If it did, ask your source system administrator to verify your connection settings and to confirm that the permissions required by the connector are properly set.

**Parent Topic:**[Configuring External Content Connectors](../concept/configuring-ext-cont-connectors.md)

