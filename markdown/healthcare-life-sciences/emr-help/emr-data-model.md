---
title: EMR Help data model
description: The EMR Help data model enables clinicians to submit service requests on your ServiceNow instance from an EMR system.
locale: en-US
release: yokohama
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring EMR Help, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# EMR Help data model

The EMR Help data model enables clinicians to submit service requests on your ServiceNow instance from an EMR system.

The EMR Help data model accesses only the EMR system data required to make the EMR Help application work.

The following diagram shows the tables and their columns, and the relationships between each table, that comprise the EMR Help data model.

![Data model displaying how the tables within EMR Help interact.](../image/emr-help-data-model.png "EMR Help data model")

The EMR Help data model uses a combination of tables to store data:

-   ServiceNow AI Platform task tables such as the Incident \[incident\] table or Healthcare Case \[sn\_hcls\_case\].
-   Tables included with the EMR Help application:
    -   [Remote request definition table](emr-remote-request-definition.md)
    -   [Remote request parameter table](emr-remote-request-parameter.md)
    -   [Remote request data table](emr-remote-request-data.md)
    -   [EMR Request Data table](emr-emr-incident-data.md)
    -   [Request configuration mapping table](emr-request-configuration-mapping.md)

