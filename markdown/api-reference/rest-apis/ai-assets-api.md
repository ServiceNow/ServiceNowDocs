---
title: AI Assets API
description: AI Assets API provides endpoints to retrieve, update, and create several types of AI assets, such as systems, data sets, prompts, and models.Retrieves the data of the specified AI dataset asset.Retrieves the data of the specified AI model asset.Retrieves the data of the specified AI prompt asset.Retrieves the data of the specified AI system asset.Creates a new AI dataset asset entry in the AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\] and AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] according to details you provide in the request body.Creates a new AI prompt asset entry in the AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\] and AI Prompt Product Model \[cmdb\_ai\_promt\_product\_model\] tables according to details you provide in the request body.Creates a new AI model asset entry in the AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\] and AI Model Product Model \[cmdb\_ai\_model\_product\_model\] tables according to details you provide in the request body.Creates a new AI system asset entry in the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] and AI System Product Model \[cmdb\_ai\_system\_product\_model\] tables according to details you provide in the request body.Updates the data of a specific AI dataset asset record according to information that you provide in the request body.Updates the data of a specific AI prompt asset record according to information you provide in the request body.Updates the data of a specific AI system record according to information you provide in the request body.Updates the data of a specific AI model asset record according to information you provide in the request body.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 82
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# AI Assets API

AI Assets API provides endpoints to retrieve, update, and create several types of AI assets, such as systems, data sets, prompts, and models.

The AI Assets API supports actions that you can perform on AI Asset records in the Expanded Model and Asset Classes application. It requires the Asset Classes \(sn\_ent\) plugin to access it. You must have the asset and model\_manager roles to call the endpoints provided by the AI Assets API.

**Note:** The data included in AI Asset records may be spread across several tables like Product Model, Configuration Item, and others. To reduce complexity when calling this API, however, the AI Assets API inserts data into only the Asset, Product Model and Configuration Item tables. Specifics about table updates are provided under each endpoint.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## AI Assets API - GET /sn\_ent/asset/ai\_dataset/\{sys\_id\}

Retrieves the data of the specified AI dataset asset.

### URL format

Versioned URL: `/api/sn_ent/{api_version}/asset/ai_dataset/{sys_id}`

Default URL: `/api/sn_ent/asset/ai_dataset/{sys_id}`

### Supported request parameters

<table id="table_ksp_xkw_5dc" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the asset in the AI Dataset Asset \[alm\_ai\_dataset\_digital\_asset\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. Failed to fetch the asset with the given sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="table_ssp_xkw_5dc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details of the newly created AI Dataset asset.Data type: Object

```
"result": {
  "acceptable_usage": {Object},
  "base_datasets": [Array],
  "created": "String",
  "dataset_card": "String",
  "data_type": {Object},
  "description": "String",
  "documentation": "String",
  "display_name": "String",
  "managed_by": {Object},
  "name": "String",
  "provider": {Object},
  "state": "Development",
  "source": "String",
  "sys_id": "String",
  "updated": "String",
  "version": "String",
}
```

</td></tr><tr><td>

result.acceptable\_usage

</td><td>

Acceptable usage for the AI Dataset Asset record. Acceptable usage refers to how a dataset or model can be used, typically for training or evaluation purposes.Data type: Object

```
"acceptable_usage": {
  "label": "String" 
  "value": "String" 
}
```

</td></tr><tr><td>

result.acceptable\_usage.label

</td><td>

Display label of the acceptable usage value.Data type: String

</td></tr><tr><td>

result.acceptable\_usage.value

</td><td>

Number value of the acceptable usage.Valid values:

-   1: Training
-   2: Evaluation

Data type: String

</td></tr><tr><td>

result.base\_datasets

</td><td>

Comma-separated list of base datasets required to build the given dataset. Accepts the name or sys\_id of a base data set in the AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\] table.Data type: Array

```
"base_datasets": ["String", "String"]
```

</td></tr><tr><td>

result.created

</td><td>

Date and time that the AI Dataset Asset record was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.data\_type

</td><td>

The type of data present in the AI Dataset Asset record.Data type: Object

```
"data_type": {
  "label": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.data\_type.label

</td><td>

The display label for the data type value.Data type: String

</td></tr><tr><td>

result.data\_type.value

</td><td>

Value of the dataset asset's data type.Data type: String

</td></tr><tr><td>

result.dataset\_card

</td><td>

The data set card. A dataset\_card is a metadata document that describes the contents, structure, and context of an AI dataset. It provides details like data sources, features, intended use, and any known limitations to ensure proper understanding and usage.Data type: String

</td></tr><tr><td>

result.description

</td><td>

Description of the associated AI Dataset Product Model record.Table: AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\]

Data type: String

</td></tr><tr><td>

result.display\_name

</td><td>

Display name of the AI Dataset Asset record.Table: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.documentation

</td><td>

Documentation of the associated AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.managed\_by

</td><td>

Details about the user who manages the AI Dataset Asset record.Data type: Object

```
"managed_by": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.managed\_by.name

</td><td>

Name of the user who manages the AI Dataset Asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.managed\_by.sys\_id

</td><td>

Sys\_id of the user who manages the AI Dataset Asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.name

</td><td>

Name of the associated AI Dataset Product Model record.Table: AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\]

Data type: String

</td></tr><tr><td>

result.provider

</td><td>

Provider of the associated AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table record.Data type: Object

```
provider: {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.provider.name

</td><td>

Name of the provider.Data type: String

</td></tr><tr><td>

result.provider.sys\_id

</td><td>

Sys\_id of the provider in the associated AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.source

</td><td>

Details about the source of AI dataset asset.Valid values:

-   Link to the source of the dataset asset.
-   Details \(in plain text\) of the source of the dataset asset. For example, the name of a product or website.

Data type: String

Default: empty or null

</td></tr><tr><td>

result.state

</td><td>

State of the AI Dataset Asset record.Possible values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the AI Dataset Asset record.Table: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.updated

</td><td>

Date and time that the AI Dataset Asset record was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.version

</td><td>

Version number of the associated AI Dataset Product Model record. For example, `V2`.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example.

```
curl "https://instance.servicenow.com/api/sn_ent/asset/ai_dataset/ cc419cb2331e92101c9aca989d5c7b4c" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user "username":"password"
```

Output:

```
{ 
  "result": { 
    "sys_id": "9d60fb5f40d21210f877b00c113d1fea", 
    "display_name": "ServiceNow Closed Incidents v1", 
    "name": "Closed Incidents", 
    "description": "Incidents with resolution", 
    "documentation": "Sample Documentation", 
    "source": "incident table on servicenow instance", 
    "dataset_card": "Sample Dataset Card", 
    "state": "Development", 
    "version": "v1", 
    "data_type": { 
      "value": "2", 
      "label": "Image" 
    }, 
    "provider": { 
      "sys_id": "93d4ecfac0a8000b6294d71b733977fb", 
      "name": "ServiceNow" 
    }, 
    "managed_by": { 
      "sys_id": "62826bf03710200044e0bfc8bcbe5df1", 
      "name": "Abel Tuter" 
    }, 
    "acceptable_usage": { 
      "value": "1", 
      "label": "Training" 
    }, 
    "base_datasets": [], 
    "created": "2024-12-11 08:50:40", 
    "updated": "2024-12-11 08:50:40" 
  } 
}
```

## AI Assets API - GET /sn\_ent/asset/ai\_model/\{sys\_id\}

Retrieves the data of the specified AI model asset.

### URL format

Versioned URL: `/api/sn_ent/{api_version}/asset/ai_model/{sys_id}`

Default URL: `/api/sn_ent/asset/ai_model/{sys_id}`

### Supported request parameters

<table id="table_ksp_xkw_5dc" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the asset in the AI Model Asset \[alm\_ai\_model\_digital\_asset\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. Failed to fetch the asset with the given sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="table_vhh_n4g_zdc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details of the model asset record.Data type: Object

```
result: {
  "base_model": {Object},
  "context_window": "String",
  "created": "String",
  "deployment_guideline": "String",
  "description": "String",
  "display_name": "String",
  "documentation": "String",
  "evaluation_datasets": [Array],
  "evaluation_metrics_report": "String",
  "managed_by": {Object},
  "model_size_in_mb": "String",
  "name": "String",
  "parameters_info": "String",
  "provider": {Object},
  "required_infrastructure": "String",
  "source": "String",
  "state": Number,
  "supported_languages": [Array],
  "sys_id": "String",
  "training_datasets": [Array],
  "training_procedure": "String",
  "updated": "String",
  "version": "String"
}
```

</td></tr><tr><td>

result.base\_model

</td><td>

AI model that this model version was derived from.**Note:** Only applicable for models developed within the organization.

Data type: Object

```
{
  "name": "String",
  "sys_id": "String"
 }
```

Default:

</td></tr><tr><td>

result.base\_model.name

</td><td>

Name of the AI model asset to model this AI model after.Data type: String

</td></tr><tr><td>

result.base\_model.sys\_id

</td><td>

Sys\_id of the AI model asset to model this AI model after.Data type: String

</td></tr><tr><td>

result.context\_window

</td><td>

Size of input sequences \(in other words, the number of tokens\) that the model can handle.Data type: String represented with a number

</td></tr><tr><td>

result.created

</td><td>

Date and time that the AI Dataset Asset record was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.deployment\_guideline

</td><td>

Instructions applicable for models developed and deployed within an organization.Data type: String

</td></tr><tr><td>

result.description

</td><td>

Description to give the AI Model Product Model. Updated in table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

</td></tr><tr><td>

result.result.display\_name

</td><td>

Display name of the asset record.Data type: String

</td></tr><tr><td>

result.documentation

</td><td>

Documentation of the AI Prompt Product Model record.Table: AI Prompt Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

</td></tr><tr><td>

result.evaluation\_datasets

</td><td>

Comma-separated list of sys\_ids or display names of AI datasets of the AI Dataset Digital Asset used for evaluating the model. Mostly applicable for models developed within an organization.Tables: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\]

Data type: Array

```
"evaluation_datasets": [
  "name": "String",
  "sys_id": "String"
]
```

</td></tr><tr><td>

result.evaluation\_metrics\_report

</td><td>

Reference to the evaluation results.Possible values:

-   Details \(in plain text\) outlining results
-   Links to specific results

Data type: String

</td></tr><tr><td>

result.managed\_by

</td><td>

Details about the user who manages the AI Model Asset record.Data type: Object

```
"managed_by": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.managed\_by.name

</td><td>

Name of the user who manages the AI Dataset Asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.managed\_by.sys\_id

</td><td>

Sys\_id of the user who manages the AI Dataset Asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.model\_size\_in\_mb

</td><td>

Size of the model in MB. Mostly applicable for models developed and deployed within an organization.Data type: Number

</td></tr><tr><td>

result.name

</td><td>

Required. Name of the AI Model Product Model. Updated in table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

</td></tr><tr><td>

result.provider

</td><td>

Provider of the associated AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table record.Data type: Object

```
provider: {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.provider.sys\_id

</td><td>

Sys\_id of the provider in the associated AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.provider.name

</td><td>

Name of the provider.Data type: String

</td></tr><tr><td>

result.required\_infrastructure

</td><td>

Documentation of infrastructure needs for the model deployment. For example, details about the infrastructure stack and processing needs. Mostly applicable for models deployed within an organization.Data type: String

</td></tr><tr><td>

result.source

</td><td>

Details about the source of the model.Possible values:

-   Link to the source of the model. For example, `https://huggingface.co/mistralai/Mixtral-8x7B-Instruct-v0.1` or a link to Github.
-   Details of the source in plain text. For example, `Microsoft Azure`

Data type: String

</td></tr><tr><td>

result.state

</td><td>

State to apply to the AI Model Asset.Possible values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

result.supported\_languages

</td><td>

Languages that are supported by the AI Model.Data type: Array

```
"supported_languages": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.supported\_languages.name

</td><td>

Name of the Language record. For example, `"French", "English"`.Table: Language \[sys\_language\]

Data type: String

</td></tr><tr><td>

result.supported\_languages.sys\_id

</td><td>

Sys\_id of the Language record.Table: Language \[sys\_language\]

Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the AI model asset record.Table: AI Model Asset \[alm\_ai\_model\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.version

</td><td>

Version for AI Model Product Model. For example, `V2`.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example.

```
curl "https://instance.servicenow.com/api/sn_ent/asset/ai_model/cc419cb2331e92101c9aca989d5c7b4c" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Output:

```
{
  "result": {
    "sys_id": "a438d170ff96da10c1fbffffffffffd5",
    "display_name": "ServiceNow Now LLM V6",
    "name": "Now LLM",
    "description": "enables text-to-text like question answering and summarization",
    "version": "V6",
    "provider": {
      "sys_id": "93d4ecfac0a8000b6294d71b733977fb",
      "name": "ServiceNow"
    },
    "documentation": "Now LLM V5 Documentation",
    "parameters_info": "7B",
    "supported_languages": [
      {
        "sys_id": "914493a30f320010e96b0e4fef767e90",
        "name": "English"
      }
    ],
    "model_size_in_mb": "87",
    "deployment_guideline": "Deployed on ServiceNow infrastructure",
    "source": null,
    "training_procedure": "2",
    "context_window": "8000",
    "state": "Deployed",
    "required_infrastructure": "undefined",
    "base_model": {
      "sys_id": null,
      "name": ""
    },
    "evaluation_datasets": [
      {
        "sys_id": "45cb45baff06d610c1fbffffffffffa9",
        "name": "ServiceNow Open Incidents"
      }
    ],
    "training_datasets": [
      {
        "sys_id": "45cb45baff06d610c1fbffffffffffa9",
        "name": "ServiceNow Open Incidents"
      }
    ],
    "evaluation_metrics_report": "Testing results: See files attached to this record",
    "managed_by": {
      "sys_id": "62826bf03710200044e0bfc8bcbe5df1",
      "name": "Abel Tuter"
    },
    "created": "2024-12-03 16:50:53",
    "updated": "2024-12-03 16:50:53"
  }
}
```

