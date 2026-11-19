---
title: Virtual Agent feedback data tables
description: Locations where ServiceNow Otto for Virtual Agent stores the requests and feedback that users give on responses, including the tables that hold the data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/now-assist-in-virtual-agent/virtual-agent-feedback-analysis-dashboard.html
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: reference
last_updated: "2026-11-16"
reading_time_minutes: 1
breadcrumb: [ServiceNow Otto for Virtual Agent reference, ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Virtual Agent feedback data tables

Locations where ServiceNow Otto for Virtual Agent stores the requests and feedback that users give on responses, including the tables that hold the data.

The Virtual Agent Feedback Analysis dashboard reports on requests and feedback stored in the Now Assist analytics tables. For information about accessing the dashboard, its requirements, and its widgets, see [Analyze response feedback on Virtual Agent responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/analyze-response-feedback-on-virtual-agent-responses.md).

## Where feedback is stored

The `sn_nowassist_va.analytics.persistence_strategy` system property determines where feedback is written. For more information about this property, see [ServiceNow Otto for Virtual Agent system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/nava-sys-props.md).

|Value|Where feedback is written|
|-----|-------------------------|
|`event`|The legacy CI Analytics \[sys\_ci\_analytics\] table. The dashboard doesn't report on feedback written only to this table.|
|`table`|The Now Assist analytics tables listed in the following table.|
|`both`|Both the legacy table and the Now Assist analytics tables.|

|Table|Contents|
|-----|--------|
|Now Assist Request \[sys\_now\_assist\_request\]|User requests.|
|Now Assist Response Item \[sys\_now\_assist\_response\_item\]|Responses returned to users.|
|Now Assist Feedback \[sys\_now\_assist\_feedback\]|The rating for each response item and the optional free-text comment that the user enters.|
|Now Assist Granular Feedback \[sys\_now\_assist\_granular\_feedback\]|The reasons that users select and that are linked to a feedback record. A single rating can have more than one reason.|

## Related information

For more information about configuring the feedback options that users see, see [Configure response feedback](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/nava-configure-response-feedback-manually.md). For more information about accessing the stored feedback data, see [Granular Feedback and Analytics in ServiceNow Otto for Virtual Agent \(KB3060968\)](https://support.servicenow.com/kb_view.do?sysparm_article=KB3060968).

