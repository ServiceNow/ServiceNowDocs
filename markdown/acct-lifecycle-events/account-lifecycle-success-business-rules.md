---
title: Customer success business rules
description: This section includes the customer success business rules.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Account Lifecycle Events reference, Account Lifecycle Events]
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

**Parent Topic:**[Account Lifecycle Events reference](account-lifecycle-reference.md)