## AI Assets API - GET /sn\_ent/asset/ai\_prompt/\{sys\_id\}

Retrieves the data of the specified AI prompt asset.

See also:

-   [AI Assets API - POST /sn\_ent/asset/ai\_prompt](ai-assets-api.md#)
-   [AI Assets API - PUT /sn\_ent/asset/ai\_prompt/\{sys\_id\}](ai-assets-api.md#)

### URL format

Versioned URL: `/api/sn_ent/{api_version}/asset/ai_prompt/{sys_id}`

Default URL: `/api/sn_ent/asset/ai_prompt/{sys_id}`

### Supported request parameters

<table id="table_ksp_xkw_5dc" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the asset in the AI Prompt Asset \[alm\_ai\_prompt\_digital\_asset\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. Failed to fetch the asset with the given sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="table_ijd_vrn_wdc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the AI Prompt Asset.```
result: {
  "ai_model": {Object},
  "created": "String",
  "description": "String",
  "display_name": "String",
  "documentation": "String",
  "managed_by": {Object},
  "name": "String",
  "prompt_info": "String",
  "provider": {Object},
  "state": Number,
  "sys_id": "String",
  "updated": "String",
  "version": "String"
}
```

</td></tr><tr><td>

result.ai\_model

</td><td>

AI Model of the AI Prompt Asset record.Data type: Object

```
"ai_model": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.ai\_model.name

</td><td>

Name of the AI model.Data type: String

</td></tr><tr><td>

result.ai\_model.sys\_id

</td><td>

Sys\_id of the AI Prompt Product Model record.Table: AI Prompt Product Model \[alm\_ai\_model\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.created

</td><td>

Date and time that the AI Prompt Asset record was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.description

</td><td>

Description of the AI Prompt Product Model record.Table: AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\]

Data type: String

</td></tr><tr><td>

result.display\_name

</td><td>

Display name of the associated AI Prompt Asset record.Table: AI Prompt Asset \[alm\_ai\_prompt\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.documentation

</td><td>

Documentation for the AI Prompt Product Model record.Table: AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\]

Data type: String

</td></tr><tr><td>

result.managed\_by

</td><td>

User who manages the AI Prompt Asset record.Data type: Object

```
"managed_by": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.managed\_by.name

</td><td>

Name of the user who manages the asset record.Data type: String

</td></tr><tr><td>

result.managed\_by.sys\_id

</td><td>

Sys\_id of the User record that corresponds to the Managed by user of the asset record.Tables: User \[sys\_user\], AI Prompt Asset \[alm\_ai\_model\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.name

</td><td>

Name of the associated AI Prompt Product Model.Table: AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\]

Data type: String

</td></tr><tr><td>

result.prompt\_info

</td><td>

Prompt information of the AI Prompt Asset record.Table: AI Prompt Asset \[alm\_ai\_prompt\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.provider

</td><td>

Provider of the AI Prompt Product Model record.```
"provider": {
  "name": "String",
  "sys_id": "String"
}
```

Data type: Object

</td></tr><tr><td>

result.provider.name

</td><td>

Name of the associated AI Prompt Product Model record.Data type: String

</td></tr><tr><td>

result.provider.sys\_id

</td><td>

Sys\_id of the Company \[core\_company\] table record that corresponds to the Provider of the associated AI Prompt Product Model record.Tables: Company \[core\_company\], AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\]

Data type: String

</td></tr><tr><td>

result.state

</td><td>

State of the AI Prompt Asset record.Possible values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the AI Prompt Asset record.Table: AI Prompt Asset \[alm\_ai\_prompt\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.updated

</td><td>

Date and time that the AI Prompt Asset record was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.version

</td><td>

Version of the associated AI Prompt Product Model record. For example, `V2`.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to retrieve information about a AI Prompt Asset Model using a specific ID.

```
curl "https://instance.servicenow.com/api/sn_ent/asset/ai_prompt/cc419cb2331e92101c9aca989d5c7b4c" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

The response body returns details about the specific prompt asset model that was retrieved.

```
{
  "result": {
    "sys_id": "cc419cb2331e92101c9aca989d5c7b4c",
    "display_name": "ServiceNow ServiceNow Incident Summarization Prompt 4 V8",
    "name": "ServiceNow Incident Summarization Prompt 4",
    "description": "Prompt for Incident Summarization",
    "version": "V8",
    "provider": {
      "sys_id": "93d4ecfac0a8000b6294d71b733977fb",
      "name": "ServiceNow"
    },
    "documentation": "Documentation",
    "state": "Development",
    "ai_model": {
      "sys_id": "a57d0be6eb1e5210aa82fab8bad0cd18",
      "name": "mistral-large"
    },
    "prompt_info": "Provide incident summary using short_decription, state, worknotes",
    "managed_by": {
      "sys_id": "62826bf03710200044e0bfc8bcbe5df1",
      "name": "Abel Tuter"
    },
    "created": "2024-12-09 03:18:46",
    "updated": "2024-12-09 04:26:08"
  }
}

```

## AI Assets API - GET /sn\_ent/asset/ai\_system/\{sys\_id\}

Retrieves the data of the specified AI system asset.

### URL format

Versioned URL: `/api/sn_ent/{api_version}/asset/ai_system/{sys_id}`

Default URL: `/api/sn_ent/asset/ai_system/{sys_id}`

### Supported request parameters

<table id="table_ksp_xkw_5dc" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the asset in the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. Failed to fetch the asset with the given sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="table_ssp_xkw_5dc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the retrieved AI System Asset.```
result: {
  "ai_models": [Array],
  "ai_prompts": [Array],
  "created": "String",
  "description": "String",
  "display_name": "String",
  "documentation": "String",
  "evaluation_datasets": [Array],
  "evaluation_metrics_report": "String",
  "managed_by": {Object},
  "name": "String",
  "provider": {Object},
  "state": Number,
  "sys_id": "String",
  "updated": "String",
  "version": "String"
}
```

</td></tr><tr><td>

result.ai\_models

</td><td>

List of AI models in the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] table record.Data type: Array

```
"ai_models": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.ai\_models.name

</td><td>

Name of the AI System Digital Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.ai\_models.sys\_id

</td><td>

Sys\_id of the AI System Digital Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.ai\_prompts

</td><td>

List of AI Prompts in the AI System Asset record.Data type: Array

```
"ai_prompts": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.ai\_prompts.name

</td><td>

Name of the AI prompt.Data type: String

</td></tr><tr><td>

result.ai\_prompts.sys\_id

</td><td>

Sys\_id of the AI Prompt Digital Asset record.Table: AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.created

</td><td>

Date and time that the AI System Asset was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.description

</td><td>

Description of the associated AI System Product Model record. Table: AI System Product Model \[cmdb\_ai\_system\_product\_model\]

Data type: String

</td></tr><tr><td>

result.display\_name

</td><td>

Display name of the AI System Asset record.Table: AI System Asset \[cmdb\_ai\_ system\_asset\_model\]

Data type: String

</td></tr><tr><td>

result.documentation

</td><td>

Documentation for the AI System Product System record.Table: AI System Product System \[cmdb\_ai\_system\_product\_system\]

Data type: String

</td></tr><tr><td>

result.evaluation\_datasets

</td><td>

List of AI datasets used for evaluating the model in the AI System Digital Asset record. Mostly applicable for models developed within an organization.Tables: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\], AI System Asset \[alm\_ai\_system\_digital\_asset\]

Data type: Array

```
"evaluation_datasets": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

Default: empty string

</td></tr><tr><td>

result.evaluation\_datasets.name

</td><td>

Name of the AI Dataset Digital Asset.Data type: String

</td></tr><tr><td>

result.evaluation\_datasets.sys\_id

</td><td>

Sys\_id of the AI Dataset Digital Asset record.Table: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.evaluation\_metrics\_report

</td><td>

Evaluation results of the AI system asset record.Possible values:

-   Details \(in plain text\) outlining results
-   Links to specific results

Data type: String

</td></tr><tr><td>

result.managed\_by

</td><td>

Details about the user who manages the AI System Asset record.Data type: Object

```
"managed_by": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.managed\_by.name

</td><td>

Sys\_id of the user who manages the AI System Asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.managed\_by.sys\_id

</td><td>

Name of the user who manages the AI System Asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.name

</td><td>

Name of the associated AI System Product Model record.Table: AI System Product Model \[cmdb\_ai\_system\_product\_model\]

Data type: String

</td></tr><tr><td>

result.provider

</td><td>

Value of the Provider field in the associated AI System Product Model record.Table: AI System Product Model \[cmdb\_ai\_ system\_product\_model\]

Data type: Object

```
provider: {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.provider.name

</td><td>

Name of the provider in the associated AI System Product Model record.Table: AI System Product Model \[cmdb\_ai\_system\_product\_model\]

Data type: String

</td></tr><tr><td>

result.provider.sys\_id

</td><td>

Sys\_id of the provider in the associated AI System Product Model record.Table: AI System Product Model \[cmdb\_ai\_system\_product\_model\]

Data type: String

</td></tr><tr><td>

result.state

</td><td>

State of the AI System Asset record.Possible values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the AI System Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.updated

</td><td>

Date and time that the AI System Asset was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.version

</td><td>

Version number of the associated AI System Product Model record. For example, `V2`.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to retrieve an AI System Model Asset with a given ID.

```
curl "https://instance.servicenow.com/api/sn_ent/asset/ai_system/3b140397435a9210a63d00002fb8f2d7" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

The response body returns details about the given AI System Model Asset.

```
{
  "result": {
      "sys_id": "3b140397435a9210a63d00002fb8f2d7",
      "display_name": "ServiceNow Incident Summarization V2",
      "name": "Incident Summarization",
      "description": "Incident Summarization Skill",
      "version": "V2",
      "provider": {
        "sys_id": "93d4ecfac0a8000b6294d71b733977fb",
        "name": "ServiceNow"
      },
      "documentation": "Sample Documentation",
      "state": "Deployed",
      "ai_models": [{ 
        "sys_id": "9tgdc7e6eb1e5210aa82fab8bad0cda2", 
        "name": "llm_generic_small" 
      },
      { 
        "sys_id": "7efdc7e6eb1e5210aa82fab8bad0cda2", 
        "name": "mixtral-instruct" 
      }],
      "ai_prompts": [{ 
        "sys_id": "7d7dc7e6eb1e5210aa82fab8bad0cda2", 
        "name": "LLM Prompt" 
      }],
      "evaluation_datasets": [{ 
        "sys_id": "9d7dc7e6eb1e5210aa82fab8bad0cda2", 
        "name": "Base dataset" 
      }],
      "evaluation_metrics_report": "Sample Report",
      "managed_by": {
        "sys_id": "62826bf03710200044e0bfc8bcbe5df1",
        "name": "Abel Tuter"
      },
      "created": "2024-12-11 18:23:09",
      "updated": "2024-12-11 18:23:09"
  }
}
```

## AI Assets API - POST /sn\_ent/asset/ai\_dataset

Creates a new AI dataset asset entry in the AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\] and AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] according to details you provide in the request body.

### URL format

Versioned URL: `/api/sn_ent/{api_version}/asset/ai_dataset`

Default URL: `/api/sn_ent/asset/ai_dataset`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{object\}

</td><td>

```
{
  "acceptable_usage": "String",
  "base_datasets": [Array],
  "dataset_card": "String"
  "data_type": "String",
  "description": "String",
  "documentation": "String",
  "managed_by": "String", 
  "name": "String", 
  "provider": "String",
  "state": "String" 
  "source": "String",
  "version": "String"
}
```

</td></tr><tr><td>

\{object\}

</td><td>

```
{
  "acceptable_usage": "String",
  "base_datasets": [Array],
  "dataset_card": "String"
  "data_type": "String",
  "description": "String",
  "documentation": "String",
  "managed_by": "String", 
  "name": "String", 
  "provider": "String",
  "state": "String" 
  "source": "String",
  "version": "String"
}
```

</td></tr><tr><td>

\{object\}.acceptable\_usage

</td><td>

Determines how a dataset or model can be used, typically for training or evaluation purposes.Valid values:

-   1: Training
-   2: Evaluation

Data type: String

</td></tr><tr><td>

\{object\}.base\_datasets

</td><td>

Comma-separated list of base datasets needed to build this dataset. Accepts names or sys\_ids of datasets present in AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\] table.Data type: Array

```
“base_datasets”: [ “String”, “String”]
```

</td></tr><tr><td>

\{object\}.data\_type

</td><td>

Type of data present in the dataset. For example, `Text,Video,Image` or `1,2`.Data type: String

</td></tr><tr><td>

\{object\}.dataset\_card

</td><td>

The data set card. A dataset\_card is a metadata document that describes the contents, structure, and context of an AI dataset. It provides details like data sources, features, intended use, and any known limitations to ensure proper understanding and usage.Data type: String

</td></tr><tr><td>

\{object\}.description

</td><td>

Description of the associated record in the AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table.Data type: String

</td></tr><tr><td>

\{object\}.documentation

</td><td>

Documentation for the AI Dataset Product Model.Data type: String

</td></tr><tr><td>

\{object\}.managed\_by

</td><td>

Value of the Managed by field of an existing User \[sys\_user\] table record. Valid values:

-   Name of the User \[sys\_user\] record
-   Sys\_id of the User \[sys\_user\] record

Data type: String

</td></tr><tr><td>

\{object\}.name

</td><td>

Required. Name of the associated record in the AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table.Data type: String

</td></tr><tr><td>

\{object\}.provider

</td><td>

Required. Value of the Provider field of an existing record in the Company \[core\_company\] table. Valid values:

-   Name of the Company \[core\_company\] record
-   Sys\_id of the Company \[core\_company\] record

Data type: String

</td></tr><tr><td>

\{object\}.source

</td><td>

Details about the source of the dataset.Valid values:

-   Link to the source of the dataset.
-   Details of the source in plain text.

Data type: String

Default: empty or null

</td></tr><tr><td>

\{object\}.state

</td><td>

State of the AI dataset asset.Valid values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

\{object\}.version

</td><td>

Version number of the associated AI Dataset Product Model record. For example, `V2`.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details of the newly created AI Dataset asset.Data type: Object

```
"result": {
  "acceptable_usage": {Object},
  "base_datasets": [Array],
  "created": "String",
  "dataset_card": "String",
  "data_type": {Object},
  "description": "String",
  "documentation": "String",
  "display_name": "String",
  "managed_by": {Object},
  "name": "String",
  "provider": {Object},
  "state": "Development",
  "source": "String",
  "sys_id": "String",
  "updated": "String",
  "version": "String",
}
```

</td></tr><tr><td>

result.acceptable\_usage

</td><td>

Acceptable usage for the AI Dataset Asset record. Acceptable usage refers to how a dataset or model can be used, typically for training or evaluation purposes.Data type: Object

```
"acceptable_usage": {
  "label": "String" 
  "value": "String" 
}
```

</td></tr><tr><td>

result.acceptable\_usage.label

</td><td>

Display label of the acceptable usage value.Data type: String

</td></tr><tr><td>

result.acceptable\_usage.value

</td><td>

Number value of the acceptable usage.Valid values:

-   1: Training
-   2: Evaluation

Data type: String

</td></tr><tr><td>

result.base\_datasets

</td><td>

Comma-separated list of base datasets required to build the given dataset. Accepts the name or sys\_id of a base data set in the AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\] table.Data type: Array

```
"base_datasets": ["String", "String"]
```

</td></tr><tr><td>

result.created

</td><td>

Date and time that the AI Dataset Asset record was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.data\_type

</td><td>

The type of data present in the AI Dataset Asset record.Data type: Object

```
"data_type": {
  "label": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.data\_type.label

</td><td>

The display label for the data type value.Data type: String

</td></tr><tr><td>

result.data\_type.value

</td><td>

Value of the dataset asset's data type.Data type: String

</td></tr><tr><td>

result.dataset\_card

</td><td>

The data set card. A dataset\_card is a metadata document that describes the contents, structure, and context of an AI dataset. It provides details like data sources, features, intended use, and any known limitations to ensure proper understanding and usage.Data type: String

</td></tr><tr><td>

result.description

</td><td>

Description of the associated AI Dataset Product Model record.Table: AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\]

Data type: String

</td></tr><tr><td>

result.display\_name

</td><td>

Display name of the AI Dataset Asset record.Table: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.documentation

</td><td>

Documentation of the associated AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.managed\_by

</td><td>

Details about the user who manages the AI Dataset Asset record.Data type: Object

```
"managed_by": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.managed\_by.name

</td><td>

Name of the user who manages the AI Dataset Asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.managed\_by.sys\_id

</td><td>

Sys\_id of the user who manages the AI Dataset Asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.name

</td><td>

Name of the associated AI Dataset Product Model record.Table: AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\]

Data type: String

</td></tr><tr><td>

result.provider

</td><td>

Provider of the associated AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table record.Data type: Object

```
provider: {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.provider.sys\_id

</td><td>

Sys\_id of the provider in the associated AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.provider.name

</td><td>

Name of the provider.Data type: String

</td></tr><tr><td>

result.source

</td><td>

Details about the source of AI dataset asset.Valid values:

-   Link to the source of the dataset asset.
-   Details \(in plain text\) of the source of the dataset asset. For example, the name of a product or website.

Data type: String

Default: empty or null

</td></tr><tr><td>

result.state

</td><td>

State of the AI Dataset Asset record.Possible values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the AI Dataset Asset record.Table: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.updated

</td><td>

Date and time that the AI Dataset Asset record was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.version

</td><td>

Version number of the associated AI Dataset Product Model record. For example, `V2`.Data type: String

</td></tr><tr><td>

result.warnings

</td><td>

Comma-separated list of warning messages that are present when creating the dataset. These warnings can be validation checks, such as when the sys\_id of an optional parameter is invalid.Data type: Array

```
"warnings": ["String"]
```

</td></tr></tbody>
</table>### cURL request

The following example shows how to create a new AI dataset asset record.

```
curl -X POST 'https://instance.servicenow.com/api/sn_ent/asset/ai_dataset' \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d ' { 
  "name": "Dataset One", 
  "description": "Description for dataset ", 
  "provider": "servicenow", 
  "version": "V1", 
  "state": 31, 
  “source”: “Source of dataset” 
  "documentation": "document", 
  “dataset_card”: “Dataset Card”, 
  “base_datasets”: [ “Dataset Two”, “Dataset Three”], 
  “data_type”: “1,2”, 
  “acceptable_usage”: “1,2”, 
  "managed_by": "abel.tuter" 
}'
```

Response body. The results of the newly created dataset asset record.

```
{ 
  "result": { 
    "asset": { 
      "sys_id": "da8393eb40d25210f877b00c113d1fc1", 
      "display_name": "ServiceNow Closed Incidents", 
      "name": "Closed Incidents", 
      "description": "Incidents with resolution", 
      "documentation": "Sample Documentation", 
      "source": "incident table on servicenow instance", 
      "dataset_card": "Dataset Card", 
      "state": "Deployed", 
      "version": null, 
      "data_type": { 
        "value": "1", 
        "label": "Text" 
      }, 
      "provider": { 
        "sys_id": "93d4ecfac0a8000b6294d71b733977fb", 
        "name": "ServiceNow" 
      }, 
      "managed_by": { 
        "sys_id": "undefined", 
        "name": "" 
      }, 
      "acceptable_usage": { 
        "value": "1", 
        "label": "Training" 
      }, 
      "base_datasets": [], 
      "created": "2024-12-12 01:23:03", 
      "updated": "2024-12-12 01:23:03" 
    }, 
    "warnings": [] 
       } 
}
```

## AI Assets API - POST /sn\_ent/asset/ai\_prompt

Creates a new AI prompt asset entry in the AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\] and AI Prompt Product Model \[cmdb\_ai\_promt\_product\_model\] tables according to details you provide in the request body.

### URL format

Versioned URL: `/api/sn_ent/{api_version}/asset/ai_prompt`

Default URL: `/api/sn_ent/asset/ai_prompt`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="id_tqz_jgh_zdc" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

object

</td><td>

Required. Content of the AI Prompt asset to update.Data type: Object

```
{
  "ai_model": "String",
  "description": "String",
  "documentation": "String",
  "managed_by": "String" 
  "name": "String",
  "prompt_info": "String", 
  "provider": "String",
  "state": Number,
  "version": "String"
} 
```

</td></tr><tr><td>

ai\_model

</td><td>

Value of the AI Model field of an existing record in the AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\] table.Valid values:

-   Name of the AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\] record
-   Sys\_id of the AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\] record

Data type: String

Default: empty string

</td></tr><tr><td>

description

</td><td>

Description to give the AI Prompt Product Model.Table: AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\]

