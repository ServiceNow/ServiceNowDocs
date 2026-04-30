---
title: Defining Approval Rules
description: To define a new approval rule, navigate to Managed Documents Administration Approval Rules and click New.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Defining Document Parameters, Features, Managed Documents, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Defining Approval Rules

To define a new approval rule, navigate to **Managed Documents** &gt; **Administration** &gt; **Approval Rules** and click **New**.

|Field|Description|
|-----|-----------|
|Name|A unique identifier for the approval rule.|
|Active|A check box indicating whether this approval rule is used.|
|Condition|A condition builder that determines which documents use this approval rule.|
|Description|A short description of the approval rule.|

Once the approval rule is saved, the **Approvers** related list defines which approvers are added if the conditions in the **Condition** field are met.

The following approval rules are available in the base system.

|Name|Condition|
|----|---------|
|Internal policy|type=Policy ^ audience=Internal|
|Development policy|type=Policy ^ department=Development|

**Parent Topic:**[Defining Document Parameters](r_DefiningDocumentParameters.md)

**Related topics**  


[Defining Document Parameters](r_DefiningDocumentParameters.md)

