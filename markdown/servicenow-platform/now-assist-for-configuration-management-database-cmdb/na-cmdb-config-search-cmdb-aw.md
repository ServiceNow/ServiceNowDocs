---
title: Configure the Search CMDB agentic workflow
description: Review and configure the settings of the Search CMDB agentic workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-config-search-cmdb-aw.html
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the Search CMDB agentic workflow

Review and configure the settings of the Search CMDB agentic workflow.

## Before you begin

The **Index All Tables** and **Index Selected Table/s** actions require the ais\_admin role, which the sn\_query\_gen.admin role includes.

Role required: sn\_query\_gen.admin

## Procedure

1.  Activate the Query Generation skills as described in [Query Generation skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/enable-query-generation.md).

2.  Navigate to **Query Generation** &gt; **Indexed Sources**.

3.  Open the **Query Generation Entity Source** record.

4.  Select **Index All Tables** or **Index Selected Table/s**.

    The Indexed Source History page appears with a message that the indexed source is queued for indexing.

5.  Repeat step 4 for the **Query Generation Dimension Source** record.


## What to do next

To monitor the progress of an indexing task, refresh the Indexed Source History page. When the **Ingestion State** field shows **indexed**, indexing is complete. If the field shows **cancelled** or **error**, indexing didn't complete successfully.

**Parent Topic:**[Configuring ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configuring.md)

**Related topics**  


[Use ServiceNow Otto to search the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-search.md)

