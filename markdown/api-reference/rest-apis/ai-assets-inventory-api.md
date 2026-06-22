---
title: AI Assets Inventory API
description: The AI Assets Inventory APIs provide programmatic access to AI assets managed under the AI Control Tower application.Retrieves a paginated list of AI governance records of a given asset class, with optional filters, sorting, and pagination.Retrieves comprehensive details about a specific AI governance record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-apis/ai-assets-inventory-api.html
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-06-08"
reading_time_minutes: 18
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# AI Assets Inventory API

The AI Assets Inventory APIs provide programmatic access to AI assets managed under the AI Control Tower application.

The AI Assets Inventory endpoints enable:

-   Listing assets filtered by asset class with optional filtering, pagination, and sorting.
-   Retrieving detailed information about a specific asset including its related assets.
-   Querying governance data such as lifecycle phase, risk classification, and assessments \(when the GRC AI Governance plugin is active\).

The AI Assets Inventory API requires the sn\_ai\_governance.integration.rest role and the AI Governance \[sn\_ai\_governance\] plugin to access it. The GET /details endpoint requires the sn\_grc\_ai\_gov plugin to be active for Governance, Risk, and Compliance \(GRC\) lookups.

This API belongs to the sn\_ai\_governance namespace.

See [AI asset inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-inventory.md) for more information about managing AI assets inventory in the [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-control-tower-landing.md).

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/api-rest.md)

## AI Assets Inventory - GET /api/sn\_ai\_governance/assets/\{asset\_class\}

Retrieves a paginated list of AI governance records of a given asset class, with optional filters, sorting, and pagination.

Use this endpoint to:

-   Browse all AI assets of a specific class.
-   Filter assets by governance status, risk level, department, vendor, provider, etc.
-   Page through inventories for reporting purposes.

### URL format

Versioned URL: `/api/sn_ai_governance/{api_version}/assets/{asset_class}`

Default URL: `/api/sn_ai_governance/assets/{asset_class}`

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

asset\_class

</td><td>

Required. Asset class table name. The value is matched against the Model Categories table, asset\_class \[cmdb\_model\_category.asset\_class\] field.Valid table values:

-   `alm_ai_system_digital_asset`: AI Systems \(skills, agents, use cases\)
-   `alm_ai_model_digital_asset`: AI Models
-   `alm_ai_prompt_digital_asset`: AI Prompts
-   `alm_ai_dataset_digital_asset`: AI Datasets

Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

risk\_classification

</td><td>

Filters results by the risk score of the AI asset. Supports comma-separated values.Valid values:

-   `1`: High risk
-   `2`: Medium risk
-   `3`: Low risk
-   `4`: Unacceptable risk
-   `5`: To be determined \(default for new records\)
-   6: Critical

Data type: String as an integer

</td></tr><tr><td>

lifecycle\_status

</td><td>

Filters results by life cycle status of the AI asset.Valid values:

-   `1`: In review
-   `2`: Approved
-   `3`: Rejected
-   `4`: Deployed
-   `5`: AI steward review
-   `6`: Approved for development
-   `7`: Ready for deployment
-   `8`: Approved for deployment
-   `9`: Canceled
-   `10`: Offboarded

Data type: String

</td></tr><tr><td>

state

</td><td>

Filters results by the installation status of the AI asset. Values are instance-dependent. Refer to the install\_status field's choice list on the cmdb\_ci table in your instance to enumerate them. The platform default 'Installed' is typically value 1.Data type: String

</td></tr><tr><td>

asset\_type

</td><td>

Filter by model category name or sys\_id.Valid names:

-   AI System
-   AI Model
-   AI Prompt
-   AI Dataset
-   Generative AI
-   Agentic AI
-   Classic AI

These values are the canonical names referenced by the app and are stable across instances unless renamed.

Table: CMDB Model Category \[cmdb\_model\_category\] for name; AIGovernanceWsConstants.MODEL\_CATEGORIES for sys\_id.

Data type: String

</td></tr><tr><td>

lifecycle\_phase

</td><td>

Filter by lifecycle phase name or sys\_id.Valid name values:

-   Assess
-   New
-   Build and test
-   Build
-   Pre-deploy
-   Deploy
-   Offboard
-   Assess offboarding
-   Pre-offboarding

**Note:** Customer instances may add or rename these values. Refer to your instance's sn\_ai\_governance\_lifecycle table.