Data type: String

Default: empty string

</td></tr><tr><td>

documentation

</td><td>

Documentation of the AI Prompt Product Model.Data type: String

Default: empty string

</td></tr><tr><td>

managed\_by

</td><td>

Value of the Managed by field of an existing record in the User \[sys\_user\] table.Valid values:

-   Name of the User \[sys\_user\] record
-   Sys\_id of the User \[sys\_user\] record

Data type: String

Default: empty string

</td></tr><tr><td>

name

</td><td>

Required. Name of the associated record in the AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\] table.Data type: String

Default: empty string

</td></tr><tr><td>

prompt\_info

</td><td>

Prompt information for AI Prompt Asset.Data type: String

Default: empty string

</td></tr><tr><td>

provider

</td><td>

Required. Value of the Provider field of an existing record in the Company \[core\_company\] table.Valid values:

-   Name of the Company \[core\_company\] record
-   Sys\_id of the Company \[core\_company\] record

Data type: String

</td></tr><tr><td>

state

</td><td>

State to apply to the AI Model Asset. For example, Valid values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

version

</td><td>

Version number to assign the AI Prompt Product Model. For example, `V2`.Data type: String

Default: empty string

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_ssp_xkw_5dc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Results of the new AI asset prompt.Data type: Object

```
"result": { 
    "asset": Object, 
    "warnings": [Array] 
 }
```

</td></tr><tr><td>

result.asset

</td><td>

Details about the newly created entry.Data type: Object

```
"asset": {
  "ai_model": [Array],
  "ai_prompts": [Array]
  "created": "String",
  "description": "String",
  "display_name": "String",
  "documentation": "String",
  "evaluation_datasets": [Array],
  "evaluation_metrics_report": String,
  "managed_by": Object,
  "name": "String",
  "provider": Object,
  "state": "String",
  "sys_id": "String",
  "updated": "String",
  "version": "String",
  "warnings": [Array]
}
```

</td></tr><tr><td>

result.asset.ai\_model

</td><td>

List of AI models in the AI System Asset \[cmdb\_ai\_ system\_asset\_model\] table record.Data type: Array

```
"ai_model": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.asset.ai\_models.name

</td><td>

Name of the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] table record.Data type: String

</td></tr><tr><td>

result.asset.ai\_models.sys\_id

</td><td>

Sys\_id of the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] table record.Data type: String

</td></tr><tr><td>

result.asset.ai\_prompts

</td><td>

List of AI Prompts of the AI System Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: Array

```
"ai_prompts": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.asset.ai\_prompts.name

</td><td>

Name of the AI prompt.Data type: String

</td></tr><tr><td>

result.asset.ai\_prompts.sys\_id

</td><td>

Sys\_id of the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] table record.Data type: String

</td></tr><tr><td>

result.asset.created

</td><td>

Date and time that the AI model asset was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.asset.description

</td><td>

Description of the associated AI System Product Model record. Table: AI System Product Model \[cmdb\_ai\_system\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.display\_name

</td><td>

Display name of the AI System Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.documentation

</td><td>

Documentation of the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.asset.evaluation\_datasets

</td><td>

List of sys\_ids or display names of the AI datasets used to evaluate the AI system asset model. Mostly applicable for models developed within an organization.Tables: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\], AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: Array

```
"evaluation_datasets": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.asset.evaluation\_datasets.name

</td><td>

Name of the AI Dataset Digital Asset.Data type: String

</td></tr><tr><td>

result.asset.evaluation\_datasets.sys\_id

</td><td>

Sys\_id of the AI System Digital Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.evaluation\_metrics\_report

</td><td>

Evaluation results of the AI system asset.Possible values:

-   Details \(in plain text\) outlining results
-   Links to specific results

Data type: String

</td></tr><tr><td>

result.asset.managed\_by

</td><td>

Details about the user who manages the asset.Data type: Object

```
"managed_by": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.asset.managed\_by.name

</td><td>

Name of the user who manages the AI model asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.asset.managed\_by.sys\_id

</td><td>

Sys\_id of the user who manages the AI model asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.asset.name

</td><td>

Name of the associated AI System Product Model record.Table: AI System Product Model \[cmdb\_ai\_system\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.provider

</td><td>

Value of the Provider field in the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: Object

```
provider: {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.asset.provider.name

</td><td>

Name of the provider in the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.asset.provider.sys\_id

</td><td>

Sys\_id of the provider in the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.asset.state

</td><td>

State of the AI Model Asset. Possible values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

result.asset.sys\_id

</td><td>

Sys\_id of the AI System Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.updated

</td><td>

Date and time that the AI model asset was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.warning

</td><td>

Comma-separated list of warning messages. These warnings can be validation checks, such as when the sys\_id of an optional parameter is invalid.Data type: Array

```
"warnings": ["String"]
```

</td></tr></tbody>
</table>### cURL request

The following example shows how to use the POST method to create a new AI prompt according to details provided in the request body.

```
curl -X POST 'https://instance.servicenow.com/api/sn_ent/asset/ai_prompt' \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d '{ 
  "name": "Incident Summarization prompt1", 
  "description": "Prompt for Incident Summarization", 
  "provider": "servicenow", 
  "version": "V1", 
  "state": 31, 
  "documentation": "Document", 
  "ai_model": "mixtral-instruct", 
  "prompt_info": "Provide incident summary using short_decription, state, worknotes", 
  "managed_by": "abel.tuter" 
 }'
