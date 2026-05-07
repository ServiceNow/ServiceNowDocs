---
title: AI Service Graph Connector for Snowflake
description: Use the  AI Service Graph Connector for Snowflake to create AI connections to discover and import AI assets such as AI systems, agents, models, prompts, tools, and datasets as well as usage data for these AI assets into AI Control Tower. This usage information is consumed by the AI Control Tower's value dashboard.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for Snowflake

Use the  AI Service Graph Connector for Snowflake to create AI connections to discover and import AI assets such as AI systems, agents, models, prompts, tools, and datasets as well as usage data for these AI assets into AI Control Tower. This usage information is consumed by the AI Control Tower's value dashboard.

## Download apps from the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to download the AI Service Graph Connector for Hugging Face app.

## Supported ServiceNow versions

-   Australia
-   Zurich

## User role

-   sn\_ai\_disc.discovery\_admin
-   sn\_cmdb\_int\_util.sgc\_admin

## Prerequisites

Steps to be performed in the Snowflake environment.

**Note:** The Outbound-integration IP addresses for the instance should be allowed in the Snowflake.

The Snowflake statements API does not support non-LDF characters in the API URL. This is a Snowflake API limitation. As a workaround, use the account\_locator in place of the account\_identifier. When configuring the connection, use the following format for connection url.

`https://<account_locator>.snowflakecomputing.com`

rather than:

`https://<account_identifier>.snowflakecomputing.com`