Table: AI Governance Lifecycle \[sn\_ai\_governance\_lifecycle\]

Data type: String

</td></tr><tr><td>

department

</td><td>

Filter by department name or sys\_id.Table: Department \[cmn\_department\]

Data type: String

</td></tr><tr><td>

managed\_by

</td><td>

Filter by user\_name or sys\_id of the user managing the asset.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

vendor

</td><td>

Filter by vendor company name or sys\_id.Table: Core Company \[core\_company\]

Data type: String

</td></tr><tr><td>

provider

</td><td>

Filter by provider/manufacturer name or sys\_id \(matched against the product model's manufacturer\).Table: Core Company \[core\_company\]

Data type: String

</td></tr><tr><td>

created\_from

</td><td>

Display date format of the calling user's session.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

created\_to

</td><td>

Display date format of the calling user's session.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

limit or sysparm\_limit

</td><td>

Number of records to return. If **limit** is missing, less than 1, or non-numeric, the configured default is used. If limit exceeds the configured maximum, it's silently capped to the maximum \(no warning\).Minimum: 1

Maximum: 500

Default: 100

Data type: Integer

</td></tr><tr><td>

offset or sysparm\_offset

</td><td>

Number of records to skip. If offset is missing or non-numeric, it's treated as 0; negative offsets are clamped to 0.Default: 0

Data type: Integer

</td></tr><tr><td>

sort\_by

</td><td>

Field to sort by. When sort\_by is not provided, results are ordered by sys\_created\_on descending \(newest first\). Valid values:

-   risk\_classification
-   lifecycle\_phase
-   lifecycle\_status
-   asset\_type
-   department
-   managed\_by
-   state
-   vendor
-   provider

Data type: String

</td></tr><tr><td>

order\_by

</td><td>

Sort direction. Case-insensitive. Only applied when sort\_by is provided and valid.Valid values:

-   `asc`: Ascending order
-   `desc`: Descending order

Default: `asc`

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sys\_id**

</td><td>

Sys ID of the governance record. Table: sn\_ai\_governance\_asset\_governance\_details

</td></tr><tr><td>

**asset\_name**

</td><td>

Display name of the underlying digital asset.Table/field: Asset \[asset\], display\_name

</td></tr><tr><td>

**asset\_type**

</td><td>

Name of the underlying asset's model category.Table/field: Asset Model Category \[asset.model\_category\], name

</td></tr><tr><td>

**created\_on**

</td><td>

Display value of the governance record's sys\_created\_on field.Table: sn\_ai\_governance\_asset\_governance\_details

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

Sys ID of the governance record. Table: sn\_ai\_governance\_asset\_governance\_details

</td></tr><tr><td>

asset\_name

</td><td>

Display name of the underlying digital asset.Table/field: Asset \[asset\], display\_name

</td></tr><tr><td>

asset\_type

</td><td>

Name of the underlying asset's model category.Table/field: Asset Model Category \[asset.model\_category\], name

</td></tr><tr><td>

created\_on

</td><td>

Display value of the governance record's sys\_created\_on field.Table: sn\_ai\_governance\_asset\_governance\_details

</td></tr></tbody>
</table>### Get All AI Systems

```
curl -X GET \ 
  'https://instance.service-now.com/api/sn_ai_governance/v1/assets/alm_ai_system_digital_asset' \ 
  -u 'username:password' \ 
  -H 'Accept: application/json'
```

```

```

### Get All AI Systems

```
curl -X GET \ 
  'https://instance.service-now.com/api/sn_ai_governance/v1/assets/alm_ai_system_digital_asset' \ 
  -u 'username:password' \ 
  -H 'Accept: application/json'
```

```

```

### Get High-Risk AI Systems in Production

```
curl -X GET \ 
  'https://instance.service-now.com/api/sn_ai_governance/v1/assets/alm_ai_system_digital_asset?risk_classification=1&lifecycle_phase=Deploy' \ 
  -u 'username:password' \ 
  -H 'Accept: application/json'
```

```

```

### Get AI Models with Pagination

```
curl -X GET \ 
  'https://instance.service-now.com/api/sn_ai_governance/v1/assets/alm_ai_model_digital_asset?limit=50&offset=0' \ 
  -u 'username:password' \ 
  -H 'Accept: application/json'
```

```

```

### Get AI Models with Pagination

```
curl -X GET \ 
  'https://instance.service-now.com/api/sn_ai_governance/v1/assets/alm_ai_model_digital_asset?limit=50&offset=0' \ 
  -u 'username:password' \ 
  -H 'Accept: application/json'
```

```

```

### Get AI Systems Created in a Date Range

```
curl -X GET \ 
  'https://instance.service-now.com/api/sn_ai_governance/v1/assets/alm_ai_system_digital_asset?created_from=2026-01-01&created_to=2026-01-31' \ 
  -u 'username:password' \ 
  -H 'Accept: application/json'
```

```

```

### Get AI Prompts by Department and Vendor

```
curl -X GET \ 
  'https://instance.service-now.com/api/sn_ai_governance/v1/assets/alm_ai_prompt_digital_asset?department=IT%20Department&vendor=ServiceNow' \ 
  -u 'username:password' \ 
  -H 'Accept: application/json'
```

```

```

### Get AI Systems Managed by a Specific User, Sorted by Department Descending

```
curl -X GET \ 
  'https://instance.service-now.com/api/sn_ai_governance/v1/assets/alm_ai_system_digital_asset?managed_by=jane.smith&sort_by=department&order_by=desc' \ 
  -u 'username:password' \ 
  -H 'Accept: application/json'
```

```

```

### Filter AI Models by Provider

```
curl -X GET \ 
  'https://instance.service-now.com/api/sn_ai_governance/v1/assets/alm_ai_model_digital_asset?provider=OpenAI' \ 
  -u 'username:password' \ 
  -H 'Accept: application/json'
```

```

```

### Get AI Systems Created in a Date Range

```
curl -X GET \ 
  'https://instance.service-now.com/api/sn_ai_governance/v1/assets/alm_ai_system_digital_asset?created_from=2026-01-01&created_to=2026-01-31' \ 
  -u 'username:password' \ 
  -H 'Accept: application/json'
```

```

```

## AI Assets Inventory - GET /api/sn\_ai\_governance/v1/assets/\{sys\_id\}/details

Retrieves comprehensive details about a specific AI governance record.

This endpoint retrieves the following record information for a single asset:

-   Basic asset information such as display name, asset class, asset type,
-   Life cycle phase and status, risk classification, state,
-   Related assets,
-   Governance, Risk, and Compliance \(GRC\) information \(assessments, risks, issues, policy exceptions\) when the sn\_grc\_ai\_gov plugin is active.

### URL format

Versioned URL: `/api/sn_ai_governance/{api_version}/assets/{sys_id}/details`

Default URL: `/api/sn_ai_governance/assets/{sys_id}/details`

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

</td><td>

Sys\_id of the governance record to retrieve.Table: AI Asset Governance Details \[sn\_ai\_governance\_asset\_governance\_details\]

**Note:** This isn't the sys\_id of the AI Dataset Digital Asset \[alm\_ai\_dataset\_digital\_asset\] table.

Data type: String

</td></tr><tr><td>

asset\_class

</td><td>

Required. Asset class table name. The value is matched against the Model Categories table, asset\_class \[cmdb\_model\_category.asset\_class\] field.Valid table values:

-   `alm_ai_system_digital_asset`: AI Systems \(skills, agents, use cases\)
-   `alm_ai_model_digital_asset`: AI Models
-   `alm_ai_prompt_digital_asset`: AI Prompts
-   `alm_ai_dataset_digital_asset`: AI Datasets

Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

include\_risk\_info

</td><td>

Optional. Flag that indicates whether to perform GRC plugin lookups, such as ai\_assessments, risk\_assessments, regulatory\_risk\_assessments, bulk\_risk\_assessments, control\_assessments, issues, policy\_exceptions, and risks. Has no effect when the sn\_grc\_ai\_gov plugin is inactive.Valid values:

-   true: Enables the lookup. Missing values or any other value \('true', 'False', '0'\) enables the lookup.
-   false: \(case sensitive\) Skips the lookup operation.

Default: true

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

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

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

**Sys\_id** or **asset\_class** path parameter missing or empty. Provide a valid **sys\_id** or **asset\_class** in the URL path.

</td></tr><tr><td>

401

</td><td>

Invalid or missing credentials. Check username/password or OAuth token.

</td></tr><tr><td>

403

</td><td>

Caller lacks the required role\(s\). Ensure the user holds the sn\_ai\_governance.integration.rest role.

</td></tr><tr><td>

404

</td><td>

Possible causes:

-   **asset\_class** doesn't match any Model Categories table, asset\_class \[cmdb\_model\_category.asset\_class\] value. Use one of the four documented **asset\_class** values.
-   No governance record exists for the given **sys\_id**. Verify the **sys\_id** is a row in the AI Asset Governance Details \[sn\_ai\_governance\_asset\_governance\_details\] table.

</td></tr><tr><td>

500

</td><td>

Unhandled exception. For example, invalid date format. Check logs to verify date inputs use the calling user's session date format.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

The top-level response shape is the same for all asset classes. The related\_assets object structure varies by asset class. See the **Related Assets** section for response parameters categorized by class.

<table id="table_z3q_jj4_njc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ai\_assessments

</td><td>

GRC AI assessments associated with this asset. Empty array if the GRC plugin isn't active or **include\_risk\_info** is `false`.Data type: Array of Objects

```

```

</td></tr><tr><td>

asset\_class

</td><td>

Table name \(sys\_class\_name\) of the digital asset.Valid values:

-   `alm_ai_system_digital_asset`: AI Systems \(sub\_ai\_systems, tools, ai\_models, ai\_prompts, evaluation\_datasets, input\_outputs, configuration\_items, business\_applications\)
-   `alm_ai_model_digital_asset`: AI Models \(derived\_ai\_models, training\_datasets, evaluation\_datasets, ai\_systems, input\_outputs, model\_lineages, configuration\_items, business\_applications\)
-   `alm_ai_prompt_digital_asset`: AI Prompts \(ai systems\)
-   `alm_ai_dataset_digital_asset`: AI Datasets \(ai\_systems, ai\_models, parent\_datasets, child\_datasets\)

Data type: String

</td></tr><tr><td>

asset\_type

</td><td>

Display value of the asset's model\_category.Data type: String

</td></tr><tr><td>

bulk\_risk\_assessments

</td><td>

GRC bulk risk assessments. Same conditions as **ai\_assessments**.Data type: Array of Objects

```
"bulk_risk_assessments": [
 {
  } 
]
```

</td></tr><tr><td>

control\_assessments

</td><td>

GRC controls.Data type: Array of Objects

```
"control_assessments": [
 {
  } 
]
```

</td></tr><tr><td>

display\_name

</td><td>

Display name of the underlying digital asset.Data type: String

</td></tr><tr><td>

issues

</td><td>

GRC issues associated with this asset.Data type: Array of Objects

```
"issues": [
 {
  } 
]
```

</td></tr><tr><td>

lifecycle\_phase

</td><td>

Life cycle phase of the asset.Data type: Object

```
"lifecycle_phase": {
  "sys_id": "String",
  "name":   "String"
}
```

</td></tr><tr><td>

lifecycle\_phase.sys\_id

</td><td>

Sys\_id of the life cycle phase record.Data type: String

</td></tr><tr><td>

lifecycle\_phase.name

</td><td>

Display value of the life cycle phase record.Data type: String

</td></tr><tr><td>

lifecycle\_status

</td><td>

Raw stored integer value of the status field on the governance record. This is the choice value, not the display label. Refer to the status field's choice list to enumerate values. Data type: String

</td></tr><tr><td>

policy\_exceptions

</td><td>

GRC policy exceptions.Data type: Array of Objects

```
"policy_exceptions": [
 {
  } 
]
```

</td></tr><tr><td>

regulatory\_risk\_assessments

</td><td>

GRC regulatory risk classifications. Same conditions as ai\_assessments.Data type: Array of Objects

```
"regulatory_risk_assessments": [
 { 
  } 
]
```

</td></tr><tr><td>

related\_assets

</td><td>

Related-asset groupings; structure depends on asset\_class. returns different fields depending on the asset\_class of the requested governance record. See the Related Assets section for associated parameters organized by asset type.Data type: Object

```
"related_assets": [
 {
  } 
]
```

</td></tr><tr><td>

risk\_assessments

</td><td>

GRC risk assessments. Same conditions as ai\_assessments.Data type: Array of Objects

```
"risk_assessments": [
 {
  } 
]
```

</td></tr><tr><td>

risk\_classification

</td><td>

Display value of risk\_score on the governance record.Possible values:

-   `1`: High risk
-   `2`: Medium risk
-   `3`: Low risk
-   `4`: Unacceptable risk
-   `5`: To be determined \(default for new records\)
-   6: Critical

Data type: String

</td></tr><tr><td>

risks

</td><td>

GRC risks.Data type: Array of Objects

```
"risks": [
 {
  } 
]
```

</td></tr><tr><td>

state

</td><td>

Install status on the linked digital asset. The serialized value reflects the raw integer \(for example, 1\), not the display label.**Note:** This differs from the state field inside related\_assets items, which returns the display value.

Data type: String

</td></tr></tbody>
</table>### Related Assets

The **related\_assets** object returns different fields depending on the asset\_class of the requested governance record. Each table documents the fields returned for that asset class, along with the structure of each item in the returned array.

**Note:** For related assets that have a governance record,

-   **sys\_id** is the governance record's sys\_id \(not the digital asset's sys\_id\),
-   **name** is the governance display value,
-   additional governance fields \(**risk\_classification**, **lifecycle\_status**, **lifecycle\_phase**, **state**\) are included.