```

Response body.

```
{ 
  "result": { 
    "asset": { 
      "sys_id": "9833721b331e92101c9aca989d5c7bf0", 
      "display_name": "ServiceNow Incident Summarization prompt1 V1", 
      "name": "Incident Summarization prompt1", 
      "description": "Prompt for Incident Summarization", 
      "version": "V1", 
      "provider": { 
        "sys_id": "93d4ecfac0a8000b6294d71b733977fb", 
        "name": "ServiceNow" 
      }, 
      "documentation": "Document", 
      "state": "Deployed", 
      "ai_model": { 
        "sys_id": "9d7dc7e6eb1e5210aa82fab8bad0cda2", 
        "name": "mixtral-instruct" 
      }, 
      "prompt_info": "Provide incident summary using short_decription, state, worknotes", 
      "managed_by": { 
        "sys_id": "62826bf03710200044e0bfc8bcbe5df1", 
        "name": "Abel Tuter" 
      }, 
      "created": "2024-12-11 04:23:17", 
      "updated": "2024-12-11 04:23:17" 
    }, 
    "warnings": [] 
  } 
}
```

## AI Assets API - POST /sn\_ent/asset/ai\_model

Creates a new AI model asset entry in the AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\] and AI Model Product Model \[cmdb\_ai\_model\_product\_model\] tables according to details you provide in the request body.

### URL format

Versioned URL: `/api/sn_ent/{api_version}/asset/ai_model`

Default URL: `/api/sn_ent/asset/ai_model`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="id_z5b_fkh_zdc" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{object\}

</td><td>

Required. Details to apply to the new asset model record.Data type: Object

```
"object": {
  "base_model": {Object},
  "context_window:" "String",
  "deployment_guideline": "String",
  "description": "String", 
  "documentation": "String",
  "evaluation_datasets": [Array],
  "evaluation_metrics_report": "String",
  "managed_by": "String", 
  "model_size_in_mb": "String",
  "model_weights_info": "String",
  "name": "String",
  "parameters_info": "String",
  "provider": "String",
  "required_infrastructure": "String",
  "source": "String",
  "state": Number,
  "supported_languages: [Array],
  "training_datasets": [Array],
  "training_procedure": "String",
  "version": "String"
} 
```

</td></tr><tr><td>

\{object\}.base\_model

</td><td>

AI model that this model version was derived from.**Note:** Only applicable for models developed within the organization.

Data type: Object

```
{
  "name": "String",
  "sys_id": "String"
 }
```

</td></tr><tr><td>

\{object\}.base\_model.name

</td><td>

Name of the AI model asset to model this AI model after.Data type: String

</td></tr><tr><td>

\{object\}.base\_model.sys\_id

</td><td>

Sys\_id of the AI model asset to model this AI model after.Table: AI Model Digital Asset \[alm\_ai\_dataset\_digital\_asset\]

Data type: String

Default: empty string

</td></tr><tr><td>

\{object\}.context\_window

</td><td>

Size of input sequences \(in other words, the number of tokens\) that the model can handle.Data type: Integer

Default: empty value

</td></tr><tr><td>

\{object\}.deployment\_guideline

</td><td>

Instructions applicable for models developed and deployed within an organization.Data type: String

Default: empty string

</td></tr><tr><td>

\{object\}.description

</td><td>

Description to give the AI Model Product Model. Updated table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

Default: empty string

</td></tr><tr><td>

\{object\}.documentation

</td><td>

Documentation of the AI Model Product Model.Data type: String

Default: empty string

</td></tr><tr><td>

\{object\}.evaluation\_datasets

</td><td>

Comma-separated list of sys\_ids or display names of AI datasets of the AI datasets used for evaluating the model. Mostly applicable for models developed within an organization.Tables: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\], AI Model Asset \[alm\_ai\_model\_digital\_asset\]

Data type: Array

```
"evaluation_datasets": ["String", "String"]
```

Valid values:

-   Name of the AI Dataset Digital Asset record.
-   Sys\_id of the AI Dataset Digital Asset record.

Default: empty string

</td></tr><tr><td>

\{object\}.evaluation\_metrics\_report

</td><td>

Reference to the evaluation results located within the text field of the AI model digital asset record. For example:```
Testing results:  link to the result document

Details:
Accuracy: 85%
Hallucination: 10%
Eval Run 1: link
Eval Run 2: link

```

Table: AI model digital asset \[alm\_ai\_model\_digital\_asset\]

Data type: String

Default: empty string

</td></tr><tr><td>

\{object\}.managed\_by

</td><td>

Value of the 'Managed by' field of an existing record in the User \[sys\_user\] table. Valid values:

-   Name of the User \[sys\_user\] record
-   Sys\_id of the User \[sys\_user\] record

Data type: String

Default: empty string

</td></tr><tr><td>

\{object\}.model\_size\_in\_mb

</td><td>

Size of the model in MB. Mostly applicable for models developed and deployed within an organization.Data type: Number

Default: null or empty

</td></tr><tr><td>

\{object\}.model\_weights\_info

</td><td>

Additional model information, if available. Mostly applicable for models developed within an organization.Data type: String

Default: null or empty

</td></tr><tr><td>

\{object\}.name

</td><td>

Required. Name of the AI Model Product Model. Table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

Default: null or empty

</td></tr><tr><td>

\{object\}.parameters\_info

</td><td>

Number of parameters given to for the model.Data type: String

Default: empty string

</td></tr><tr><td>

\{object\}.provider

</td><td>

Required. Value of the 'Provider' field of existing record in Company \[core\_company\] table. Assigns this provider to the new AI model.Valid values:

-   Name of the Company \[core\_company\] record
-   Sys\_id of the Company \[core\_company\] record

Data type: String

Default: empty string

</td></tr><tr><td>

\{object\}.required\_infrastructure

</td><td>

Documentation of infrastructure needs for the model deployment. For example, details about the infrastructure stack and processing needs. Mostly applicable for models deployed within an organization.Data type: String

Default: empty or null

</td></tr><tr><td>

\{object\}.source

</td><td>

Details about the source of who or what created the model.Valid values:

-   Link to the source of the model. For example, `https://huggingface.co/mistralai/Mixtral-8x7B-Instruct-v0.1` or a link to Github.
-   Details of the source in plain text. For example, `Microsoft Azure`

Data type: String

Default: empty or null

</td></tr><tr><td>

\{object\}.state

</td><td>

State to apply to the AI Model Asset.Valid values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

\{object\}.supported\_languages

</td><td>

Comma-separated list of languages that are supported by the AI Model.Data type: Array

```
"supported_languages": [
  "String",
  "String"
]
```

Valid values:

-   Sys\_id of Language \[sys\_language\] record
-   Name of Language \[sys\_language\] record. For example, `"French", "English"`.

Default: empty string

</td></tr><tr><td>

\{object\}.training\_datasets

</td><td>

Datasets used to train the AI Model. Comma-separated list of sys\_ids or display names of the AI Dataset Asset \[alm\_ai\_dataset\_digital\_asset\] table. Mostly applicable for models developed within an organization.Data type: Array

```
"training_datasets": [
  "String",
  "String"
]
```

Default: empty string

</td></tr><tr><td>

\{object\}.training\_procedure

</td><td>

Type of training to apply to the AI model.Valid values:

-   1: Decision Trees
-   2: Deep Neural Networks
-   3: Linear Regression
-   4: Logistic Regression
-   5: Random Forest
-   6: Supervised Learning
-   7: Unsupervised Learning
-   8: Reinforcement Learning
-   9: Transfer Learning
-   10: Semi-Supervised Learning
-   11: Instruction Finetuning
-   12: Supervised Finetuning

Data type: String represented with a number \(for example, `"3"`\)

Default: 1: Decision Trees

</td></tr><tr><td>

\{object\}.version

</td><td>

Version for AI Model Product Model. For example, `V2`.Data type: String

Default: empty string

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|201|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="id_itg_lz3_12c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Results of the AI model asset creation.Data type: Object

```
"result": { 
    "asset": Object, 
    "warnings": [Array], 
 } 
```

</td></tr><tr><td>

result.asset

</td><td>

Details about the created AI model asset.Data type: Object

```
"asset": {
  "base_model": Object,
  "context_window": String,
  "created": "String",
  "deployment_guideline": String,
  "description": "String",
  "display_name": "String",
  "documentation": "String",
  "evaluation_datasets": Array,
  "evaluation_metrics_report": String,
  "managed_by": Object,
  "model_size_in_mb": String,
  "name": "String",
  "parameters_info": "String",
  "provider": Object,
  "required_infrastructure": String,
  "state": "String",
  "source": String, 
  "supported_languages": Array,
  "sys_id": "String",
  "training_datasets": Array,
  "training_procedure": String,
  "updated": "String",
  "version": "String"
}
```

</td></tr><tr><td>

result.asset.base\_model

</td><td>

Information about the AI model asset from which this version derived from.Data type: Object

```
"base_model": { 
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.asset.base\_model.name

</td><td>

Display name of AI model asset.Table: AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.base\_model.sys\_id

</td><td>

Sys\_id of AI model asset.Table: AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.context\_window

</td><td>

Size of input sequences that the model can handle. In other words, the number of tokens.Data type: String represented with a number. For example, `"6000"`.

</td></tr><tr><td>

result.asset.created

</td><td>

Date and time that the AI model asset was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.asset.deployment\_guideline

</td><td>

Instructions applicable for models developed and deployed within an organization.Data type: String

</td></tr><tr><td>

result.asset.description

</td><td>

Description of the associated AI Model Product Model record.Table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.display\_name

</td><td>

Display name of the AI Model Asset record.Table: AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\] \(display\_name field\)

Data type: String

</td></tr><tr><td>

result.asset.documentation

</td><td>

Documentation of the associated AI Model Product Model record.Table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.evaluation\_datasets

</td><td>

Comma-separated list of sys\_ids or display names of AI datasets of the AI Model Digital Asset used for evaluating the model. Mostly applicable for models developed within an organization.Tables: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\], AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]

Data type: Array

```
"evaluation_datasets": [
  { 
  "name": "String",
  "sys_id": "String"
  } 
]
```

</td></tr><tr><td>

result.evaluation\_datasets.name

</td><td>

Name of the AI Dataset Digital Asset.Data type: String

</td></tr><tr><td>

result.evaluation\_datasets.sys\_id

</td><td>

Sys\_id of the AI Model Digital Asset record.Table: AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.evaluation\_metrics\_report

</td><td>

Reference to the evaluation results.Possible values:

-   Details \(in plain text\) outlining results
-   Links to specific results

Data type: String

</td></tr><tr><td>

result.asset.managed\_by

</td><td>

User that manages the AI model asset record.Data type: Object

```
" managed_by": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.asset.managed\_by.name

</td><td>

Name of the user who manages the AI model asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.asset.managed\_by.sys\_id

</td><td>

Sys\_id of the user who manages the AI model asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.asset.model\_size\_in\_mb

</td><td>

Size of the model in MB. Usually applicable for models developed and deployed within an organization.Data type: Number

</td></tr><tr><td>

result.asset.name

</td><td>

Name of the associated AI Model Product Model record.Table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.provider

</td><td>

Provider of the associated AI Model Product Model record.Table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: Object

```
"provider": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.asset.provider.name

</td><td>

Name of the provider.Data type: String

</td></tr><tr><td>

result.asset.provider.sys\_id

</td><td>

Sys\_id of the record from Company \[core\_company\] table that corresponds to the Provider of the associated AI Model Product Model record.Table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.source

</td><td>

Details about the source of the asset.Valid values:

-   Link to the source of the model. For example, `https://huggingface.co/mistralai/Mixtral-8x7B-Instruct-v0.1` or a link to Github.
-   Details of the source in plain text. For example, `Microsoft Azure`

Data type: String

</td></tr><tr><td>

result.asset.state

</td><td>

State of the AI Model Asset record.Possible values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

result.asset.supported\_languages.name

</td><td>

Name of the supported language.Table: Language \[sys\_language\]

Data type: String

</td></tr><tr><td>

result.asset.supported\_languages.sys\_id

</td><td>

Sys\_id of the supported language.Table: Language \[sys\_language\]

Data type: String

</td></tr><tr><td>

result.asset.sys\_id

</td><td>

Sys\_id of the AI Model Asset record Table: AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.training\_datasets

</td><td>

Reference to 1+ associated data sets used for training the model.Data type: Array

```
"training_datasets": [
  { 
  "name": "String",
  "sys_id": "String"
  } 
]
```

</td></tr><tr><td>

result.asset.training\_procedure

</td><td>

Type of AI training applied to the model.Possible values:

-   1: Decision Trees
-   2: Deep Neural Networks
-   3: Linear Regression
-   4: Logistic Regression
-   5: Random Forest
-   6: Supervised Learning
-   7: Unsupervised Learning
-   8: Reinforcement Learning
-   9: Transfer Learning
-   10: Semi-Supervised Learning
-   11: Instruction Finetuning
-   12: Supervised Finetuning

Data type: String

</td></tr><tr><td>

result.asset.updated

</td><td>

Date and time that the AI model asset was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.asset.version

</td><td>

Version of the associated AI Model Product Model record.Table: AI Model Product Model \[cmdb\_ai\_model\_product\_model table\]

Data type: String

</td></tr><tr><td>

result.required\_infrastructure

</td><td>

Documentation of infrastructure needs for the model's deployment. For example, details about the infrastructure stack and processing needs.Data type: String

</td></tr><tr><td>

result.asset.parameters\_info

</td><td>

Properties of the training data that learn during the learning process. For example: `7B` or `30B`.Data type: String

</td></tr><tr><td>

result.asset.supported\_languages

</td><td>

Details about the languages supported by the AI model asset.Table: Language \[sys\_language\]

Data type: Object

