---
title: Pass multivalued properties with an Exchange activity
description: To set a multivalued property using an Exchange activity, you must use a specific parameter format.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exchange activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Pass multivalued properties with an Exchange activity

To set a multivalued property using an Exchange activity, you must use a specific parameter format.

## About this task

The Optional parameters shared input variable allows you to set [multivalued properties](http://technet.microsoft.com/en-us/library/bb684908%28v=exchg.150%29.aspx).

## Procedure

-   To set a multivalued property, replacing any existing values, use this format: "`PropertyName`":"\(`value1`, `value2`, `value3`\)"

-   To add values, use this format: "PropertyName":"+\(`value1`, `value2`, `value3`\);"

-   To remove values, use this format: "PropertyName":"-\(`value1`, `value2`, `value3`\);"

-   To both add and remove values, use this format: "PropertyName":"-\(`value1`, `value2`, `value3`\);+\(`value1`, `value2`, `value3`\);"


**Parent Topic:**[Exchange activity pack](../concept/c_OrchestrationExchangeActivities.md)