When no governance record exists, only the base fields are returned.

<table id="table_zz3_c14_njc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ai\_models

</td><td>

AI Models referenced from the system's ai\_models field.Data type: Object

```
ai_models: [
  {
    "sys_id": "String",
    "name": "String",
    "asset_class": "String",
    "asset_type": "String",
    // Governance fields (when record exists):
    "risk_classification": "String",
    "lifecycle_status": "String",
    "lifecycle_phase": "String",
    "state": "String"
  }
]
```

</td></tr><tr><td>

ai\_prompts

</td><td>

AI Prompts referenced from the system's ai\_prompts field.Data type: Object

```
ai_prompts: [
  {
   "sys_id": "String",
   "name": "String",
   "asset_class": "String",
   "asset_type": "String",
   // Governance fields (when record exists):
   "risk_classification": "String",
   "lifecycle_status": "String",
   "lifecycle_phase": "String",
   "state": "String"
  }
]
```

</td></tr><tr><td>

business\_applications

</td><td>

Business applications mapped to this asset's product model via the Product Model Map \[sn\_apm\_ws\_ba\_product\_model\_map\] table. Returned only if that table exists in the instance.Data type: Object

```
business_applications: [
{
 "sys_id": "String",
 "name": "String"
 }
]
```

</td></tr><tr><td>

