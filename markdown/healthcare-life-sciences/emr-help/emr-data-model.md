---
title: EMR Help data model
description: The EMR Help data model enables clinicians to submit service requests on your ServiceNow instance from an EMR system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/emr-help/emr-data-model.html
release: australia
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# EMR Help data model

The EMR Help data model enables clinicians to submit service requests on your ServiceNow instance from an EMR system.

The EMR Help data model accesses only the EMR system data required to make the EMR Help application work.

The following diagram shows the tables and their columns, and the relationships between each table, that comprise the EMR Help data model.

\[Omitted image "emr-help-data-model.png"\] Alt text: Data model displaying how the tables within EMR Help interact.

The EMR Help data model uses a combination of tables to store data:

-   ServiceNow AI Platform task tables such as the Incident \[incident\] table or Healthcare Case \[sn\_hcls\_case\].
-   Tables included with the EMR Help application:
    -   [Remote request definition table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/emr-help/emr-remote-request-definition.md)
    -   [Remote request parameter table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/emr-help/emr-remote-request-parameter.md)
    -   [Remote request data table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/emr-help/emr-remote-request-data.md)
    -   [EMR Request Data table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/emr-help/emr-emr-incident-data.md)
    -   [Request configuration mapping table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/emr-help/emr-request-configuration-mapping.md)

