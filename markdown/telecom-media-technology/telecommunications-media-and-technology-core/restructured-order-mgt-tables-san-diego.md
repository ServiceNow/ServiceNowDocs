---
title: Restructured Order Management tables
description: The table architecture that supports the Order Management for Telecommunications, Media, and Technology application has been restructured. Existing customers who upgraded from earlier releases to the San Diego release must first run a Post upgrade Script to reparent the order tables and then perform column promotions.OM revamp project - This topic is obsolete and has been removed from the SOM bundle on Oct 27, 2025.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/restructured-order-mgt-tables-san-diego.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Approve or reject a customer order, Customer orders, Use, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Restructured Order Management tables

The table architecture that supports the Order Management for Telecommunications, Media, and Technology application has been restructured. Existing customers who upgraded from earlier releases to the San Diego release must first run a Post upgrade Script to reparent the order tables and then perform column promotions.

Before you use Order Management for Telecommunications, Media, and Technology \(2.0.0\), you must run the Post Upgrade Script after your upgrade to San Diego. For detailed information about this script, see the [Order Management for Telecommunications, Media, and Technology \(2.0.0\) version: Post upgrade reparenting script for the San Diego release \[KB1000941\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1000941) article in the Now Support Knowledge Base.

**Note:** If you don't run this script to perform table reparenting and column promotion, the order decomposition and order fulfillment functions don't work as designed. In these cases, the following error message appears after the approval of an order:

```
Some of the OMT tables need reparenting. Please contact system administrator to execute the reparenting script.
```

By using the [Now Support Portal](https://support.servicenow.com/now?id=ns_automation_store&catalog_sys_id=891f088e465667e234a3cb52ffa1d299), raise a new Case with the Technical Support team to assist you in applying these changes.