configuration\_items

</td><td>

CIs related to this digital asset via the Asset-CI Relationship \[cmdb\_rel\_asset\_ci\] table.Data type: Object

```
configuration_items: [
 {
  "sys_id": "String",
  "name":   "String"
 }
]
```

</td></tr><tr><td>

evaluation\_datasets

</td><td>

AI datasets referenced from the system's evaluation\_datasets field.Data type: Object

```
evaluation_datasets: [
  {
    "sys_id": "String",
    "name": "String",
    "asset_class": "String",
    "asset_type": "String",
    // Governance fields (when record exists):
    "risk_classification": "String",
    "lifecycle_status": "String",
    "lifecycle_phase": "String",
    "state": "String"
  }
]
```

</td></tr><tr><td>

input\_outputs

</td><td>

Input/output specifications for this system from the \[AI Input Output\] sn\_ent\_ai\_input\_output table, ordered by io\_category.Data type: Object

```
input_outputs: [
  {
    "sys_id": "String",
    "name": "String",
    "description": "String",
    "io_type": "String",
    "information_object": "String"
  }
]
```

</td></tr><tr><td>

sub\_ai\_systems

</td><td>

AI Systems registered as subcomponents of this system, sourced from the AI System Subcomponent Map \[sn\_ent\_ai\_system\_subcomponent\_m2m\] table where `ai_subcomponent_reference_table = alm_ai_system_digital_asset`.When a governance record exists for the related asset, the governance record's sys\_id, name, and governance fields are included. When no governance record exists, only the base fields are returned.

