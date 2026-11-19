---
title: Differences between data fabric tables and remote tables
description: Data fabric tables are similar to remote tables on the ServiceNow AI Platform, but differ in how they connect to data and what write operations they support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/dft-vs-remote-tables.html
release: brazil
topic_type: concept
last_updated: "2026-11-11"
reading_time_minutes: 1
keywords: [data fabric tables vs remote tables, remote tables comparison]
breadcrumb: [Explore, Zero Copy Connectors, Workflow Data Fabric]
---

# Differences between data fabric tables and remote tables

Data fabric tables are similar to remote tables on the ServiceNow AI Platform, but differ in how they connect to data and what write operations they support.

Unlike remote tables, data fabric tables query external data sources using a zero copy connection instead of a script.

A data fabric table lets you view external data. You can't insert, update, or delete data in an external data source, as you can from a remote table.

