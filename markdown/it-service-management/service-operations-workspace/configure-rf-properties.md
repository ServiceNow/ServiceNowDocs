---
title: Configure Recommendation Framework for an incident in Service Operations Workspace
description: Enable recommendations at field level or from the contextual sidebar for an incident in Service Operations Workspace.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up Recommendation Framework in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure Recommendation Framework for an incident in Service Operations Workspace

Enable recommendations at field level or from the contextual sidebar for an incident in Service Operations Workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Recommendation Framework** &gt; **Administration** &gt; **Recommendation Properties**.

2.  From the Recommendation Properties page, configure the recommendation framework settings.

    |Property|Description|
    |--------|-----------|
    |Activate/Deactivate Recommendation Rule|
    |Assignment group recommendation for Incident|Enables the field-level recommendation for the **Assignment group** field of an incident.|
    |Configuration item recommendation for Incident|Enables the field-level recommendation for the **Configuration item** field of an incident.|
    |Knowledge articles for Incident|Enables the **Knowledge articles** card when you access recommendations from the sidebar.|
    |Propose major incident for Incident|Enables the **Propose major incident** card when you access recommendations from the sidebar.|
    |Relevant problems for Incident|Enables the **Relevant problems** card when you access recommendations from the sidebar.|
    |Service recommendation for Incident|Enables the field-level recommendation for the **Service** field of an incident.|
    |Similar major incidents for Incident|Enables the **Similar major incidents** card when you access recommendations from the sidebar.|
    |Similar open incidents for Incident|Enables the **Similar open incidents** card when you access recommendations from the sidebar.|
    |Similar resolved incidents for Incident|Enables the **Similar resolved incidents** card when you access recommendations from the sidebar.|
    |Set threshold value for field level stamping|
    |Assignment group recommendation for Assignment group|Threshold value for auto-populating a recommendation in the **Assignment group** field. When the prediction value is greater than or equal to the specified threshold value, the recommendation is auto-populated as the field value.|
    |Configuration item recommendation for Configuration item|Threshold value for auto-populating a recommendation in the **Configuration item** field. When the prediction value is greater than or equal to the specified threshold value, the recommendation is auto-populated as the field value.|
    |Service recommendation for Service|Threshold value for auto-populating a recommendation in the **Service** field. When the prediction value is greater than or equal to the specified threshold value, the recommendation is auto-populated as the field value.|

    For information on recommendation rules, see [Recommendation rules for an incident in Service Operations Workspace](../reference/recommendation-rules.md).

3.  Click **Save**.


**Parent Topic:**[Setting up Recommendation Framework in Service Operations Workspace](../concept/set-up-recommendation-framework-sow.md)