Data type: Array of Objects

```
sub_ai_systems: [
  {
   "sys_id": "String",
   "name": "String",
   "description": "String",
   "asset_class": "String",
   // Governance fields (when record exists):
   "risk_classification": "String",
   "lifecycle_status": "String",
   "lifecycle_phase": "String",
   "state": "String"
  }
]
```

</td></tr><tr><td>

tools

</td><td>

Enterprise AI tools registered as subcomponents, sourced the AI System Subcomponent Map \[sn\_ent\_ai\_system\_subcomponent\_m2m\] table where `ai_subcomponent_reference_table = sn_ent_ai_tool`.Data type: Array of Objects

```
tools: [
  {
    "sys_id": "String",
    "name": "String",
    "description": "String",
    "asset_class": "String",
    // Governance fields (when record exists):
    "risk_classification": "String",
    "lifecycle_status": "String",
    "lifecycle_phase": "String",
    "state": "String"
  }
]
```

</td></tr></tbody>
</table><table id="table_rnd_5b4_njc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

derived\_ai\_models

</td><td>

AI Models whose base\_model points to this model.Data type: Array of Objects

```
derived_ai_models: [
  {
    "sys_id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

training\_datasets

</td><td>

Datasets referenced from this model's training\_datasets field.Data type: Array of Objects

```
training_datasets: [
  {
    "sys_id": "String",
    "name":   "String"
  }
]
```

</td></tr><tr><td>

evaluation\_datasets

</td><td>

Datasets referenced from this model's evaluation\_datasets field.Data type: Array of Objects

```
evaluation_datasets: [
  {
    "sys_id": "String",
    "name":   "String"
  }
]
```

</td></tr><tr><td>

ai\_systems

</td><td>

AI Systems whose ai\_models field contains this model.Data type: Array of Objects

```
ai_systems: [
  {
    "sys_id": "String",
    "name":   "String"
  }
]
```

</td></tr><tr><td>

input\_outputs

</td><td>

Input/output specifications.Table: AI Input Output \[sn\_ent\_ai\_input\_output\] table, Category \[io\_category\] field

Data type: Array of Objects

```
input_outputs: [
  {
    "sys_id": "String",
    "name": "String",
    "description": "String",
    "io_type": "String",
    "information_object": "String"
  }
]
```

</td></tr><tr><td>

model\_lineages

</td><td>

Models of this type.Table: AI Model Lineage \[sn\_ent\_ai\_model\_lineage\], AI model digital asset \[ai\_model\] column

Data type: Array of Objects

```
model_lineages: [
  {
    "sys_id": "String",
    "dataset":  "String",
    "activity": "String",
    "training_procedure": "String",
    "model_checkpoint_id": "String",
    "user_group": "String",
    "start_time": "String",
    "end_time": "String"
  }
]
```

</td></tr><tr><td>

configuration\_items

</td><td>

CIs related to this digital asset.Table: Asset-CI Relationship \[cmdb\_rel\_asset\_ci\]

Data type: Array of Objects

```
configuration_items: [
  {
    "sys_id": "String",
    "name":   "String"
  }
]
```

</td></tr><tr><td>

business\_applications

</td><td>

Business applications mapped to this asset's product model, if the Product Model Map \[sn\_apm\_ws\_ba\_product\_model\_map\] table exists in the instance.Data type: Array of Objects

```
business_applications: [
  {
    "sys_id": "String",
    "name":   "String"
  }
]
```

</td></tr></tbody>
</table><table id="table_ll5_hc4_njc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ai\_systems

</td><td>

AI Systems whose ai\_prompts field contains this prompt.Data type: Array of Objects

```
ai_systems: [
  {
    "sys_id": "String",
    "name":   "String"
  }
]
```

</td></tr></tbody>
</table><table id="table_zyf_qc4_njc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ai\_systems

</td><td>

AI Systems whose evaluation\_datasets field contains this dataset.Data type: Array of Objects

```
ai_systems: [
  {
    "sys_id": "String",
    "name":   "String"
  }
]
```

</td></tr><tr><td>

ai\_models

</td><td>

AI Models whose training\_datasets or evaluation\_datasets field contains this dataset.Data type: Array of Objects

```
ai_models: [
  {
    "sys_id": "String",
    "name":   "String"
  }
]
```

</td></tr><tr><td>

parent\_datasets

</td><td>

Datasets referenced from this dataset's base\_datasets field.Data type: Array of Objects

```
parent_datasets: [
  {
    "sys_id": "String",
    "name":   "String"
  }
]
```

</td></tr><tr><td>

child\_datasets

</td><td>

Datasets whose base\_datasets field contains this dataset.Data type: Array of Objects

```
child_datasets: [
  {
    "sys_id": "String",
    "name":   "String"
  }
]
```

</td></tr></tbody>
</table>### Get AI System details

Request to retrieve **asset\_class** `alm_ai_system_digital_asset` details:

```
curl -X GET \
  'https://instance.service-now.com/api/sn_ai_governance/v1/assets/a1b2c3d4e5f6a1b2c3d4e5f6a1b2c3d4/details' \
  -u 'username:password' \
  -H 'Accept: application/json'
