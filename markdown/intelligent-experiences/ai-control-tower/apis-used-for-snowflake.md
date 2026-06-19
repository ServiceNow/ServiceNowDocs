---
title: Snowflake Statements API Reference
description: The connector uses the Snowflake Statements API to query AI assets and usage data. The following queries are executed during discovery and usage collection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/apis-used-for-snowflake.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [Snowflake, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# Snowflake Statements API Reference

The connector uses the Snowflake Statements API to query AI assets and usage data. The following queries are executed during discovery and usage collection.

## Asset Discovery Queries

<table id="table_a4q_gdt_mjc"><tbody><tr><td>

Query

</td><td>

Description

</td></tr><tr><td>

Show Accounts

</td><td>

Retrieves a list of all Snowflake accounts accessible with the provided credentials.

</td></tr><tr><td>

Show Agents

</td><td>

Discovers all AI agents configured in your Snowflake account.

</td></tr><tr><td>

Describe Agent

</td><td>

Retrieves comprehensive metadata for a specific agent, including configuration, capabilities, and runtime parameters.

</td></tr><tr><td>

Query Model Versions

</td><td>

Retrieves detailed version history and metadata for AI models from the information schema.

</td></tr><tr><td>

Describe Model

</td><td>

Fetches comprehensive model metadata including type, ownership, version information, and configuration.

</td></tr><tr><td>

Describe Fine-Tuning Job

</td><td>

Retrieves status, metrics, and output details for completed fine-tuning jobs.

</td></tr></tbody>
</table>## Usage Analytics Query

The connector queries the SNOWFLAKE.LOCAL.AI\_OBSERVABILITY\_EVENTS table to collect AI agent usage data.

This query analyzes usage within a specified time window and returns the following data:

-   Session IDs
-   Agent names
-   Users
-   Database and schema names
-   Request counts

