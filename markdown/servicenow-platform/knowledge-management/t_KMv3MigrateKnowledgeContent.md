---
title: Knowledge content migration from v2 to v3
description: To use the new functionality available in knowledge v3 with legacy articles, you must migrate these articles out of the default knowledge base.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge content migration from v2 to v3

To use the new functionality available in knowledge v3 with legacy articles, you must migrate these articles out of the default knowledge base.

To migrate knowledge content, move articles out of the default knowledge base by changing the **Knowledge Base** value for each article. The state of the article remains unchanged when moving articles. After selecting a new knowledge base, assign a category to each article using the category structure defined in the new knowledge base.

After you migrate a knowledge article, the legacy feedback functionality is automatically replaced with the new knowledge feedback mechanisms. Legacy feedback is copied to the Live Feed Message \[live\_message\] table to ensure previously submitted feedback is available for knowledge v3 articles.

