---
title: sn\_erp\_integration API - Scoped, Global
description: Script include providing a chainable API for interacting with Zero Copy Connector for ERP \(Enterprise Resource Planning\) models.Initializes a new Zero Copy Connector for ERP API instance.Filters records using an encoded query.Add an OR query condition.Add a query condition for filtering data.Executes the configured operation.Specifies the model fields to return. This is the primary method for field selection.Alias for the execute\(\) method for retrieving a single record in the results.Gets the available IDoc configuration details for the selected system.Returns a list of all available input fields for the selected operation.Returns a list of available models for the selected system.Gets the available operations for the selected model.Gets a list of all available output fields for the selected operation.Gets a list of all available ERP systems that can be accessed through the API.Returns of list of only the required input fields for the selected model and create operation.Selects an IDoc configuration to operate on.Limits the number of results returned.Selects a model to operate on.Sets the starting offset for results.Selects an operation to use on a selected model.Sets a single field value for create or update operations.Selects a system to operate on.Sets JSON data for the operation. For read operations, this method sets filter conditions. For create or update operations, this method sets the fields with data to be created or updated.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# sn\_erp\_integration API- Scoped, Global

Script include providing a chainable API for interacting with Zero Copy Connector for ERP \(Enterprise Resource Planning\) models.

This script include requires the Zero Copy Connector for ERP \(com.sn\_erp\_integration\) store application and is provided within the sn\_erp\_integration namespace. For more information, refer to [Zero Copy Connector for ERP](https://www.servicenow.com/docs/access?context=erp-integration-overview&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

Role required: sn\_erp\_integration.erp\_user

-   **Metadata**

    Use metadata methods to discover the system, model, and IDoc information available in your Zero Copy Connector for ERP environment.

    -   getAvailableSystems\(\)
    -   getAvailableModels\(\)
    -   getAvailableOperations\(\)
    -   getAvailableInputs\(\)
    -   getRequiredInputs\(\)
    -   getAvailableOutputs\(\)
    -   getAvailableIdocConfigs\(\)
-   **Configuration**

    Use configuration methods to select available systems, models, operations, and IDoc configurations for processing. You can also use these methods to filter model field return values.

    -   system\(\)
    -   model\(\)
    -   operation\(\)
    -   idocConfig\(\)
    -   fields\(\)
    -   limit\(\)
    -   offset\(\)
-   **Query building**

    Use query building methods to filter results.

    -   addEncodedQuery\(\)
    -   addQuery\(\)
    -   addOrQuery\(\)
-   **Data input**

    Use the data input methods to set field values. The withJSON\(\)method can be used for input on nested objects and IDoc fields. The set\(\) method is used to set a single field value.

    -   set\(\)
    -   withJSON\(\)
-   **Operation execution**

    Use the execute\(\) method when working with multiple records, and the get\(\) method for results of a single record.

    -   execute\(\)
    -   get\(\)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## API - API constructor

Initializes a new Zero Copy Connector for ERP API instance.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following examples show how to create an instance of the API to access an ERP system.

```
// Select the system1 system
const api = new sn_erp_integration.API().system('system1');
```

## API - addEncodedQuery\(String encodedQuery\)

Filters records using an encoded query.

See also:

-   [API - addOrQuery\(String field, String operator, String value\)](sn_erp_integrationBothAPI.md#)
-   [API - addQuery\(String field, String operator, String value, String joinType\)](sn_erp_integrationBothAPI.md#)
-   [API - fields\(Array fields\)](sn_erp_integrationBothAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|encodedQuery|String|An [encoded query string](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).|

|Type|Description|
|----|-----------|
|Object|Returns this instance for chaining.|

The following example shows how to use an encoded query to retrieve company codes in the US.

```
const api = new sn_erp_integration.API()
  .system('system1')
  .model('company_code')
  .operation('read')
  .addEncodedQuery('company_codes_countryregion_key=US')
  .execute();
```

## API - addOrQuery\(String field, String operator, String value\)

Add an OR query condition.

See also:

-   [API - addEncodedQuery\(String encodedQuery\)](sn_erp_integrationBothAPI.md#)
-   [API - addQuery\(String field, String operator, String value, String joinType\)](sn_erp_integrationBothAPI.md#)
-   [API - fields\(Array fields\)](sn_erp_integrationBothAPI.md#)

<table id="table_qkt_53x_3hc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

field

</td><td>

String

</td><td>

The name of the field to be queried.

</td></tr><tr><td>

operator

</td><td>

String

</td><td>

Optional. Query operator. The query option used depends on whether data provided for the *value* parameter is a number or string.Default value: =

Numbers:

-   =
-   !=
-   &gt;
-   &gt;=
-   &lt;
-   &lt;=

Strings \(must be in upper case\):

-   =
-   !=
-   IN
-   NOT IN
-   STARTSWITH
-   ENDSWITH
-   CONTAINS
-   DOES NOT CONTAIN

**Note:** Use CONTAINS instead of the LIKE operator.

</td></tr><tr><td>

value

</td><td>

String

</td><td>

Value on which to query \(not case-sensitive\).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Returns this instance for chaining.|

The following example shows how to return all company codes in the US and Canada.

```
const api = new sn_erp_integration.API();
const companyCodes = api
  .system('system1')
  .model('company_code')
  .operation('read')
  .addQuery('company_codes_countryregion_key', 'US')
  .addOrQuery('company_codes_countryregion_key', 'CA')
  .fields(['company_codes_company_code', 'company_codes_company_name', 'company_codes_countryregion_key', 'company_codes_currency'])
  .execute();

// Process the results
companyCodes.forEach(companyCode => {
  gs.info('Company Code: ${companyCode.company_codes_company_code}, Name: ${companyCode.company_codes_company_name}, Country: ${companyCode.company_codes_countryregion_key}');
  
  // Do something with each company code
  if (companyCode.company_codes_countryregion_key === 'US') {
    // Process US company codes
  } else {
    // Process Canadian company codes
  }
});
```

## API - addQuery\(String field, String operator, String value, String joinType\)

Add a query condition for filtering data.

See also:

-   [API - addEncodedQuery\(String encodedQuery\)](sn_erp_integrationBothAPI.md#)
-   [API - addOrQuery\(String field, String operator, String value\)](sn_erp_integrationBothAPI.md#)
-   [API - fields\(Array fields\)](sn_erp_integrationBothAPI.md#)

<table id="table_qkt_53x_3hc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

field

</td><td>

String

</td><td>

The name of the field to be queried.

</td></tr><tr><td>

operator

</td><td>

String

</td><td>

Optional. Query operator. The query option used depends on whether data provided for the *value* parameter is a number or string.Default value: =

Numbers:

-   =
-   !=
-   &gt;
-   &gt;=
-   &lt;
-   &lt;=

Strings \(must be in upper case\):

-   =
-   !=
-   IN
-   NOT IN
-   STARTSWITH
-   ENDSWITH
-   CONTAINS
-   DOES NOT CONTAIN

**Note:** Use CONTAINS instead of the LIKE operator.

</td></tr><tr><td>

value

</td><td>

String

</td><td>

Value on which to query \(not case-sensitive\).

</td></tr><tr><td>

joinType

</td><td>

String

</td><td>

Optional. Join type.Possible values:

-   AND
-   OR

Default value: AND

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Returns this instance for chaining.|

The following example shows how to use the &gt; operator to return results that are priority one or a priority greater than two.

```
// Results in: priority=1^ORpriority>2
const api = new sn_erp_integration.API();
  .system('system1')
  .model('request')
  .operation('read')
  .addQuery('priority', '1)
  .addOrQuery('priority', '>', '2')
  .execute();
```

## API - execute\(\)

Executes the configured operation.

To execute an operation on a single result, use [API - get\(\)](sn_erp_integrationBothAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object\|Array|The result of the operation. Error if unsuccessful.|

The following example shows how to create a new company code.

```
const newCompanyCode = new sn_erp_integration.API()
  .system('system1')
  .model('company_code')
  .operation('create')
  .withJSON({
    company_codes_company_code: '1234',
    company_codes_company_name: 'New York Office',
    company_codes_countryregion_key: 'US',
    company_codes_language_key: 'EN'
  })
  .execute();
```

## API - fields\(Array fields\)

Specifies the model fields to return. This is the primary method for field selection.

To retrieve a list of fields available for a model, use [API - getAvailableOutputs\(\)](sn_erp_integrationBothAPI.md#).

See also:

-   [API - limit\(Number max\)](sn_erp_integrationBothAPI.md#)
-   [API - offset\(Number start\)](sn_erp_integrationBothAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|fields|Array|One or more model field names listed as strings.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to return specific fields for all company codes in the US.

```
const companyCodes = new API()
  .system('system1')
  .model('company_code')
  .operation('read')
  .addQuery('company_codes_countryregion_key', 'US')
  .fields(['company_codes_company_code', 'company_codes_company_name', 'company_codes_countryregion_key'])
  .execute();
```

## API - get\(\)

Alias for the execute\(\) method for retrieving a single record in the results.

See also [API - execute\(\)](sn_erp_integrationBothAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|The first result of the operation.|

The following example shows how to retrieve a specific sales document.

```
const salesDoc = new sn_erp_integration.API()
  .system('system1')
  .model('sales_document')
  .operation('read')
  .addQuery('document_number', '0000123456')
  .get();
```

## API - getAvailableIdocConfigs\(\)

Gets the available IDoc configuration details for the selected system.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rkt_53x_3hc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array of objects

</td><td>

List of available IDoc configurations. Throws an error if no system has been selected.See also [API - system\(String systemId\)](sn_erp_integrationBothAPI.md#).

</td></tr><tr><td>

object.id

</td><td>

IDoc ID. Use this value to select an IDoc with the [API - idocConfig\(String configId\)](sn_erp_integrationBothAPI.md#) method.Data type: String

</td></tr><tr><td>

object.name

</td><td>

IDoc display name.Data type: String

</td></tr><tr><td>

object.description

</td><td>

Description of the IDoc.Data type: String

</td></tr></tbody>
</table>The following example shows how to get all available IDoc configurations for a selected system.

```
const idocConfigs = new sn_erp_integration.API()
  .system('system1')
  .getAvailableIdocConfigs();

gs.info(JSON.stringify(idocConfigs, null, 2));
```

Output:

```
[
  {
    "id": "OBC0001002",
    "name": "Sales Order IDoc",
    "description": "IDoc for sales order processing"
  },
  {
    "id": "OBC0001003",
    "name": "Material IDoc",
    "description": "IDoc for material core data"
  }
]
```

## API - getAvailableInputs\(\)

Returns a list of all available input fields for the selected operation.

For a list of only the required input fields for a selected model, use the [API - getRequiredInputs\(\)](sn_erp_integrationBothAPI.md#) method.

See also:

-   [API - addEncodedQuery\(String encodedQuery\)](sn_erp_integrationBothAPI.md#)
-   [API - addOrQuery\(String field, String operator, String value\)](sn_erp_integrationBothAPI.md#)
-   [API - addQuery\(String field, String operator, String value, String joinType\)](sn_erp_integrationBothAPI.md#)
-   [API - system\(String systemId\)](sn_erp_integrationBothAPI.md#)
-   [API - withJSON\(Object data\)](sn_erp_integrationBothAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rkt_53x_3hc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object describing available inputs and their types.See also [API - system\(String systemId\)](sn_erp_integrationBothAPI.md#).

</td></tr><tr><td>

object.variable\_name

</td><td>

Variable name of the input field.Data type: String

</td></tr><tr><td>

object.label

</td><td>

Display name of the input field.Data type: String

</td></tr><tr><td>

object.data\_type

</td><td>

Data type of the operation input.Data type: String

</td></tr><tr><td>

object.required

</td><td>

Flag that indicates whether the input field is required.Valid values:

-   true: The input field is required.
-   false: The input field isn’t required.

Data type: Boolean

</td></tr></tbody>
</table>Get available inputs for creating a company code.

```
const inputs = new sn_erp_integration.API()
  .system('system1')
  .model('company_code')
  .operation('read')
  .getAvailableInputs();

gs.info(JSON.stringify(operations, null, 2));
```

Output:

```
[
  {
    "variable_name": "company_codes_company_code",
    "label": "Company Code",
    "data_type": "string",
    "required": true
  },
  {
    "variable_name": "company_codes_company_name",
    "label": "Company Name",
    "data_type": "string",
    "required": true
  }
]
```

## API - getAvailableModels\(\)

Returns a list of available models for the selected system.

For more information, see

-   [API - model\(String modelId\)](sn_erp_integrationBothAPI.md#)
-   [Building and managing models to work with ERP data](https://www.servicenow.com/docs/access?context=work-with-erp-data-models&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rkt_53x_3hc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array of objects

</td><td>

List of available models listed as a JSON object with an ID, name, and description property. Throws an error if no system has been selected.See also [API - system\(String systemId\)](sn_erp_integrationBothAPI.md#).

</td></tr><tr><td>

object.id

</td><td>

Model ID. Use this value to select a model with the [API - model\(String modelId\)](sn_erp_integrationBothAPI.md#) method.Data type: String

</td></tr><tr><td>

object.name

</td><td>

Model label, that is, the display name.Data type: String

</td></tr><tr><td>

object.description

</td><td>

Description of the model.Data type: String

</td></tr></tbody>
</table>The following example shows how to retrieve all available models for a selected system.

```
// Get all available models for system1
const models = new sn_erp_integration.API()
  .system('system1')
  .getAvailableModels();

gs.info(JSON.stringify(models, null, 2));
```

Output:

```
[
  {
    "id": "company_code",
    "name": "Company Code",
    "description": "Company Code"
  },
  {
    "id": "country",
    "name": "Country",
    "description": "Country"
  },
  {
    "id": "currency",
    "name": "Currency",
    "description": "Currency"
  },
  {
    "id": "customer_invoice",
    "name": "Customer Invoice",
    "description": "Customer Invoice"
  },
  {
    "id": "language",
    "name": "Language",
    "description": "Language"
  }
]
```

## API - getAvailableOperations\(\)

Gets the available operations for the selected model.

See also:

-   [API - model\(String modelId\)](sn_erp_integrationBothAPI.md#)
-   [API - operation\(String operationId\)](sn_erp_integrationBothAPI.md#)
-   [API - system\(String systemId\)](sn_erp_integrationBothAPI.md#)
-   [Building and managing models to work with ERP data](https://www.servicenow.com/docs/access?context=work-with-erp-data-models&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rkt_53x_3hc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

List of available ERP model operations. Throws an error if no model or system has been selected.

</td></tr><tr><td>

object.id

</td><td>

Model operation ID. Use this value to select a model operation with the [API - operation\(String operationId\)](sn_erp_integrationBothAPI.md#) method.Data type: String

</td></tr><tr><td>

object.name

</td><td>

Model operation label, that is, the display name.Data type: String

</td></tr></tbody>
</table>The following example shows how to get all available operations for the **company\_code** model.

```
const operations = new sn_erp_integration.API()
  .system('system1')
  .model('company_code')
  .getAvailableOperations();

gs.info(JSON.stringify(operations, null, 2));
```

Output:

```
[
  {
    "id": "create",
    "name": "Company Code - Create"
  },
  {
    "id": "read",
    "name": "Company Code - Read"
  }
]
```

## API - getAvailableOutputs\(\)

Gets a list of all available output fields for the selected operation.

The field names returned by this method can be used with the [API - fields\(Array fields\)](sn_erp_integrationBothAPI.md#) method to filter field results.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rkt_53x_3hc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array of objects

</td><td>

List of available output fields. Throws an error if no model or system has been selected.See also [API - system\(String systemId\)](sn_erp_integrationBothAPI.md#).

</td></tr><tr><td>

object.variable\_name

</td><td>

Variable name of the output field.Data type: String

</td></tr><tr><td>

object.label

</td><td>

Display name of the output field.Data type: String

</td></tr><tr><td>

object.data\_type

</td><td>

Data type of the operation output.Data type: String

</td></tr></tbody>
</table>The following example shows how to get the available output provided by reading a model operation called **vendor**.

```
// Get available outputs for read operation on a vendor model
const outputs = new sn_erp_integration.API()
  .system('system1')
  .model('vendor')
  .operation('read')
  .getAvailableOutputs();

gs.info(JSON.stringify(outputs, null, 2));
```

Output:

```
[
  {
    "variable_name": "supplier_country",
    "label": "Country",
    "data_type": "string"
  }
  {
    "variable_name": "supplier_city",
    "label": "City",
    "data_type": "string"
  },
  {
    "variable_name": "supplier_location",
    "label": "Location",
    "data_type": "string"
  },
  {
    "variable_name": "supplier_street",
    "label": "Street",
    "data_type": "string"
  },
  {
    "variable_name": "supplier_name",
    "label": "Name",
    "data_type": "string"
  },
  {
    "variable_name": "supplier_postal_code",
    "label": "Postal Code",
    "data_type": "string"
  },
  {
    "variable_name": "supplier_state",
    "label": "State",
    "data_type": "string"
  }
]
```

## API - getAvailableSystems\(\)

Gets a list of all available ERP systems that can be accessed through the API.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rkt_53x_3hc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array of objects

</td><td>

List of available ERP systems.

</td></tr><tr><td>

object.id

</td><td>

System ID. Use this value to select a system with the [API - system\(String systemId\)](sn_erp_integrationBothAPI.md#) method.Data type: String

</td></tr><tr><td>

object.name

</td><td>

System label, that is, the display name.Data type: String

</td></tr></tbody>
</table>The following example shows how to get a list of all available ERP systems.

```
const systems = new sn_erp_integration.API().getAvailableSystems();

gs.info(JSON.stringify(systems));
```

Output:

```
[
  {
    "id": "system1",
    "name": "SAP DEV"
  },
  {
    "id": "system2",
    "name": "SAP PROD"
  }
]
```

## API - getRequiredInputs\(\)

Returns of list of only the required input fields for the selected model and create operation.

Required input fields are set when models are created.

For a complete list of input fields for a selected model, use the [API - getAvailableInputs\(\)](sn_erp_integrationBothAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rkt_53x_3hc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array of objects

</td><td>

List of required input field names.

</td></tr><tr><td>

object.variable\_name

</td><td>

Variable name of the required input field.Data type: String

</td></tr><tr><td>

object.label

</td><td>

Display name of the required input field.Data type: String

</td></tr><tr><td>

object.data\_type

</td><td>

Data type of the operation required input.Data type: String

</td></tr><tr><td>

object.required

</td><td>

Flag that indicates whether the input field is required. This method only returns results if the value is true.Data type: Boolean

</td></tr></tbody>
</table>The following example shows how to return the required input fields for creating an invoice.

```
const requiredInputs = new sn_erp_integration.API()
  .system('system1')
  .model('invoice')
  .operation('create')
  .getRequiredInputs();

gs.info(JSON.stringify(requiredInputs, null, 2));
```

Output:

```
{
  "variable_name": "INVOICE01",
  "label": "INVOICE01",
  "data_type": "array",
  "required": true
}
```

## API - idocConfig\(String configId\)

Selects an IDoc configuration to operate on.

See also:

-   [Outbound message configuration fields](https://www.servicenow.com/docs/access?context=erp-canvas-add-new-outbound-message-configuration-fields&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)
-   [Outbound message IDoc status for IDoc log tab fields](https://www.servicenow.com/docs/access?context=erp-canvas-outbound-message-idoc-status-for-idoc-log-tab-columns&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

|Name|Type|Description|
|----|----|-----------|
|configId|String|ID of the IDoc outbound configuration. To retrieve a list of IDoc configuration IDs, use the [API - getAvailableIdocConfigs\(\)](sn_erp_integrationBothAPI.md#) method.|

|Type|Description|
|----|-----------|
|Object|Returns this instance for chaining.|

The following example shows how to select an IDoc configuration and set values for processing.

```
const api = new sn_erp_integration.API()
  .system('system1')
  .idocConfig('OBC0001002')
  .withJSON({
    idoc_field1: 'value1',
    idoc_field2: 'value2'
  })
  .execute();
```

## API - limit\(Number max\)

Limits the number of results returned.

|Name|Type|Description|
|----|----|-----------|
|max|Number|Maximum number of records to return.|

|Type|Description|
|----|-----------|
|Object|Returns this instance for chaining.|

The following example shows how to retrieve only the first 10 company code records.

```
// Get only the first 10 company codes
const api = new sn_erp_integration.API()
  .system('system1')
  .model('company_code')
  .fields(['company_codes_company_code', 'company_codes_company_name'])
  .limit(10)
  .execute();
```

## API - model\(String modelId\)

Selects a model to operate on.

<table id="table_qkt_53x_3hc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

modelId

</td><td>

String

</td><td>

The ID of the model.To retrieve a list of all models with their IDs, use [API - getAvailableModels\(\)](sn_erp_integrationBothAPI.md#).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Returns this instance for chaining.|

The following example shows how to select the company\_code model in system1. You can chain additional methods for getting and setting data for the selected model.

```
const api = new sn_erp_integration.API()
  .system('system1')
  .model('company_code')
  .execute();
```

## API - offset\(Number start\)

Sets the starting offset for results.

|Name|Type|Description|
|----|----|-----------|
|start|Number|Starting point at which to begin retrieving results. For example, setting this value to 10 skips the first 10 results returned in a query.|

|Type|Description|
|----|-----------|
|Object|Returns this instance for chaining.|

The following example shows how to retrieve 10 company code records skipping the first 10 results \(11-20\).

```
const api = new sn_erp_integration.API()
  .system('system1')
  .model('company_code')
  .fields(['company_codes_company_code', 'company_codes_company_name'])
  .limit(10)
  .offset(10)
  .execute();
```

## API - operation\(String operationId\)

Selects an operation to use on a selected model.

To return a list of model operations, use [API - getAvailableOperations\(\)](sn_erp_integrationBothAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|operationId|String|The ID of the model operation.|

|Type|Description|
|----|-----------|
|Object|Returns this instance for chaining.|

The following example shows how to select the read operation for the **company\_code** model.

```
const api = new sn_erp_integration.API()
  .system('system1')
  .model('company_code')
  .operation('read')
  .execute();
```

## API - set\(String field, String value\)

Sets a single field value for create or update operations.

|Name|Type|Description|
|----|----|-----------|
|field|String|Name of the field on which to set a value.|
|value|String|Value to set for the field.|

|Type|Description|
|----|-----------|
|Object|Returns this instance for chaining.|

The following example shows how to create a company code entry and assign field values to it.

```
const api = new sn_erp_integration.API()
  .system('system1')
  .model('company_code')
  .operation('create')
  .set('company_codes_company_code', '1234')
  .set('company_codes_company_name', 'New York Office')
  .set('company_codes_countryregion_key', 'US')
  .set('company_codes_language_key', 'EN')
  .execute();
```

The following example shows how to update a sales document with nested properties. For nested data structures with additional levels, use [API - withJSON\(Object data\)](sn_erp_integrationBothAPI.md#).

```
const api = new sn_erp_integration.API()
  .system('system1')
  .model('sales_document')
  .operation('update')
  .set('document_number', '0000123456')
  .set('header.document_type', 'OR')
  .set('header.sales_organization', '1000')
  .execute();
```

## API - system\(String systemId\)

Selects a system to operate on.

See also:

-   [API - getAvailableSystems\(\)](sn_erp_integrationBothAPI.md#)
-   [API - model\(String modelId\)](sn_erp_integrationBothAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|systemId|String|The system ID. You can retrieve the system ID using the [API - getAvailableSystems\(\)](sn_erp_integrationBothAPI.md#) method.|

|Type|Description|
|----|-----------|
|Object|Returns this instance for chaining.|

The following example shows how to select a system. You can chain additional methods to select a model within the system, and additional methods for using data on the selected system.

```
const api = new sn_erp_integration.API().system('system1');
```

## API - withJSON\(Object data\)

Sets JSON data for the operation. For read operations, this method sets filter conditions. For create or update operations, this method sets the fields with data to be created or updated.

See also [API - set\(String field, String value\)](sn_erp_integrationBothAPI.md#).

<table id="table_qkt_53x_3hc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Object

</td><td>

JSON data listing fields and their values.Format:

```
{fieldname: 'value'}
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Returns this instance for chaining.|

The following example shows how to set data for a create operation.

```
const api = new sn_erp_integration.API()
  .system('system1')
  .model('company_code')
  .operation('create')
  .withJSON({
    company_codes_company_code: '1234',
    company_codes_company_name: 'New York Office',
    company_codes_countryregion_key: 'US'
  })
  .execute();
```

The following example shows how to set a nested filter for a read operation.

```
const api = new sn_erp_integration.API()
  .system('system1')
  .model('sales_document')
  .operation('read')
  .withJSON({
    header: {
      document_type: 'OR',
      sales_organization: '1000'
    }
  })
  .operation('read')
  .execute();
```