```
"supported_languages": [
 { 
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.warnings

</td><td>

Comma-separated list of warning messages. These warnings can be validation checks, such as when the sysId of an optional parameter is invalid.Data type: Array

```
"warnings": ["String"]
```

</td></tr></tbody>
</table>### cURL request

The following example creates an AI model asset according to details provided in the request body.

```
curl -X POST 'https://instance.servicenow.com/api/sn_ent/asset/ai_prompt' \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d ' {
  "name": "Now LLM",
  "description": "enables text-to-text like question answering and summarization",
  "provider": "servicenow",
  "documentation": "Now LLM V5 Documentation",
  "version": "V8",
  "parameters_info": "7B",
  "supported_languages": [
    "English",
    "French"
  ],
  "model_size_in_mb": "87",
  "deployment_guideline": "Deployed on ServiceNow infrastructure",
  "source": "https://huggingface.co/mistralai/Mixtral-8x7B-Instruct-v0.1",
  "training_procedure": "2",
  "context_window": "8000",
  "state": "31",
  "base_model": "Servicenow Now LLM V6",
  "model_weights_info": "refer to weights and biases project",
  "required_infrastructre": "GPUs needed: 1, GPU Type: A100",
  "training_datasets": [
    "Servicenow Open Incidents"
  ],
  "evaluation_datasets": [
    "Servicenow Open Incidents"
  ],
  "evaluation_metrics_report": "Testing results: See files attached to this record",
  "managed_by": "abel.tuter"
}'
```

The response body shows details about the newly created AI model asset, including the resultant sys\_id.

```
{
  "result": {
    "asset": {
      "sys_id": "a438d170ff96da10c1fbffffffffffd5",
      "display_name": "ServiceNow Now LLM V6",
      "name": "Now LLM",
      "description": "enables text-to-text like question answering and summarization",
      "version": "V8",
      "provider": {
        "sys_id": "93d4ecfac0a8000b6294d71b733977fb",
        "name": "ServiceNow"
      },
      "documentation": "Now LLM V5 Documentation",
      "parameters_info": "7B",
      "supported_languages": [
        {
          "sys_id": "914493a30f320010e96b0e4fef767e90",
          "name": "English"
        }
      ],
      "model_size_in_mb": "87",
      "deployment_guideline": "Deployed on ServiceNow infrastructure",
      "source": "https://huggingface.co/mistralai/Mixtral-8x7B-Instruct-v0.1",
      "training_procedure": "2",
      "context_window": "8000",
      "state": "Deployed",
      "required_infrastructure": "Servicenow Instance",
      "base_model": {
        "sys_id": "a438d170ff96da10c1fbffffffffffd5",
        "name": "ServiceNow Now LLM V8"
      },
      "evaluation_datasets": [
        {
          "sys_id": "45cb45baff06d610c1fbffffffffffa9",
          "name": "ServiceNow Open Incidents"
        }
      ],
      "training_datasets": [
        {
          "sys_id": "45cb45baff06d610c1fbffffffffffa9",
          "name": "ServiceNow Open Incidents"
        }
      ],
      "evaluation_metrics_report": "Testing results: See files attached to this record",
      "managed_by": {
        "sys_id": "62826bf03710200044e0bfc8bcbe5df1",
        "name": "Abel Tuter"
      },
      "created": "2024-12-03 16:50:53",
      "updated": "2024-12-12 15:56:28"
    },
    "warnings": [
      "Reference record 'French' not found for supported_languages in table sys_language"
    ]
  }
}
```

## AI Assets API - POST /sn\_ent/asset/ai\_system

Creates a new AI system asset entry in the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] and AI System Product Model \[cmdb\_ai\_system\_product\_model\] tables according to details you provide in the request body.

### URL format

Versioned URL: `/api/sn_ent/{api_version}/asset/ai_system`

Default URL: `/api/sn_ent/asset/ai_system`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="id_ack_2dh_zdc" class="rest_api_request_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

object

</td><td>

Required. Details to update in the AI system.Data type: Object

```
{ 
  "name": "String", 
  "description": "String", 
  "provider": "String", 
  "version": "String", 
  "state": Number, 
  "documentation": "String", 
  "ai_models": "String", 
  "ai_prompts": "Strings", 
  "evaluation_datasets": [Array], 
  "evaluation_metrics_report": "String", 
  "managed_by": "String" 
}
```

</td></tr><tr><td>

object.name

</td><td>

Required. Name for the AI System Product Model.Data type: String

</td></tr><tr><td>

object.description

</td><td>

Description for the AI System Product Model.Data type: String

</td></tr><tr><td>

object.provider

</td><td>

Required. Value of the Provider field in an existing Company \[core\_company\] table record. Valid values:

-   Name of the Company \[core\_company\] record
-   Sys\_id of the Company \[core\_company\] record

Data type: String

</td></tr><tr><td>

object.state

</td><td>

State to apply to the AI System Asset. Valid values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

Default: empty string

</td></tr><tr><td>

object.version

</td><td>

Version for AI System Product Model. For example, `V2`.Data type: String

Default: empty string

</td></tr><tr><td>

object.documentation

</td><td>

Documentation of the AI System Asset.Data type: String

Default:

</td></tr><tr><td>

object.ai\_models

</td><td>

Comma-separated list of strings, where each string represents an AI Model field value of an existing AI Model Digital Asset record.Table: AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]

Valid values:

-   Name of the AI Model Digital Asset record.
-   Sys\_id of the AI Model Digital Asset record.

Data type: String

Default: empty string

</td></tr><tr><td>

object.evaluation\_datasets

</td><td>

Comma-separated list of AI datasets used for evaluating the AI System Asset record. Mostly applicable for models developed within an organization.Tables: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\], AI System Asset \[AI System Digital Asset alm\_ai\_system\_digital\_asset\]

Data type: Array

```
"evaluation_datasets": [{String", "String"}]
```

Valid values:

-   Name of the AI Dataset Digital Asset record.
-   Sys\_id of the AI Dataset Digital Asset record.

Default: empty string

</td></tr><tr><td>

object.evaluation\_metrics\_report

</td><td>

Reference to the evaluation results located within the text field of the AI system asset record. For example:```
Testing results:  link to the result document

Details:
Accuracy: 85%
Hallucination: 10%
Eval Run 1: link
Eval Run 2: link
```

Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

Default: empty string

</td></tr><tr><td>

object.managed\_by

</td><td>

Value of the 'Managed by' field of an existing User \[sys\_user\] table record. Valid values:

-   Name of the User \[sys\_user\] record
-   Sys\_id of the User \[sys\_user\] record

Data type: String

Default: empty string

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Results of the new AI system asset.Data type: Object

```
"result": {
  "asset": Object,
  "warnings": [Array]
}
```

</td></tr><tr><td>

result.asset

</td><td>

Details about the newly created entry.Data type: Object

```
"asset": {
  "ai_model": [Array],
  "ai_prompts": [Array]
  "created": "String",
  "description": "String",
  "display_name": "String",
  "documentation": "String",
  "evaluation_datasets": [Array],
  "evaluation_metrics_report": String,
  "managed_by": Object,
  "name": "String",
  "provider": Object,
  "state": "String",
  "sys_id": "String",
  "updated": "String",
  "version": "String",
  "warnings": [Array]
}
```

</td></tr><tr><td>

result.asset.ai\_models

</td><td>

List of AI models in the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] record.Data type: Array

```
"ai_models": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.asset.ai\_models.name

</td><td>

Name of the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] table record.Data type: String

</td></tr><tr><td>

result.asset.ai\_models.sys\_id

</td><td>

Sys\_id of the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] table record.Data type: String

</td></tr><tr><td>

result.asset.ai\_prompts

</td><td>

List of AI Prompts of the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] record.Data type: Array

```
"ai_prompts": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.asset.ai\_prompts.name

</td><td>

Name of the AI prompt.Data type: String

</td></tr><tr><td>

result.asset.ai\_prompts.sys\_id

</td><td>

Sys\_id of the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] table record.Data type: String

</td></tr><tr><td>

result.asset.created

</td><td>

Date and time that the AI model asset was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.asset.description

</td><td>

Description of the associated AI System Product Model record. Table: AI System Product Model \[cmdb\_ai\_system\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.display\_name

</td><td>

Display name of the AI System Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.documentation

</td><td>

Documentation of the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.asset.evaluation\_datasets

</td><td>

List of AI datasets used for evaluating the AI System Asset record. Mostly applicable for models developed within an organization.Tables: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\], AI System Asset \[alm\_ai\_system\_digital\_asset\]

Data type: Array

```
"evaluation_datasets": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.asset.evaluation\_datasets.name

</td><td>

Name of the AI Dataset Digital Asset.Data type: String

</td></tr><tr><td>

result.asset.evaluation\_datasets.sys\_id

</td><td>

Sys\_id of the AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\] table record.Data type: String

</td></tr><tr><td>

result.asset.evaluation\_metrics\_report

</td><td>

Evaluation results of the AI system asset.Possible values:

-   Details \(in plain text\) outlining results
-   Links to specific results

Data type: String

</td></tr><tr><td>

result.asset.managed\_by

</td><td>

Comma-separated list of sys\_ids or display names of AI datasets of the AI System Asset used for evaluating the model. Mostly applicable for models developed within an organization.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: Object