```

Response body:

```
{
  "display_name": "Customer Service AI Assistant", 
  "asset_type": "Generative AI", 
  "asset_class": "alm_ai_system_digital_asset", 
  "lifecycle_status": "2", 
  "lifecycle_phase": { "sys_id": "lifecycle123", "name": "Production" }, 
  "state": "1", 
  "risk_classification": "medium", 
  "related_assets": { 
    "sub_ai_systems": [ 
      { 
        "sys_id": "govSub123", 
        "name": "FAQ Handler Sub-Agent", 
        "description": "Handles frequently asked questions", 
        "asset_class": "alm_ai_system_digital_asset", 
        "risk_classification": "low", 
        "lifecycle_status": "2", 
        "lifecycle_phase": "Production", 
        "state": "Active" 
      } 
    ], 
    "tools": [ 
      { 
        "sys_id": "tool123", 
        "name": "Knowledge Base Search", 
        "description": "Searches internal knowledge base", 
        "asset_class": "sn_ent_ai_tool" 
      } 
    ], 
    "ai_models": [ 
      { "sys_id": "govModel123", "name": "GPT-4", 
        "asset_class": "alm_ai_model_digital_asset", "asset_type": "Generative AI", 
        "risk_classification": "1", "lifecycle_status": "2", 
        "lifecycle_phase": "Production", "state": "Active" } 
    ], 
    "ai_prompts": [ 
      { "sys_id": "govPrompt123", "name": "Customer Service Greeting Prompt", 
        "asset_class": "alm_ai_prompt_digital_asset", "asset_type": "Prompt" } 
    ], 
    "evaluation_datasets": [ 
      { "sys_id": "govDataset123", "name": "CS Evaluation Dataset", 
        "asset_class": "alm_ai_dataset_digital_asset", "asset_type": "Dataset" } 
    ], 
    "input_outputs": [ 
      { "sys_id": "io123", "name": "Customer Query", 
        "description": "Natural language customer question", 
        "io_type": "Input", "information_object": "Text" }, 
      { "sys_id": "io456", "name": "AI Response", 
        "description": "AI-generated response to customer", 
        "io_type": "Output", "information_object": "Text" } 
    ], 
    "configuration_items": [ 
      { "sys_id": "ci123", "name": "CS AI Assistant CI" } 
    ], 
    "business_applications": [ 
      { "sys_id": "ba123", "name": "Customer Service Platform" } 
    ] 
  }, 
  "ai_assessments": [], 
  "risk_assessments": [], 
  "regulatory_risk_assessments": [], 
  "bulk_risk_assessments": [], 
  "control_assessments": [], 
  "issues": [], 
  "policy_exceptions": [], 
  "risks": [] 
}
```

### Get AI Model details \(skip GRC data\)

Request to retrieve **asset\_class** `alm_ai_model_digital_asset` details:

```
curl "https://instance.servicenow.com/api/sn_ent/asset/ai_system/3b140397435a9210a63d00002fb8f2d7" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Response body:

```
{
  "display_name": "GPT-4 Turbo", 
  "asset_type": "AI Model", 
  "asset_class": "alm_ai_model_digital_asset", 
  "lifecycle_status": "2", 
  "lifecycle_phase": { "sys_id": "lifecycle456", "name": "Production" }, 
  "state": "1", 
  "risk_classification": "1", 
  "related_assets": { 
    "derived_ai_models": [ 
      { "sys_id": "derived123", "name": "GPT-4 Turbo Fine-tuned for CS" } 
    ], 
    "training_datasets": [ 
      { "sys_id": "train123", "name": "General Training Dataset" } 
    ], 
    "evaluation_datasets": [ 
      { "sys_id": "eval123", "name": "Model Evaluation Dataset" } 
    ], 
    "ai_systems": [ 
      { "sys_id": "sys123", "name": "Customer Service AI Assistant" } 
    ], 
    "input_outputs": [], 
    "model_lineages": [ 
      { 
        "sys_id": "lineage123", 
        "dataset": "Training Dataset v2.0", 
        "activity": "Fine-tuning", 
        "training_procedure": "Supervised Learning", 
        "model_checkpoint_id": "checkpoint_42", 
        "user_group": "AI Team", 
        "start_time": "2026-01-10 08:00:00", 
        "end_time": "2026-01-12 18:30:00" 
      } 
    ], 
    "configuration_items": [ 
      { "sys_id": "ciModel1", "name": "GPT-4 Turbo CI" } 
    ], 
    "business_applications": [ 
      { "sys_id": "baModel1", "name": "AI Platform" } 
    ] 
  }, 
  "ai_assessments": [], 
  "risk_assessments": [], 
  "regulatory_risk_assessments": [], 
  "bulk_risk_assessments": [], 
  "control_assessments": [], 
  "issues": [], 
  "policy_exceptions": [], 
  "risks": [] 
}
```

