---
title: Default state field policies in base system change models
description: The Change Management - Change Model Foundation Data plugin \(com.snc.change\_management.change\_model.foundation\) includes state field policies for the base system change models. All default policies make fields mandatory only.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/default-state-field-policies.html
release: brazil
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 1
keywords: [default state field policies, change model, mandatory fields, base system, change request]
breadcrumb: [State field policies for change models, Create a Change model, Configure, Change Management, IT Service Management]
---

# Default state field policies in base system change models

The Change Management - Change Model Foundation Data plugin \(com.snc.change\_management.change\_model.foundation\) includes state field policies for the base system change models. All default policies make fields mandatory only.

To view, edit, or deactivate these policies, go to the **State Field Policies** related list on the model state record. To add or modify policies, see [Add state field policies to a change model state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/define-state-field-policies.md).

|State|Mandatory fields|
|-----|----------------|
|Normal|
|Assess|**Assignment group**|
|Authorize|**Assignment group**|
|Scheduled|**Assignment group**|
|Implement|**Assignment group**|
|Review|**Assignment group**|
|Closed|**Assignment group**, **Close code**, **Close notes**|
|Standard|
|Scheduled|**Assignment group**|
|Implement|**Assignment group**|
|Review|**Assignment group**|
|Closed|**Assignment group**, **Close code**, **Close notes**|
|Emergency|
|Authorize|**Assignment group**|
|Scheduled|**Assignment group**|
|Implement|**Assignment group**|
|Review|**Assignment group**|
|Closed|**Close code**, **Close notes**|
|Unauthorized Change|
|Review|**Assignment group**|
|Authorize|**Assignment group**, **Configuration item**, **Short description**, **Description**|
|Closed|**Assignment group**, **Close code**, **Close notes**|
|Change Registration|
|Review|**Assignment group**|
|Closed|**Assignment group**, **Description**, **Close code**, **Close notes**|
|Canceled|**Description**|
|Cloud Infrastructure|
|Authorize|**Assignment group**|
|Closed|**Configuration item**, **Short description**, **Planned start date**, **Planned end date**, **Close code**, **Close notes**|

**Parent Topic:**[State field policies for change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/state-field-policies-change-models.md)

**Related topics**  


[State field policies for change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/state-field-policies-change-models.md)

[Add state field policies to a change model state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/define-state-field-policies.md)

