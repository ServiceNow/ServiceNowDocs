---
title: Validating JSON payloads using TSOM Schema Validator
description: Use the TsomSchemaValidator utility class to validate JSON payloads against TSOM schemas before importing data. This helps identify errors early, reduce ETL failures, and confirm data quality.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Telecommunications Service Operations Management]
---

# Validating JSON payloads using TSOM Schema Validator

Use the TsomSchemaValidator utility class to validate JSON payloads against TSOM schemas before importing data. This helps identify errors early, reduce ETL failures, and confirm data quality.

Use this validator to check whether your JSON payloads conform to the expected schema for telco objects like Devices, Logical Connections, and Topologies before creating import sets. This pre-validation step helps to prevent schema mismatch errors and improves debugging.

## Supported schema types

The validator supports multiple schema types for different telco data structures:

-   Logical Composites - Representing groupings of components: Equipment, PDUs, Fan Shelves
-   Devices - Equipment and their contained components
-   Logical Connections - Connections between network interfaces
-   Port Relations - Relationships between network interfaces: physical, logical, lags
-   Logical Connection Relations - Relationships between logical connections
-   Topologies - Network topology

## Class structure

```
let TsomSchemaValidator = Class.create();
TsomSchemaValidator.prototype = {
initialize: function() {
this.schemas = new TsomGenericSchema();
},
isValidJson: function(payload) {
// Validation logic that determines if the JSON structure is valid
// Returns boolean (true/false)
},
checkJsonValidation: function(payload) {
// Validation logic that determines if the JSON structure is valid
// Returns a JSON object containing errors (if exist)
},
type: 'TsomSchemaValidator'
};
```

## Steps

1.  Instantiate the Schema ValidatorjavascriptCopyEdit

    ```
    var TsomSchemaValidator = new sn_tsom_core.TsomSchemaValidator();
    
    ```

2.  Run a Boolean Validation Check

    ```
    if (!TsomSchemaValidator.isValidJson(target_json)) {
        gs.error('Invalid JSON: ' + JSON.stringify(target_json));
        return;
    }
    
    ```

3.  Run a Detailed Validation Check

    ```
    let result = TsomSchemaValidator.checkJsonValidation(target_json);
    if (!result.valid) {
        gs.error('Invalid JSON: ' + JSON.stringify(result, null, 2));
        return;
    }
    
    ```


## Example output

```
Example Output
{
  "schemaName": "devices",
  "errors": [
    {
      "message": "Missing required property: model_name",
      "params": { "key": "model_name" },
      "code": 302,
      "dataPath": "/devices/0/ports/0",
      "schemaPath": "/properties/devices/items/properties/ports/items/required/4"
    }
  ],
  "valid": false
}

```

**Parent Topic:**[Using Telecommunications Service Operations Management](using-tsom.md)

**Related topics**  


[Configuring the Telecom Discovery Builder framework ETL in a connector](configuring-the-telco-generic-schema-etl.md)

[Telecom Discovery Builder framework](exploring-the-telco-generic-schema-etl-framework.md)