```
"managed_by": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.asset.managed\_by.name

</td><td>

Sys\_id of the user who manages the AI model asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.asset.managed\_by.sys\_id

</td><td>

Name of the user who manages the AI model asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.asset.name

</td><td>

Name of the associated AI System Product Model record.Table: AI System Product Model \[cmdb\_ai\_system\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.provider

</td><td>

Value of the Provider field in the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: Object

```
provider: {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.asset.provider.name

</td><td>

Name of the provider in the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.asset.provider.sys\_id

</td><td>

Sys\_id of the provider in the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.asset.state

</td><td>

State of the AI Model Asset. Possible values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

result.asset.sys\_id

</td><td>

Sys\_id of the AI System Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.updated

</td><td>

Date and time that the AI model asset was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.asset.version

</td><td>

Version number of the associated AI System Product Model record. For example, `V2`.Data type: String

</td></tr><tr><td>

result.asset.warnings

</td><td>

Comma-separated list of warning messages. These warnings can be validation checks, such as when the sys\_id of an optional parameter is invalid.Data type: Array

```
"warnings": ["String"]
```

</td></tr></tbody>
</table>### cURL request

The following example inserts a new entry into the AI System Digital Asset and AI System Product Model tables using details included in the request body.

```
curl -X POST 'https://instance.servicenow.com/api/sn_ent/asset/ai_prompt' \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d '{ 
  "name": "Incident Summarization", 
  "description": "Incident Summarization Skill", 
  "provider": "servicenow", 
  "documentation": "Sample Documentation", 
  "version": "V2", 
  "state": 31, 
  "ai_models": [ 
    "llm_generic_small", 
    "mixtral-instruct" 
  ], 
  "ai_prompts": [ 
    "LLM Prompt"   
  ], 
  "evaluation_datasets": [ 
    "Base dataset" 
  ], 
  "evaluation_metrics_report": "Sample Report", 
  "managed_by": "abel.tuter" 
}'
```

Response body.

```
{ 
  "result": { 
    "asset": { 
      "sys_id": "3b140397435a9210a63d00002fb8f2d7", 
      "display_name": "ServiceNow Incident Summarization V2", 
      "name": "Incident Summarization", 
      "description": "Incident Summarization Skill", 
      "version": "V2", 
      "provider": { 
        "sys_id": "93d4ecfac0a8000b6294d71b733977fb", 
        "name": "ServiceNow" 
      }, 
      "documentation": "Sample Documentation", 
      "state": "Deployed", 
      "ai_models": [{  
        "sys_id": "9tgdc7e6eb1e5210aa82fab8bad0cda2",  
        "name": "llm_generic_small"  
      }, 
      {  
        "sys_id": "7efdc7e6eb1e5210aa82fab8bad0cda2",  
        "name": "mixtral-instruct"  
      }], 
      "ai_prompts": [{  
        "sys_id": "7d7dc7e6eb1e5210aa82fab8bad0cda2",  
        "name": "LLM Prompt"  
      }], 
      "evaluation_datasets": [{  
        "sys_id": "9d7dc7e6eb1e5210aa82fab8bad0cda2",  
        "name": "Base dataset"  
      }], 
      "evaluation_metrics_report": "Sample Report", 
      "managed_by": { 
        "sys_id": "62826bf03710200044e0bfc8bcbe5df1", 
        "name": "Abel Tuter" 
      }, 
      "created": "2024-12-11 18:23:09", 
      "updated": "2024-12-11 18:23:09" 
    }, 
    "warnings": [] 
  } 
}
```

## AI Assets API - PUT /sn\_ent/asset/ai\_dataset/\{sys\_id\}

Updates the data of a specific AI dataset asset record according to information that you provide in the request body.

**Note:** Provide only the parameter-value pairs for the specific data you want to update. This endpoint overwrites the data for any parameters that are sent in the request.

Use the [AI Assets API - GET /sn\_ent/asset/ai\_dataset/\{sys\_id\}](ai-assets-api.md#) method to retrieve an existing AI dataset record with a given ID. You can then use this PUT method to update values in the dataset using the same ID information.

### URL format

Versioned URL: `/api/sn_ent/{api_version}/asset/ai_dataset/{sys_id}`

Default URL: `/api/sn_ent/asset/ai_dataset/{sys_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="entry-ai-assetapi-datasetID">

Sys\_id of the asset in the AI Dataset Asset \[alm\_ai\_dataset\_digital\_asset\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{object\}

</td><td>

```
{
  "acceptable_usage": "String",
  "base_datasets": [Array],
  "dataset_card": "String"
  "data_type": "String",
  "description": "String",
  "documentation": "String",
  "managed_by": "String", 
  "name": "String", 
  "provider": "String",
  "state": "String" 
  "source": "String",
  "version": "String"
}
```

</td></tr><tr><td>

\{object\}.acceptable\_usage

</td><td>

Determines how a dataset or model can be used, typically for training or evaluation purposes.Valid values:

-   1: Training
-   2: Evaluation

Data type: String

</td></tr><tr><td>

\{object\}.base\_datasets

</td><td>

Comma-separated list of base datasets needed to build this dataset. Accepts names or sys\_ids of datasets present in AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\] table.Data type: Array

```
“base_datasets”: [ “String”, “String”]
```

</td></tr><tr><td>

\{object\}.data\_type

</td><td>

Type of data present in the dataset. For example, `Text,Video,Image` or `1,2`.Data type: String

</td></tr><tr><td>

\{object\}.dataset\_card

</td><td>

The data set card. A dataset\_card is a metadata document that describes the contents, structure, and context of an AI dataset. It provides details like data sources, features, intended use, and any known limitations to ensure proper understanding and usage.Data type: String

</td></tr><tr><td>

\{object\}.description

</td><td>

Description of the associated record in the AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table.Data type: String

</td></tr><tr><td>

\{object\}.documentation

</td><td>

Documentation for the AI Dataset Product Model.Data type: String

</td></tr><tr><td>

\{object\}.managed\_by

</td><td>

Value of the Managed by field of an existing User \[sys\_user\] table record. Valid values:

-   Name of the User \[sys\_user\] record
-   Sys\_id of the User \[sys\_user\] record

Data type: String

</td></tr><tr><td>

\{object\}.name

</td><td>

Required. Name of the associated record in the AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table.Data type: String

</td></tr><tr><td>

\{object\}.provider

</td><td>

Required. Value of the Provider field of an existing record in the Company \[core\_company\] table. Valid values:

-   Name of the Company \[core\_company\] record
-   Sys\_id of the Company \[core\_company\] record

Data type: String

</td></tr><tr><td>

\{object\}.source

</td><td>

Details about the source of the dataset.Valid values:

-   Link to the source of the dataset.
-   Details of the source in plain text.

Data type: String

Default: empty or null

</td></tr><tr><td>

\{object\}.state

</td><td>

State of the AI dataset asset.Valid values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

\{object\}.version

</td><td>

Version number of the associated AI Dataset Product Model record. For example, `V2`.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_x5t_yks_ydc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details of the newly created AI Dataset asset.Data type: Object

```
"result": {
  "acceptable_usage": {Object},
  "base_datasets": [Array],
  "created": "String",
  "dataset_card": "String",
  "data_type": {Object},
  "description": "String",
  "documentation": "String",
  "display_name": "String",
  "managed_by": {Object},
  "name": "String",
  "provider": {Object},
  "state": "Development",
  "source": "String",
  "sys_id": "String",
  "updated": "String",
  "version": "String",
}
```

</td></tr><tr><td>

result.acceptable\_usage

</td><td>

Acceptable usage for the AI Dataset Asset record. Acceptable usage refers to how a dataset or model can be used, typically for training or evaluation purposes.Data type: Object

```
"acceptable_usage": {
  "label": "String" 
  "value": "String" 
}
```

</td></tr><tr><td>

result.acceptable\_usage.label

</td><td>

Display label of the acceptable usage value.Data type: String

</td></tr><tr><td>

result.acceptable\_usage.value

</td><td>

Number value of the acceptable usage.Valid values:

-   1: Training
-   2: Evaluation

Data type: String

</td></tr><tr><td>

result.base\_datasets

</td><td>

Comma-separated list of base datasets required to build the given dataset. Accepts the name or sys\_id of a base data set in the AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\] table.Data type: Array

```
"base_datasets": ["String", "String"]
```

</td></tr><tr><td>

result.created

</td><td>

Date and time that the AI Dataset Asset record was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.data\_type

</td><td>

The type of data present in the AI Dataset Asset record.Data type: Object

```
"data_type": {
  "label": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.data\_type.label

</td><td>

The display label for the data type value.Data type: String

</td></tr><tr><td>

result.data\_type.value

</td><td>

Value of the dataset asset's data type.Data type: String

</td></tr><tr><td>

result.dataset\_card

</td><td>

The data set card. A dataset\_card is a metadata document that describes the contents, structure, and context of an AI dataset. It provides details like data sources, features, intended use, and any known limitations to ensure proper understanding and usage.Data type: String

</td></tr><tr><td>

result.description

</td><td>

Description of the associated AI Dataset Product Model record.Table: AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\]

Data type: String

</td></tr><tr><td>

result.display\_name

</td><td>

Display name of the AI Dataset Asset record.Table: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.documentation

</td><td>

Documentation of the associated AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.managed\_by

</td><td>

Details about the user who manages the AI Dataset Asset record.Data type: Object

```
"managed_by": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.managed\_by.name

</td><td>

Name of the user who manages the AI Dataset Asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.managed\_by.sys\_id

</td><td>

Sys\_id of the user who manages the AI Dataset Asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.name

</td><td>

Name of the associated AI Dataset Product Model record.Table: AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\]

Data type: String

</td></tr><tr><td>

result.provider

</td><td>

Provider of the associated AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table record.Data type: Object

```
provider: {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.provider.name

</td><td>

Name of the provider.Data type: String

</td></tr><tr><td>

result.provider.sys\_id

</td><td>

Sys\_id of the provider in the associated AI Dataset Product Model \[cmdb\_ai\_dataset\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.source

</td><td>

Details about the source of AI dataset asset.Valid values:

-   Link to the source of the dataset asset.
-   Details \(in plain text\) of the source of the dataset asset. For example, the name of a product or website.

Data type: String

Default: empty or null

</td></tr><tr><td>

result.state

</td><td>

State of the AI Dataset Asset record.Possible values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the AI Dataset Asset record.Table: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.updated

</td><td>

Date and time that the AI Dataset Asset record was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.version

</td><td>

Version number of the associated AI Dataset Product Model record. For example, `V2`.Data type: String

</td></tr><tr><td>

result.warnings

</td><td>

Comma-separated list of warning messages that are present when creating the dataset. These warnings can be validation checks, such as when the sys\_id of an optional parameter is invalid.Data type: Array

```
"warnings": ["String"]
```

</td></tr></tbody>
</table>### cURL request

The following example shows how to update details in an AI dataset record with a given ID. The request body contains the parameter values to update.

```
curl -X PUT 'https://instance.servicenow.com/api/sn_ent/asset/ai_dataset/9833721b331e92101c9aca989d5c7bf0' \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d '{ 
  "name": "Dataset One", 
  "description": "Description for dataset ", 
  "provider": "servicenow", 
  "version": "V1", 
  "state": 31, 
  “source”: “Source of dataset” 
  "documentation": "document", 
  “dataset_card”: “Dataset Card”, 
  “base_datasets”: [ “Dataset Two”, “Dataset Three”], 
  “data_type”: “1,2”, 
  “acceptable_usage”: “1,2”, 
  "managed_by": "abel.tuter" 
}'
```

Response body.

```
{ 
  "result": { 
    "asset": { 
      "sys_id": "da8393eb40d25210f877b00c113d1fc1", 
      "display_name": "ServiceNow Closed Incidents", 
      "name": "Closed Incidents", 
      "description": "Incidents with resolution", 
      "documentation": "Sample Documentation", 
      "source": "incident table on servicenow instance", 
      "dataset_card": "Dataset Card", 
      "state": "Deployed", 
      "version": null, 
      "data_type": { 
        "value": "1", 
        "label": "Text" 
      }, 
      "provider": { 
        "sys_id": "93d4ecfac0a8000b6294d71b733977fb", 
        "name": "ServiceNow" 
      }, 
      "managed_by": { 
        "sys_id": "undefined", 
        "name": "" 
      }, 
      "acceptable_usage": { 
        "value": "1", 
        "label": "Training" 
      }, 
      "base_datasets": [], 
      "created": "2024-12-12 01:23:03", 
      "updated": "2024-12-12 01:23:03" 
    }, 
    "warnings": [] 
       } 
}
```

## AI Assets API - PUT /sn\_ent/asset/ai\_prompt/\{sys\_id\}

Updates the data of a specific AI prompt asset record according to information you provide in the request body.

See also:

-   [AI Assets API - GET /sn\_ent/asset/ai\_system/\{sys\_id\}](ai-assets-api.md#)
-   [AI Assets API - POST /sn\_ent/asset/ai\_prompt](ai-assets-api.md#)

**Note:** Provide only the parameter-value pairs for the specific data you want to update. This endpoint overwrites the data for any parameters that are sent in the request.

### URL format

Versioned URL: `/api/sn_ent/{api_version}/asset/ai_prompt/{sys_id}`

Default URL: `/api/sn_ent/asset/ai_prompt/{sys_id}`

### Supported request parameters

<table id="table_ksp_xkw_5dc" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the asset in the AI Prompt Asset \[alm\_ai\_prompt\_digital\_asset\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="table_ifm_ncj_12c" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

object

</td><td>

Required. Content of the AI Prompt asset to update.Data type: Object

```
{
  "ai_model": "String",
  "description": "String",
  "documentation": "String",
  "managed_by": "String" 
  "name": "String",
  "prompt_info": "String", 
  "provider": "String",
  "state": Number,
  "version": "String"
} 
```

</td></tr><tr><td>

ai\_model

</td><td>

Value of the AI Model field of an existing record in the AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\] table.Valid values:

-   Name of the AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\] record
-   Sys\_id of the AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\] record

Data type: String

Default: empty string

</td></tr><tr><td>

description

</td><td>

Description to give the AI Prompt Product Model.Table: AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\]

Data type: String

Default: empty string

</td></tr><tr><td>

documentation

</td><td>

Documentation of the AI Prompt Product Model.Data type: String

Default: empty string

</td></tr><tr><td>

managed\_by

</td><td>

Value of the Managed by field of an existing record in the User \[sys\_user\] table.Valid values:

-   Name of the User \[sys\_user\] record
-   Sys\_id of the User \[sys\_user\] record

Data type: String

Default: empty string

</td></tr><tr><td>

name

</td><td>

Required. Name of the associated record in the AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\] table.Data type: String

Default: empty string

</td></tr><tr><td>

prompt\_info

</td><td>

Prompt information for AI Prompt Asset.Data type: String

Default: empty string

</td></tr><tr><td>

provider

</td><td>

Required. Value of the Provider field of an existing record in the Company \[core\_company\] table.Valid values:

-   Name of the Company \[core\_company\] record
-   Sys\_id of the Company \[core\_company\] record

Data type: String

</td></tr><tr><td>

state

</td><td>

State to apply to the AI Model Asset. For example, Valid values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

version

</td><td>

Version number to assign the AI Prompt Product Model. For example, `V2`.Data type: String

Default: empty string

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. Failed to fetch the asset with the given sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="table_ssp_xkw_5dc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

```
result: {
  "asset": {Object},
  "warnings": [Array]
}
```

</td></tr><tr><td>

result.asset

</td><td>

Details about the newly created entry.Data type: Object

```
"asset": {
  "ai_model": Object,
  "created": "String",
  "description": "String",
  "display_name": "String",
  "documentation": "String",
  "managed_by": Object,
  "name": "String",
  "prompt_info": "String",
  "provider": Object,
  "state": "String",
  "sys_id": "String",
  "updated": "String",
  "version": "String",
  "warnings": [Array]
}
```

</td></tr><tr><td>

result.asset.ai\_model

</td><td>

List of AI models in the AI System Asset \[cmdb\_ai\_ system\_asset\_model\] table record.Data type: Array

```
"ai_model": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.asset.ai\_models.name

</td><td>

Name of the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] table record.Data type: String

</td></tr><tr><td>

result.asset.ai\_models.sys\_id

</td><td>

Sys\_id of the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] table record.Data type: String

</td></tr><tr><td>

result.asset.created

</td><td>

Date and time that the AI model asset was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.asset.description

</td><td>

Description of the associated AI System Product Model record. Table: AI System Product Model \[cmdb\_ai\_system\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.display\_name

</td><td>

Display name of the AI System Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.documentation

</td><td>

Documentation of the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.asset.managed\_by

</td><td>

Details about the user who manages the asset.Data type: Object

```
"managed_by": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.asset.managed\_by.name

</td><td>

Name of the user who manages the AI model asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.asset.managed\_by.sys\_id

</td><td>

Sys\_id of the user who manages the AI model asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.asset.name

</td><td>

Name of the associated AI System Product Model record.Table: AI System Product Model \[cmdb\_ai\_system\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.prompt\_info

</td><td>

Prompt Information of the AI Prompt Asset record.Data type: String

</td></tr><tr><td>

result.asset.provider

</td><td>

Value of the Provider field in the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: Object

```
provider: {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.asset.provider.name

</td><td>

Name of the provider in the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.asset.provider.sys\_id

</td><td>

Sys\_id of the provider in the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.asset.state

</td><td>

State of the AI Model Asset. Possible values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

result.asset.sys\_id

</td><td>

Sys\_id of the AI System Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.updated

</td><td>

Date and time that the AI model asset was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.asset.version

</td><td>

Version number of the associated AI System Product Model record. For example, `V2`.Data type: String

</td></tr><tr><td>

result.warning

</td><td>

Comma-separated list of warning messages. These warnings can be validation checks, such as when the sys\_id of an optional parameter is invalid.Data type: Array

```
"warnings": ["String"]
```

</td></tr></tbody>
</table>### cURL request

The following example updates the data of the AI Prompt asset with the given sys\_id according to the provided parameter values in the request body.

```
curl -X PUT 'https://instance.servicenow.com/api/sn_ent/asset/ai_prompt/9833721b331e92101c9aca989d5c7bf0' \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -u 'username':'password' \
  -d '{
  "name": "Incident Summarization prompt1",
  "description": "Prompt for Incident Summarization",
  "provider": "servicenow",
  "version": "V1",
  "state": 31,
  "documentation": "Docuuu",
  "ai_model": "mixtral-instruct",
  "prompt_info": "Provide incident summary using short_decription, state, worknotes",
  "managed_by": "abel.tuter"
 }'
```

Response body:

```
{
  "result": {
    "asset": {
      "sys_id": "9833721b331e92101c9aca989d5c7bf0",
      "display_name": "ServiceNow Incident Summarization prompt1 V1",
      "name": "Incident Summarization prompt1",
      "description": "Prompt for Incident Summarization",
      "version": "V1",
      "provider": {
        "sys_id": "93d4ecfac0a8000b6294d71b733977fb",
        "name": "ServiceNow"
      },
      "documentation": "Docuuu",
      "state": "Deployed",
      "ai_model": {
        "sys_id": "9d7dc7e6eb1e5210aa82fab8bad0cda2",
        "name": "mixtral-instruct"
      },
      "prompt_info": "Provide incident summary using short_decription, state, worknotes",
      "managed_by": {
        "sys_id": "62826bf03710200044e0bfc8bcbe5df1",
        "name": "Abel Tuter"
      },
      "created": "2024-12-11 04:23:17",
      "updated": "2024-12-11 04:23:17"
    },
    "warnings": []
  }
}
```

## AI Assets API - PUT /sn\_ent/asset/ai\_system/\{sys\_id\}

Updates the data of a specific AI system record according to information you provide in the request body.

**Note:** Provide only the parameter-value pairs for the specific data you want to update. This endpoint overwrites the data for any parameters that are sent in the request.

### URL format

Versioned URL: `/api/sn_ent/{api_version}/asset/ai_system/{sys_id}`

Default URL: `/api/sn_ent/asset/ai_system/{sys_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="entry-ai-assetapi-systemID">

Sys\_id of the asset in the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="id_ary_vfj_12c" class="rest_api_request_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

object

</td><td>

Required. Details to update in the AI system.Data type: Object

```
{ 
  "name": "String", 
  "description": "String", 
  "provider": "String", 
  "version": "String", 
  "state": Number, 
  "documentation": "String", 
  "ai_models": "String", 
  "ai_prompts": "Strings", 
  "evaluation_datasets": [Array], 
  "evaluation_metrics_report": "String", 
  "managed_by": "String" 
}
```

</td></tr><tr><td>

object.name

</td><td>

Required. Name for the AI System Product Model.Data type: String

</td></tr><tr><td>

object.description

</td><td>

Description for the AI System Product Model.Data type: String

</td></tr><tr><td>

object.provider

</td><td>

Required. Value of the Provider field in an existing Company \[core\_company\] table record. Valid values:

-   Name of the Company \[core\_company\] record
-   Sys\_id of the Company \[core\_company\] record

Data type: String

</td></tr><tr><td>

object.state

</td><td>

State to apply to the AI System Asset. Valid values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

Default: empty string

</td></tr><tr><td>

object.version

</td><td>

Version for AI System Product Model. For example, `V2`.Data type: String

Default: empty string

</td></tr><tr><td>

object.documentation

</td><td>

Documentation of the AI System Asset.Data type: String

Default:

</td></tr><tr><td>

object.ai\_models

</td><td>

Comma-separated list of strings, where each string represents an AI Model field value of an existing AI Model Digital Asset record.Table: AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]

Valid values:

-   Name of the AI Model Digital Asset record.
-   Sys\_id of the AI Model Digital Asset record.

Data type: String

Default: empty string

</td></tr><tr><td>

object.evaluation\_datasets

</td><td>

Comma-separated list of AI datasets used for evaluating the AI System Asset record. Mostly applicable for models developed within an organization.Tables: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\], AI System Asset \[AI System Digital Asset alm\_ai\_system\_digital\_asset\]

Data type: Array

```
"evaluation_datasets": [{String", "String"}]
```

Valid values:

-   Name of the AI Dataset Digital Asset record.
-   Sys\_id of the AI Dataset Digital Asset record.

Default: empty string

</td></tr><tr><td>

object.evaluation\_metrics\_report

</td><td>

Reference to the evaluation results located within the text field of the AI system asset record. For example:```
Testing results:  link to the result document

Details:
Accuracy: 85%
Hallucination: 10%
Eval Run 1: link
Eval Run 2: link
```

Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

Default: empty string

</td></tr><tr><td>

object.managed\_by

</td><td>

Value of the 'Managed by' field of an existing User \[sys\_user\] table record. Valid values:

-   Name of the User \[sys\_user\] record
-   Sys\_id of the User \[sys\_user\] record

Data type: String

Default: empty string

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. Failed to fetch the asset with the given sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_gdt_wkm_ydc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Results of the updated AI System Asset.Data type: Object

```
"result": {
  "asset": Object,
  "warnings": [Array]
}
```

</td></tr><tr><td>

result.asset

</td><td>

Details about the newly created asset.Data type: Object

```
"asset": {
  "ai_model": [Array],
  "ai_prompts": [Array]
  "created": "String",
  "description": "String",
  "display_name": "String",
  "documentation": "String",
  "evaluation_datasets": Array,
  "evaluation_metrics_report": String,
  "managed_by": Object,
  "name": "String",
  "provider": Object,
  "state": "String",
  "sys_id": "String",
  "updated": "String",
  "version": "String",
  "warnings": [Array]
}
```

</td></tr><tr><td>

result.ai\_models

</td><td>

List of AI models in the AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] table record.Data type: Array

