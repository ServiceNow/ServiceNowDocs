---
title: Customer success business rules
description: This section includes the customer success business rules.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Customer Success Management reference, Customer Success Management]
---

# Customer success business rules

This section includes the customer success business rules.

|Business rule|Table|Description|
|-------------|-----|-----------|
|Domain - Set Domain|Engagement|Sets the domain information.|
|Required fields for engagement|Engagement|Validates required fields.|
|State is closed or canceled|Engagement|Ensures closure information is populated and object is marked inactive before marking it as closed or canceled.|
|Engagement is reopened|Engagement|Ensures closure information is removed and object is marked active before reopening.|
|Validate account change for engagement|Engagement|Prevent account change if the engagement has objectives, success cases, internal plays, or risk signals associated with it.|
|Validate engagement parent|Engagement|Prevent cyclic relationship for the parents in engagement hierarchy.|
|Validate onboarding for engagement|Engagement|Ensures the engagement account matches the account of its onboarding case and sets the go live date based on the go live date of its onboarding case.|
|Domain - Set Domain|Success objective|Sets the domain information.|
|Required fields for objective|Success objective|Validates required fields|
|Validate closure for objective|Success objective|Ensures closure information is populated and object is marked inactive before marking closed/canceled.|
|Success objective is reopened|Success objective|Ensures closure information is removed and object is marked active before reopening.|
|Validate engagement change for objective|Success objective|Prevents engagement change if the objective has outcomes or risk signals associated with it.|
|Validate planned start and stop|Success objective|Ensures planned stop date is not before planned start date.|
|Domain - Set Domain|Success outcome|Sets the domain information.|
|Required fields for outcome|Success outcome|Validates required fields.|
|Validate closure for outcome|Success outcome|Ensures closure information is populated and object is marked inactive before marking it as closed or canceled.|
|Success outcome is reopened|Success outcome|Ensures closure information is removed and object is marked active before reopening.|
|Validate objective change for outcome|Success outcome|Prevents objective change if the outcome has initiatives or risk signals associated with it.|
|Validate planned dates|Success outcome|Ensures planned stop date is not before planned start date.|
|Validate tracking method|Success outcome|Validates tracking method to see if the correct reference field for tracking is populated.|
|Required fields for initiative|Success initiative|Validates required fields.|
|Validate closure for initiative|Success initiative|Ensures closure information is populated and object is marked inactive before marking it as closed or canceled.|
|Success initiative is reopened|Success initiative|Ensures closure information is removed and object is marked active before reopening.|
|Validate outcome change for initiative|Success initiative|Prevents outcome change if the initiative has success tasks or risk signals associated with it.|
|After close or cancel SI|Success initiative|Cancels process automation playbooks associated with initiative if closed or canceled.|
|Required fields for success case|Success case|Validates required fields.|
|Validate closure for success case|Success case|Ensures closure information is populated and object is marked inactive before marking it as closed or canceled.|
|Success case is reopened|Success case|Ensures closure information is removed and object is marked active before reopening.|
|Validate engagement update|Success case|Prevents engagement change if the success case has success tasks or risk signals associated with it.|
|Required fields for touchpoint|Touchpoint|Validates required fields.|
|Validate closure for touchpoint|Touchpoint|Ensures closure information is populated and object is marked inactive before marking it as closed or canceled.|
|Touchpoint is reopened|Touchpoint|Ensures closure information is removed and object is marked active before reopening.|
|Validate engagement update|Touchpoint|Prevents engagement change if the touchpoint has success tasks or risk signals associated with it.|
|Required fields for success task|Success task|Validates required fields.|
|Validate closure for success task|Success task|Ensures closure information is populated and object is marked inactive before marking it as closed or canceled.|
|Success task is reopened|Success task|Ensures closure information is removed and object is marked active before reopening|
|Validate parent change for success task|Success task|Prevents parent change if the success task has risk signals associated with it.|
|Required fields for internal play|Internal play|Validates required fields.|
|Internal play is closed or canceled|Internal play|Ensures closure information is populated and object is marked inactive before marking it as closed or canceled.|
|Reopen internal play|Internal play|Ensures closure information is removed and object is marked active before reopening.|
|Parent for internal play must be empty|Internal play|Ensures parent is empty for all internal plays.|
|Validate engagement change|Internal play|Prevents engagement change if the internal play has internal play tasks or risk signals associated with it.|
|Required fields for internal play task|Internal play task|Validates required fields.|
|Internal play task is closed or canceled|Internal play task|Ensures closure information is populated and object is marked inactive before marking it as closed or canceled.|
|Reopen internal play task|Internal play task|Ensures closure information is removed and object is marked active before reopening.|
|Validate internal play change|Internal play task|Prevents internal play change if the internal play task has risk signals associated with it.|
|Domain - Set Domain|Risk signal and issue|Sets the domain information.|
|Field validation|Risk signal and issue|Validates required fields.|
|Validate risk signal closure|Risk signal and issue|Ensures closure information is populated and object is marked inactive before marking it as closed or canceled.|
|Reopen risk signal|Risk signal and issue|Ensures closure information is removed and object is marked active before reopening|
|Avoid duplicate definition record|Definition record|Ensures the no two records share the same title and category.|
|Domain - Set Domain|Definition record|Sets the domain information.|
|Set active flag|Definition record|Sets status to active if published, else inactive.|
|Avoid duplicate risk signal solution|Risk signal solution relationship|Ensures the no two records share the same solution record.|
|Avoid duplicate squad member|Squad member|Ensures the no two records share the same user and responsibility|
|Domain - Set Domain|Squad member|Sets the domain information.|
|Avoid duplicate engagement to contract relationship|Engagement to contract relationship|Ensures the no two records share the same engagement and contract.|
|Validate contract account|Engagement to contract relationship|Ensures contract account matches the engagement account.|
|Contract relationship updated|Engagement to contract relationship|Ensures renewal date for engagement is updated to the date of the earliest non expired contract.|
|Contract relationship removed|Engagement to contract relationship|Ensures renewal date for engagement is updated to the date of the earliest non expired contract.|
|Validate context on publish|Data Source|When publishing a data source, it needs to have at least one valid context record, which should have at least one context mapper record associated.|
|Avoid duplicate data source|Data Source|Data source should not have duplicate source and configurations.|
|Autopopulate unit of measurement|Data Source|Automatically populated unit of measurement for data source.|
|Last run/Next run validation|Data Source|Data source last run date should not come after next run date.|
|Unique source to context|Context Engine Mapper|Ensure there is an unique source to context.|
|Process externally sourced context data|Context Engine Data|When creating a data record for external source, update associated data source date last run field and populate data record's context field.|
|Validate externally sourced context data|Context Engine Data|Context engine date records with external source should have all required fields.|
|Unique context per source|Context|Context record's mappers should be unique.|
|Abort if duplicate record found|Engagement Risk Definition|Aborts if similar record already exists|
|Abort if invalid template|Engagement Risk Definition|Aborts if risk template set for the risk definition is invalid|
|Abort if duplicate record found|Risk Threshold Override|Aborts if similar record already exists|
|Abort if no context mapper for risk def|Engagement Risk Definition|Aborts if risk definition is table type and no active mapper exists with the table selected in risk definition as the source and engagement as context|
|Abort if color or range validation fails|Color Banding|Aborts if duplicate color exists for a record of the same type or max value is lesser than min value or if the given min-max range already overlaps with another existing record of the same type.|
|Abort if global min-max range is invalid|Color Banding|Aborts if global band has min less than 0 and max greater than 100|
|Limit \# of global health definition to 1|Engagement Health Definition|Ensures there is at most 1 global health definition in system|
|Unique engagement health definition|Engagement Health Definition|Ensures each health definition is unique|
|Validate sum of health def config weight|Engagement Health Definition|Checks all health definition metric configuration for a health definition sums to 100|
|Abort creation for published health def|Health Metric Configuration|User should not be able to create health metric configuration for published health definition|
|Check unique health metric configuration|Health Metric Configuration|Metric configuration for a health definition should not be duplicate by data source|
|Update last touchpoint|Touchpoint|Update last\_touchpoint field in engagement table|
|Update last touchpoint for Delete|Touchpoint|Update last\_touchpoint field in engagement table|
|Avoid duplicate entitlements|Applicable Entitlement|Aborts if similar record already exists|
|Avoid duplicate sold product|Applicable Sold Product|Aborts if similar record already exists|
|Avoid duplicate customer team|Applicable Customer Team|Aborts if similar record already exists|
|Avoid duplicate account team|Applicable Account Team|Aborts if similar record already exists|

**Parent Topic:**[Customer Success Management reference](account-lifecycle-reference.md)

