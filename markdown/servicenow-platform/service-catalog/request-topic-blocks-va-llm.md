---
title: Request catalog item through Now LLM
description: You can design a topic conversation in Virtual Agent powered Now LLM by including reusable topic blocks to perform request submission tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/request-topic-blocks-va-llm.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [LLM topic blocks, Conversational Catalog Requests reference, Conversational Catalog Requests, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Request catalog item through Now LLM

You can design a topic conversation in Virtual Agent powered Now LLM by including reusable topic blocks to perform request submission tasks.

You can use this topic block to request for a catalog item through a conversational and streamlined experience based on generative AI. For information about configuring ServiceNow Otto in conversational catalog request, see [Configure ServiceNow Otto in Conversational Catalog Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-gen-ai-catalog-item.md).

|Parameter|Description|
|---------|-----------|
|catalog\_item\_id|sys\_id of the catalog item that should be requested.|
|context\_json|Context of the conversation in JSON format.|
|execute\_contextual\_search|Option to specify if the contextual search should be run for a record producer based on its configuration. For information on defining contextual search for a record producer, see [Define contextual search for record producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CntxtSearchRP.md).|
|confirm\_catalog\_item|Option to specify whether the user must confirm the catalog item before continuing with the next step. If this is set to `false`, user can answer the catalog items questions by skipping the confirmation.|
|show\_end\_state\_card|Option to display the end state card information about the generated record to the user.|

<table id="table_jrd_dvg_lzb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

record\_id

</td><td>

sys\_id of the record that is generated after the item submission.If the catalog item is not supported in the conversation mode or if the user does not have access to the item, -1 is returned.

</td></tr><tr><td>

record\_table

</td><td>

Name of the table in which the record is generated.

</td></tr><tr><td>

status

</td><td>

Status of the request. Possible options are success or error.

</td></tr><tr><td>

variables

</td><td>

Questions related to the catalog item.

</td></tr><tr><td>

message

</td><td>

Message that gives additional information in case of any failure.

</td></tr><tr><td>

used\_LLM

</td><td>

Option that indicates if Now LLM was used while requesting the item, that is, if slot filling was done for questions defined in a catalog item using generative AI.

</td></tr></tbody>
</table>**Parent Topic:**[LLM topic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/llm-topic-blocks-reference.md)

**Related topics**  


[Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md)

[Catalog builder preview topic conversation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/catalog-builder-preview-topic.md)

[Now LLM Service updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-llm-model-updates.md)