```
"ai_models": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.ai\_models.name

</td><td>

Name of the AI System Digital Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.ai\_models.sys\_id

</td><td>

Sys\_id of the AI System Digital Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.ai\_prompts

</td><td>

List of AI Prompts in the AI System Asset record.Data type: Array

```
"ai_prompts": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.ai\_prompts.name

</td><td>

Name of the AI prompt.Data type: String

</td></tr><tr><td>

result.ai\_prompts.sys\_id

</td><td>

Sys\_id of the AI Prompt Digital Asset record.Table: AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.created

</td><td>

Date and time that the AI model asset was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.asset.description

</td><td>

Description of the associated AI System Product Model record. Table: AI System Product Model \[cmdb\_ai\_system\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.display\_name

</td><td>

Display name of the AI System Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.documentation

</td><td>

Documentation of the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.asset.evaluation\_datasets

</td><td>

List of AI datasets used for evaluating the AI System Asset record. Mostly applicable for models developed within an organization.Tables: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\], AI System Asset \[alm\_ai\_system\_digital\_asset\]

Data type: Array

```
"evaluation_datasets": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.asset.evaluation\_datasets.name

</td><td>

Name of the AI Dataset Digital Asset.Data type: String

</td></tr><tr><td>

result.asset.evaluation\_datasets.sys\_id

</td><td>

Sys\_id of the AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\] table record.Data type: String

</td></tr><tr><td>

result.asset.evaluation\_metrics\_report

</td><td>

Evaluation results of the AI system asset.Possible values:

-   Details \(in plain text\) outlining results
-   Links to specific results

Data type: String

</td></tr><tr><td>

result.asset.managed\_by

</td><td>

Comma-separated list of sys\_ids or display names of AI datasets of the AI System Asset used for evaluating the model. Mostly applicable for models developed within an organization.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: Object

```
"managed_by": [
  {
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.asset.managed\_by.name

</td><td>

Sys\_id of the user who manages the AI model asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.asset.managed\_by.sys\_id

</td><td>

Name of the user who manages the AI model asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.asset.name

</td><td>

Name of the associated AI System Product Model record.Table: AI System Product Model \[cmdb\_ai\_system\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.provider

</td><td>

Value of the Provider field in the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: Object

```
provider: {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.asset.provider.name

</td><td>

Name of the provider in the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.asset.provider.sys\_id

</td><td>

Sys\_id of the provider in the associated AI System Product Model \[cmdb\_ai\_ system\_product\_model\] table record.Data type: String

</td></tr><tr><td>

result.asset.state

</td><td>

State of the AI Model Asset. Possible values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

result.asset.sys\_id

</td><td>

Sys\_id of the AI System Asset record.Table: AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.updated

</td><td>

Date and time that the AI model asset was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.asset.version

</td><td>

Version number of the associated AI System Product Model record. For example, `V2`.Data type: String

</td></tr><tr><td>

result.asset.warnings

</td><td>

Comma-separated list of warning messages. These warnings can be validation checks, such as when the sys\_id of an optional parameter is invalid.Data type: Array

```
"warnings": ["String"]
```

</td></tr></tbody>
</table>### cURL request

The following example updates the AI System with details to update in the request body.

```
curl -X PUT 'https://instance.servicenow.com/api/sn_ent/asset/ai_prompt/3b140397435a9210a63d00002fb8f2d7' \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d '{ 
  "name": "Incident Summarization", 
  "description": "Skill to summarize incident", 
  "provider": "servicenow", 
  "documentation": "Sample Documentation", 
  "version": "V3", 
  "state": 31, 
  "ai_models": [ 
    "llm_generic_small" 
  ], 
  "ai_prompts": [ 
    "LLM Prompt" 
  ], 
  "evaluation_datasets": [ 
    "Base dataset" 
  ], 
  "evaluation_metrics_report": "Sample Report", 
  "managed_by": "abel.tutor" 
}'
```

Response body shows the results of the update that was applied to the given AI system sys\_id.

```
{ 
  "result": { 
    "asset": { 
      "sys_id": "3b140397435a9210a63d00002fb8f2d7", 
      "display_name": "ServiceNow Incident Summarization V2", 
      "name": "Incident Summarization", 
      "description": "Skill to summarize incident", 
      "version": "V3", 
      "provider": { 
        "sys_id": "93d4ecfac0a8000b6294d71b733977fb", 
        "name": "ServiceNow" 
      }, 
      "documentation": "Sample Documentation", 
      "state": "Deployed", 
      "ai_models": [{  
       "sys_id": "9tgdc7e6eb1e5210aa82fab8bad0cda2",  
       "name": "llm_generic_small"  
     }], 
      "ai_prompts": [{  
       "sys_id": "7d7dc7e6eb1e5210aa82fab8bad0cda2",  
       "name": "LLM Prompt"  
     }], 
      "evaluation_datasets": [{  
       "sys_id": "9d7dc7e6eb1e5210aa82fab8bad0cda2",  
       "name": "Base dataset"  
     }], 
      "evaluation_metrics_report": "Sample Report", 
      "managed_by": { 
        "sys_id": "a8f98bb0eb32010045e1a5115206fe3a", 
        "name": "Abraham Lincoln" 
      }, 
      "created": "2024-12-11 19:07:13", 
      "updated": "2024-12-11 19:07:42" 
    }, 
    "warnings": [] 
  } 
}
```

## AI Assets API - PUT /sn\_ent/asset/ai\_model/\{sys\_id\}

Updates the data of a specific AI model asset record according to information you provide in the request body.

**Note:** Provide only the parameter-value pairs for specific data you want to update. This endpoint overwrites the data for all parameters that are sent in the request.

### URL format

Versioned URL: `/api/sn_ent/{api_version}/asset/ai_model/{sys_id}`

Default URL: `/api/sn_ent/asset/ai_model/{sys_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="entry-ai-assetapi-promptID">

Sys\_id of the asset in the AI Prompt Asset \[alm\_ai\_prompt\_digital\_asset\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

object

</td><td>

Required. Details to update in the given AI model.Data type: Object

```
{
  "base_model": "String",
  "context_window": "String",
  "deployment_guideline": "String",
  "description": "String",
  "documentation": "String",
  "evaluation_datasets": "String",
  "evaluation_metrics_report": "String",
  "managed_by": "String",
  "model_size_in_mb": "String",
  "model_weights_info": "String",
  "name": "String",
  "parameters_info": "String",
  "provider": "String",
  "required_infrastructure": "String",
  "state": Number,
  "supported_languages": "String",
  "training_datasets": "String",
  "training_procedure": "String",
  "version": "String"
} 
```

</td></tr><tr><td>

base\_model

</td><td>

AI model that this model version was derived from.**Note:** Only applicable for models developed within the organization.

Data type: Object

```
{
  "name": "String",
  "sys_id": "String"
 }
```

Default: empty object

</td></tr><tr><td>

base\_model.name

</td><td>

Name of the AI model asset to model this AI model after.Data type: String

</td></tr><tr><td>

base\_model.sys\_id

</td><td>

Sys\_id of the AI model asset to model this AI model after.Table: AI Model Digital Asset alm\_ai\_model\_digital\_asset

Data type: String

</td></tr><tr><td>

context\_window

</td><td>

Size of input sequences \(in other words, the number of tokens\) that the model can handle.Data type: Integer

Default: 0

</td></tr><tr><td>

deployment\_guideline

</td><td>

Instructions applicable for models developed and deployed within an organization.Data type: String

Default: empty

</td></tr><tr><td>

description

</td><td>

Description to give the AI Model Product Model. Updated in table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

Default: empty

</td></tr><tr><td>

documentation

</td><td>

Documentation of the AI Prompt Product Model record.Table: AI Prompt Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

Default: empty

</td></tr><tr><td>

evaluation\_datasets

</td><td>

Comma-separated list of sys\_ids or display names of AI datasets of the AI Prompt Digital Asset used for evaluating the model. Mostly applicable for models developed within an organization.Tables: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\], AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\]

Data type: Array

```
"evaluation_datasets": [
  "String",
  "String"
]
```

Valid values:

-   Name of the AI Dataset Digital Asset record.
-   Sys\_id of the AI Dataset Digital Asset record.

Default: empty string

</td></tr><tr><td>

evaluation\_metrics\_report

</td><td>

Reference to the evaluation results located within the text field of the AI Dataset Asset record. For example:```
Testing results:  link to the result document

Details:
Accuracy: 85%
Hallucination: 10%
Eval Run 1: link
Eval Run 2: link

```

Table: AI Dataset Asset \[alm\_ai\_dataset\_digital\_asset\]

Data type: String

Default: empty string

</td></tr><tr><td>

managed\_by

</td><td>

Value of the 'Managed by' field of an existing record in the User \[sys\_user\] table. Valid values:

-   Name of the User \[sys\_user\] record
-   Sys\_id of the User \[sys\_user\] record

Data type: String

Default: empty

</td></tr><tr><td>

model\_size\_in\_mb

</td><td>

Size of the model in MB. Mostly applicable for models developed and deployed within an organization.Data type: Number

Default: empty

</td></tr><tr><td>

model\_weights\_info

</td><td>

Additional model information, if available. Mostly applicable for models developed within an organization.Data type: String

Default: empty

</td></tr><tr><td>

name

</td><td>

Required. Name of the AI Model Product Model. Updated in table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

</td></tr><tr><td>

parameters\_info

</td><td>

Number of parameters to give to the model.Data type: String

Default: empty string

</td></tr><tr><td>

provider

</td><td>

Required. Value of the 'Provider' field of an existing Company \[core\_company\] table record. Assigns this provider to the new AI model.Valid values:

-   Name of the Company \[core\_company\] record
-   Sys\_id of the Company \[core\_company\] record

Data type: String

</td></tr><tr><td>

required\_infrastructure

</td><td>

Documentation of infrastructure needs for the model deployment. For example, details about the infrastructure stack and processing needs. Mostly applicable for models deployed within an organization.Data type: String

Default: empty

</td></tr><tr><td>

source

</td><td>

Details about the source of who or what created the model.Valid values:

-   Link to the source of the model. For example, `https://huggingface.co/mistralai/model1` or a link to Github.
-   Details of the source in plain text. For example, `Microsoft Azure`

Data type: String

Default: empty or null

</td></tr><tr><td>

state

</td><td>

State to apply to the AI Model Asset.Valid values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

supported\_languages

</td><td>

Comma-separated list of languages that are supported by the AI Model.Data type: Array

```
"supported_languages": [
  "String",
  "String"
]
```

Valid values:

-   Sys\_id of the Language \[sys\_language\] record
-   Name of the Language \[sys\_language\] record. For example, `"French", "English"`

Default: empty string

</td></tr><tr><td>

training\_datasets

</td><td>

Reference to 1+ associated datasets used for training the model. Comma-separated list of sys\_ids or display names of the AI Dataset Asset \[alm\_ai\_dataset\_digital\_asset\] table. Mostly applicable for models developed within an organization.Data type: Array

```
"training_datasets": [
  "String",
  "String"
]
```

Default: empty string

</td></tr><tr><td>

training\_procedure

</td><td>

Type of training to apply to the AI model.Valid values:

-   1: Decision Trees
-   2: Deep Neural Networks
-   3: Linear Regression
-   4: Logistic Regression
-   5: Random Forest
-   6: Supervised Learning
-   7: Unsupervised Learning
-   8: Reinforcement Learning
-   9: Transfer Learning
-   10: Semi-Supervised Learning
-   11: Instruction Finetuning
-   12: Supervised Finetuning

Data type: String represented with a number \(for example, `"3"`\)

Default: 1: Decision Trees

</td></tr><tr><td>

version

</td><td>

Version for AI Model Product Model. For example, `V2`.Data type: String

Default: empty

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

<table id="id_itx_mjj_12c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Results of the AI model asset creation.Data type: Object

```
"result": { 
    "asset": Object, 
    "warnings": [Array], 
 } 
```

</td></tr><tr><td>

result.asset

</td><td>

Details about the created AI model asset.Data type: Object

```
"asset": {
  "base_model": Object,
  "context_window": String,
  "created": "String",
  "deployment_guideline": String,
  "description": "String",
  "display_name": "String",
  "documentation": "String",
  "evaluation_datasets": Array,
  "evaluation_metrics_report": String,
  "managed_by": Object,
  "model_size_in_mb": String,
  "name": "String",
  "parameters_info": "String",
  "provider": Object,
  "required_infrastructure": String,
  "state": "String",
  "source": String, 
  "supported_languages": Array,
  "sys_id": "String",
  "training_datasets": Array,
  "training_procedure": String,
  "updated": "String",
  "version": "String"
}
```

</td></tr><tr><td>

result.asset.base\_model

</td><td>

Information about the AI model asset from which this version derived from.Data type: Object

```
"base_model": { 
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.asset.base\_model.name

</td><td>

Display name of AI model asset.Table: AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.base\_model.sys\_id

</td><td>

Sys\_id of AI model asset.Table: AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.context\_window

</td><td>

Size of input sequences that the model can handle. In other words, the number of tokens.Data type: String represented with a number. For example, `"6000"`.

</td></tr><tr><td>

result.asset.created

</td><td>

Date and time that the AI model asset was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.asset.deployment\_guideline

</td><td>

Instructions applicable for models developed and deployed within an organization.Data type: String

</td></tr><tr><td>

result.asset.description

</td><td>

Description of the associated AI Model Product Model record.Table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.display\_name

</td><td>

Display name of the AI Model Asset record.Table: AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\] \(display\_name field\)

Data type: String

</td></tr><tr><td>

result.asset.documentation

</td><td>

Documentation of the associated AI Model Product Model record.Table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.evaluation\_datasets

</td><td>

Comma-separated list of sys\_ids or display names of AI datasets of the AI Model Digital Asset used for evaluating the model. Mostly applicable for models developed within an organization.Tables: AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\], AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]

Data type: Array

```
"evaluation_datasets": [
  { 
  "name": "String",
  "sys_id": "String"
  } 
]
```

</td></tr><tr><td>

result.evaluation\_datasets.name

</td><td>

Name of the AI Dataset Digital Asset.Data type: String

</td></tr><tr><td>

result.evaluation\_datasets.sys\_id

</td><td>

Sys\_id of the AI Model Digital Asset record.Table: AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.evaluation\_metrics\_report

</td><td>

Reference to the evaluation results.Possible values:

-   Details \(in plain text\) outlining results
-   Links to specific results

Data type: String

</td></tr><tr><td>

result.asset.managed\_by

</td><td>

User that manages the AI model asset record.Data type: Object

```
" managed_by": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.asset.managed\_by.name

</td><td>

Name of the user who manages the AI model asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.asset.managed\_by.sys\_id

</td><td>

Sys\_id of the user who manages the AI model asset record.Table: User \[user\]

Data type: String

</td></tr><tr><td>

result.asset.model\_size\_in\_mb

</td><td>

Size of the model in MB. Usually applicable for models developed and deployed within an organization.Data type: Number

</td></tr><tr><td>

result.asset.name

</td><td>

Name of the associated AI Model Product Model record.Table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.provider

</td><td>

Provider of the associated AI Model Product Model record.Table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: Object

```
"provider": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.asset.provider.name

</td><td>

Name of the provider.Data type: String

</td></tr><tr><td>

result.asset.provider.sys\_id

</td><td>

Sys\_id of the record from Company \[core\_company\] table that corresponds to the Provider of the associated AI Model Product Model record.Table: AI Model Product Model \[cmdb\_ai\_model\_product\_model\]

Data type: String

</td></tr><tr><td>

result.asset.source

</td><td>

Details about the source of the asset.Valid values:

-   Link to the source of the model. For example, `https://huggingface.co/mistralai/Mixtral-8x7B-Instruct-v0.1` or a link to Github.
-   Details of the source in plain text. For example, `Microsoft Azure`

Data type: String

</td></tr><tr><td>

result.asset.state

</td><td>

State of the AI Model Asset record.Possible values:

-   1: In use
-   31: Deployed
-   32: Retired
-   33: Development
-   34: Unknown
-   35: N/A

Data type: String

</td></tr><tr><td>

result.asset.supported\_languages.name

</td><td>

Name of the supported language.Table: Language \[sys\_language\]

Data type: String

</td></tr><tr><td>

result.asset.supported\_languages.sys\_id

</td><td>

Sys\_id of the supported language.Table: Language \[sys\_language\]

Data type: String

</td></tr><tr><td>

result.asset.sys\_id

</td><td>

Sys\_id of the AI Model Asset record Table: AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]

Data type: String

</td></tr><tr><td>

result.asset.training\_datasets

</td><td>

Reference to 1+ associated data sets used for training the model.Data type: Array

```
"training_datasets": [
  { 
  "name": "String",
  "sys_id": "String"
  } 
]
```

</td></tr><tr><td>

result.asset.training\_procedure

</td><td>

Type of AI training applied to the model.Possible values:

-   1: Decision Trees
-   2: Deep Neural Networks
-   3: Linear Regression
-   4: Logistic Regression
-   5: Random Forest
-   6: Supervised Learning
-   7: Unsupervised Learning
-   8: Reinforcement Learning
-   9: Transfer Learning
-   10: Semi-Supervised Learning
-   11: Instruction Finetuning
-   12: Supervised Finetuning

Data type: String

</td></tr><tr><td>

result.asset.updated

</td><td>

Date and time that the AI model asset was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

result.asset.version

</td><td>

Version of the associated AI Model Product Model record.Table: AI Model Product Model \[cmdb\_ai\_model\_product\_model table\]

Data type: String

</td></tr><tr><td>

result.required\_infrastructure

</td><td>

Documentation of infrastructure needs for the model's deployment. For example, details about the infrastructure stack and processing needs.Data type: String

</td></tr><tr><td>

result.asset.parameters\_info

</td><td>

Properties of the training data that learn during the learning process. For example: `7B` or `30B`.Data type: String

</td></tr><tr><td>

result.asset.supported\_languages

</td><td>

Details about the languages supported by the AI model asset.Table: Language \[sys\_language\]

Data type: Object

```
"supported_languages": [
 { 
  "name": "String",
  "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.warnings

</td><td>

Comma-separated list of warning messages. These warnings can be validation checks, such as when the sysId of an optional parameter is invalid.Data type: Array

```
"warnings": ["String"]
```

</td></tr></tbody>
</table>### cURL request

The following example shows how to update a given AI asset model using the PUT method.

```
curl -X PUT 'https://instance.servicenow.com/api/sn_ent/asset/ai_model/9833721b331e92101c9aca989d5c7bf0' \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
-d '{ 
    "name": "Now LLM", 
    "description": "enables text-to-text like question answering and summarization", 
    "provider": "servicenow", 
    "documentation": "Now LLM V5 Documentation", 
    "version": "V8", 
    "parameters_info": "7B", 
    "supported_languages": [ 
        "English", 
        "French" 
    ], 
    "model_size_in_mb": "87", 
    "deployment_guideline": "Deployed on ServiceNow infrastructure", 
    "source": "huggingface.co/mistralai/Mixtral-8x7B-Instruct-v0.1", 
    "training_procedure": "2", 
    "context_window": "8000", 
    "state": "31", 
    "base_model": "Servicenow Now LLM V6", 
    "model_weights_info": "refer to weights and biases project", 
    "required_infrastructre": "GPUs needed: 1, GPU Type: A100", 
    "training_datasets": [ 
        "Servicenow Open Incidents" 
    ], 
    "evaluation_datasets": [ 
        "Servicenow Open Incidents" 
    ], 
    "evaluation_metrics_report": "Testing results: See files attached to this record", 
    "managed_by": "abel.tuter" 
}' 
```

Response body.

```
 { 
  "result": { 
    "asset": { 
      "sys_id": "a438d170ff96da10c1fbffffffffffd5", 
      "display_name": "ServiceNow Now LLM V6", 
      "name": "Now LLM", 
      "description": "enables text-to-text like question answering and summarization", 
      "version": "V8", 
      "provider": { 
        "sys_id": "93d4ecfac0a8000b6294d71b733977fb", 
        "name": "ServiceNow" 
      }, 
      "documentation": "Now LLM V5 Documentation", 
      "parameters_info": "7B", 
      "supported_languages": [ 
        { 
          "sys_id": "914493a30f320010e96b0e4fef767e90", 
          "name": "English" 
        } 
      ], 
      "model_size_in_mb": "87", 
      "deployment_guideline": "Deployed on ServiceNow infrastructure", 
      "source": "https://huggingface.co/mistralai/Mixtral-8x7B-Instruct-v0.1", 
      "training_procedure": "2", 
      "context_window": "8000", 
      "state": "Deployed", 
      "required_infrastructure": "undefined", 
      "base_model": { 
        "sys_id": "a438d170ff96da10c1fbffffffffffd5", 
        "name": "ServiceNow Now LLM V8" 
      }, 
      "evaluation_datasets": [ 
        { 
          "sys_id": "45cb45baff06d610c1fbffffffffffa9", 
          "name": "ServiceNow Open Incidents" 
        } 
      ], 
      "training_datasets": [ 
        { 
          "sys_id": "45cb45baff06d610c1fbffffffffffa9", 
          "name": "ServiceNow Open Incidents" 
        } 
      ], 
      "evaluation_metrics_report": "Testing results: See files attached to this record", 
      "managed_by": { 
        "sys_id": "62826bf03710200044e0bfc8bcbe5df1", 
        "name": "Abel Tuter" 
      }, 
      "created": "2024-12-03 16:50:53", 
      "updated": "2024-12-12 15:56:28" 
    }, 
    "warnings": [ 
      "Reference record 'French' not found for supported_languages in table sys_language" 
    ] 
  } 
} 
```

