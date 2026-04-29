---
title: Service recommendations for interactions
description: Recommend the most relevant services to an agent based on the context of an interaction record, such as the short description or description.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service definitions, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Service recommendations for interactions

Recommend the most relevant services to an agent based on the context of an interaction record, such as the short description or description.

With Service recommendations for interactions, agents can see the recommended services in the case type selector based on the information provided in the interaction record.

**Note:** The service recommendations for interactions feature requires the Now Assist for Customer Service Management \(CSM\) application.

The system displays the recommended services in a separate section at the top of the case type selector. By default, this section shows a maximum of four recommended services. The number of recommended services that can be displayed is controlled by the **sn\_csm\_case\_types.top\_ai\_predictions\_limit** system property.

![Case type selector with the Top AI Predictions section that displays cards for AI predicted services based on the interaction context](../image/case-type-selector-ai-predictions.png "Case type selector with Top AI Predictions")

## Service recommendations for interactions properties

The Service recommendations for interactions feature includes the following properties.

<table id="table_kly_4dc_4fc"><thead><tr><th>

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_csm\_case\_types.top\_ai\_predictions\_enabled

</td><td>

Enables AI predictions for services and displays those services in the case type selector.-   **Type**: true\|false
-   **Value**: true
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_csm\_case\_types.top\_ai\_predictions\_limit

</td><td>

Sets the maximum number of AI predicted services to display in the case type selector.-   **Type**: integer
-   **Value**: 4
-   **Location**: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>**Related topics**  


[Configure service recommendations for interactions](../task/configure-service-recommendations-int.md)

[Create a case based on service definition recommendations](../task/use-service-definition-rec.md)