### Get AI Prompt details

Request to retrieve **asset\_class** `alm_ai_prompt_digital_asset` details:

```
curl -X GET \
  'https://instance.service-now.com/api/sn_ai_governance/v1/assets/e5f6a1b2c3d4e5f6a1b2c3d4e5f6a1b2/details' \
  -u 'username:password' \
  -H 'Accept: application/json'
```

Respone body:

```
{ 
  "display_name": "Customer Greeting Prompt", 
  "asset_type": "AI Prompt", 
  "asset_class": "alm_ai_prompt_digital_asset", 
  "lifecycle_status": "2", 
  "lifecycle_phase": { "sys_id": "lifecycle789", "name": "Production" }, 
  "state": "Active", 
  "risk_classification": "low", 
  "related_assets": { 
    "ai_systems": [ 
      { "sys_id": "sys123", "name": "Customer Service AI Assistant" } 
    ] 
  }, 
  "ai_assessments": [], 
  "risk_assessments": [], 
  "regulatory_risk_assessments": [], 
  "bulk_risk_assessments": [], 
  "control_assessments": [], 
  "issues": [], 
  "policy_exceptions": [], 
  "risks": [] 
}
```

### Get AI Dataset details

Request to retrieve **asset\_class** `alm_ai_dataset_digital_asset` details:

```
curl -X GET \
  'https://instance.service-now.com/api/sn_ai_governance/v1/assets/d4e5f6a1b2c3d4e5f6a1b2c3d4e5f6a1/details' \
  -u 'username:password' \
  -H 'Accept: application/json'
```

Response body:

```
{ 
  "display_name": "Customer Service Evaluation Dataset", 
  "asset_type": "AI Dataset", 
  "asset_class": "alm_ai_dataset_digital_asset", 
  "lifecycle_status": "2", 
  "lifecycle_phase": { "sys_id": "lifecycle321", "name": "Production" }, 
  "state": "Active", 
  "risk_classification": "low", 
  "related_assets": { 
    "ai_systems": [ 
      { "sys_id": "sys123", "name": "Customer Service AI Assistant" } 
    ], 
    "ai_models": [ 
      { "sys_id": "model123", "name": "GPT-4" } 
    ], 
    "parent_datasets": [ 
      { "sys_id": "parent123", "name": "Base CS Dataset" } 
    ], 
    "child_datasets": [ 
      { "sys_id": "child123", "name": "Extended CS Dataset v2" } 
    ] 
  }, 
  "ai_assessments": [], 
  "risk_assessments": [], 
  "regulatory_risk_assessments": [], 
  "bulk_risk_assessments": [], 
  "control_assessments": [], 
  "issues": [], 
  "policy_exceptions": [], 
  "risks": [] 
}
```

### Quick Command Reference

List all AI systems:

```
curl -X GET 'https://instance.service-now.com/api/sn_ai_governance/v1/assets/alm_ai_system_digital_asset'
 -u 'user:password' 
```

Get high-risk assets:

```
curl -X GET 'https://instance.service-now.com/api/sn_ai_governance/v1/assets/alm_ai_system_digital_asset?risk_classification=1'
 -u 'user:password' 
```

Get asset details \(skip GRC data\):

```
curl -X GET 'https://instance.service-now.com/api/sn_ai_governance/v1/assets/{sys_id}/details'
 -u 'user:password'
```

Paginate results:

```
curl -X GET 'https://instance.service-now.com/api/sn_ai_governance/v1/assets/alm_ai_system_digital_asset?limit=100&offset=0'
 -u 'user:password'
```

