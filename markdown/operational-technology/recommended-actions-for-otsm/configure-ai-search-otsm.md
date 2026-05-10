---
title: Configure AI Search for Operational Technology Service Management
description: Configure AI Search for Recommended Actions for Operational Technology Service Management \(OTSM\) to enable intelligent query features that help you quickly find the answers you need for OT incidents.
locale: en-US
release: australia
product: Recommended Actions for OTSM
classification: recommended-actions-for-otsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Recommended Actions for OTSM, Operational Technology]
---

# Configure AI Search for Operational Technology Service Management

Configure AI Search for Recommended Actions for Operational Technology Service Management \(OTSM\) to enable intelligent query features that help you quickly find the answers you need for OT incidents.

## Before you begin

Role required: admin

## About this task

For Operational Technology Service Management users, you must define the OT incident \[sn\_ot\_incident\] table as an indexed source in order to use AI Search for OT incident records. For more information about indexing, see [Indexed sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/indexed-sources-ais.md).

**Note:** Knowledge \[kb\_knowledge\] is also used as an indexed source for Recommended Actions for OTSM, but Knowledge is already indexed.

To define indexed sources, you can use the Guided Setup for AI Search. The following procedure describes how to access the **Define indexed sources** task. For more information about the Guided Setup for AI Search, see [Configuring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configuring-ais.md).

## Procedure

1.  Navigate to **AI Search** &gt; **Guided Setup**.

2.  In the **Define Searchable Content** section, select the **Define indexed sources** task.

3.  Select **Configure**.

4.  In the **AI Search Indexed Sources** list, select the OT Incident record.

5.  Select the **Index Selected Table/s** button.


**Parent Topic:**[Configuring Recommended Actions for Operational Technology Service Management \(OTSM\)](../../operational-technology-recommended-actions/concept/configuring-recommended-actions-otsm.md)

