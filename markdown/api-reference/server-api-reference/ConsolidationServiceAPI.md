---
title: ConsolidationService - Scoped, Gobal
description: The ConsolidationService API is a script include with methods for merging and de-duplicating complex, hierarchical business data \(such as contracts, quotes, line items, and entitlements\) using custom logic.Overridable method for specifying which child entity types can be consolidated within a JSON. The base implementation returns false for all entity types if not overridden.Overridable method that adds conditions for determining whether two entity JSONs with the same hash can be consolidated. The base implementation returns false if not overridden.Overridable method for specifying which child entity types can be merged from source JSONs into the target JSON. The base implementation returns false for all entity types if not overridden.Merges source entity JSON\(s\) into a target entity JSON and consolidates child entities within the merged result based on hash-based grouping and pairwise consolidation logic.Overridable method that controls whether consolidation is enabled for this service instance. The base implementation returns false if not overridden. Implementing classes must override this method to return true to enable consolidation.Overridable method that returns the hash configuration for grouping entities before consolidation. The configuration specifies which attributes and child context types generate an MD5 hash for each entity. Entities with the same hash are grouped for pairwise consolidation. The base implementation returns an empty object when not overridden.Overridable method to determine the primary JSON when two JSONs are being consolidated. For non-overridden attributes, the primary JSON's attribute values are used on the consolidated result. The base implementation returns json1 if not overridden.Overridable method, called after two JSONs are consolidated, for updating attributes on the consolidated JSON. The base implementation is a no-op if not overridden.Overridable method that applies final modifications to the consolidated JSON after hierarchy consolidation is complete. The base implementation is a no-op if not overridden.Overridable method called before merge and consolidation for performing custom pre-processing tasks such as bulk map creation or caching lookup data.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 21
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ConsolidationService- Scoped, Gobal

The ConsolidationService API is a script include with methods for merging and de-duplicating complex, hierarchical business data \(such as contracts, quotes, line items, and entitlements\) using custom logic.

This API belongs to the sn\_l2c\_core namespace, and requires the admin role and the Lead to Cash Core \(com.snc.l2c\_core\) plugin to access it.

Use the ConsolidationService API when you need precise control over how records are combined. This API provides complex functionality not available on the UI, such as:

-   Defining what makes two records the same across multiple attributes or nested child entities.
-   Conditionally merging records when certain criteria are met.
-   Applying custom calculations during consolidation, like summing quantities or calculating date ranges.
-   Recursively deduplicating \(consolidating\) deeply nested child structures.
-   Reusing the same consolidation logic consistently across flows and integrations.

The ConsolidationService is part of the Lead to Cash Core primitives engine and is accessed via the Lead to Cash Core product.

## Before you begin

Before implementing ConsolidationService, ensure you have:

-   The Lead to Cash Core plugin \(`com.snc.l2c_core`\) installed and the `admin` role.
-   A custom script include that extends `sn_l2c_core.LeadToCashService` and returns your `ConsolidationService` implementation from `getConsolidationService()`. This wires your consolidation logic into the pipeline so it's resolved by PrimitiveUtil at runtime.
-   Familiarity with PrimitiveUtil, which is the entry point for invoking L2C Core primitives including consolidation.

ConsolidationService is part of the Lead to Cash Core \(l2c\) Core primitives engine. Before implementing this API, you should understand how it fits into the broader invocation pipeline.

PrimitiveUtil is the runtime entry point for all L2C Core primitive operations, including consolidation. Rather than invoking ConsolidationService directly, PrimitiveUtil uses an extension point mechanism to resolve the correct service implementation at runtime, whether triggered from a server-side script or a Lead-to-Cash Flow Designer primitive.

To wire your ConsolidationService logic into this pipeline, you must create a custom script include that extends sn\_l2c\_core.LeadToCashService and returns your ConsolidationService implementation from getConsolidationService\(\). PrimitiveUtil checks the extension point registry for a custom LeadToCashService at runtime and invokes it if one is found. If no custom implementation is registered, PrimitiveUtil falls back to the base sn\_l2c\_core.LeadToCashService automatically. You never need to instantiate or reference this fallback directly in your code.

## ConsolidationServiceSNC API extension and workflow

The ConsolidationServiceSNC API's base system is disabled by default to ensure that unwanted consolidation isn't applied unknowingly. To enable consolidation actions, you must create custom logic and optionally override methods provided with the ConsolidationServiceSNC script include.

To extend and use the ConsolidationServiceSNC API:

1.  Required. Create a custom script include that extends sn\_l2c\_core.ConsolidationService.
2.  Required. Override enableConsolidation\(\) to return `true`. This flag enables the system to allow consolidation on your service. Example script:

    ```
    var MyConsolidationService = Class.create();
    MyConsolidationService.prototype = Object.extendsObject(
        sn_l2c_core.ConsolidationService,
    {
        enableConsolidation: function () {
            return true; // REQUIRED
        },
    
        type: 'MyConsolidationService'
    });
    ```

3.  Depending on the entities you want to control, optionally override \(or enable\) any number of these additional methods:

    **Note:** If you don’t override any methods, `consolidate()` returns the target JSON unchanged with no merging or consolidation performed.

    |Method|Action|
    |------|------|
    |canConsolidateEntity\(contextType\)|Choose which child arrays to consolidate within a target.|
    |canMergeEntity\(contextType\)|Merge source children into a target.|
    |getHashConfig\(\)|Specify how entities are grouped \(hashing\).|
    |canConsolidateJSONs\(json1, json2\)|Decide if two JSONs should merge.|
    |overrideAttributeValues\(\)|Apply custom business logic after a merge and before the final consolidated JSON continues through the workflow.|
    |getPrimary\(json1, json2\)|Decides which of the two entities is treated as the primary record during consolidation, whose attribute values are retained by default in the merged result.|
    |preProcess\(\)|Pre-hook for computing data.|
    |postHierarchyConsolidation\(\)|Post-hook for final cleanup.|

4.  Return your custom ConsolidationService from sn\_l2c\_core.LeadToCashService. `LeadToCashService` is the entry point that wires your consolidation logic into the Lead‑to‑Cash pipeline so that it's actually used whenever consolidation is invoked. Example script:

    ```
    var MyLeadToCashService = Class.create();
    MyLeadToCashService.prototype = Object.extendsObject(
        sn_l2c_core.LeadToCashService,
    {
        getConsolidationService: function () {
            return new MyConsolidationService();
        },
    
        type: 'MyLeadToCashService'
    });
    ```

5.  Invoke your consolidation by calling LeadToCashService.consolidate\(\) either directly from a server‑side script or indirectly via Lead‑to‑Cash Flow Designer primitives.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ConsolidationService - canConsolidateEntity\(String contextType\)

Overridable method for specifying which child entity types can be consolidated within a JSON. The base implementation returns `false` for all entity types if not overridden.

|Name|Type|Description|
|----|----|-----------|
|contextType|String|The key name of the array property on the entity JSON representing the child entity type. Examples: `"lineItems"`, `"characteristics"`, `"coveredProducts"`.|

<table id="table_t2c_sbh_53c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag indicating whether consolidation is possible on the selected entity type.Valid values:

-   true: Groups entities of this type by hash and consolidates them.
-   false: Doesn't consolidate entities of this type.

Default: false

</td></tr></tbody>
</table>The following example shows how to override canConsolidateEntity\(\) to enable consolidation for line items and covered products.

```
var MyConsolidationService = Class.create();

MyConsolidationService.prototype = Object.extendsObject(sn_l2c_core.ConsolidationService, {
    enableConsolidation: function() {
        return true;
    },

    canConsolidateEntity: function(contextType) {
        return contextType == "lineItems" || contextType == "coveredProducts";
    },

    type: 'MyConsolidationService'
});

var service = new MyConsolidationService();

gs.info("Can consolidate lineItems = " + service.canConsolidateEntity("lineItems"));

gs.info("Can consolidate characteristics = " + service.canConsolidateEntity("characteristics"));
```

Output:

```
Can consolidate lineItems = true
Can consolidate characteristics = false
```

## ConsolidationService - canConsolidateJSONs\(Object json1, Object json2\)

Overridable method that adds conditions for determining whether two entity JSONs with the same hash can be consolidated. The base implementation returns false if not overridden.

|Name|Type|Description|
|----|----|-----------|
|json1|Object|First entity JSON to compare. Contains sys\_id, table, attributes, and child arrays.|
|json2|Object|Second entity JSON to compare. Contains sys\_id, table, attributes, and child arrays.|

<table id="table_szb_ndh_53c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the two JSONs can be consolidated into one.Valid values:

-   true: Both JSONs can be merged via consolidateJSONs\(\).
-   false: Both JSONs remain separate.

Default: false

</td></tr></tbody>
</table>This example shows how to override canConsolidateJSONs\(\) to allow consolidation of line items with the same product offering.

```
var MyConsolidationService = Class.create();

MyConsolidationService.prototype = Object.extendsObject(sn_l2c_core.ConsolidationService, {

    enableConsolidation: function() {

        return true;

    },

    canConsolidateJSONs: function(json1, json2) {

        if (json1.table == "sn_quote_mgmt_core_quote_line_item") {

            // Fall back to empty string if product_offering has no value
            var po1 = json1.attributes.product_offering ? json1.attributes.product_offering.value : "";

            // Fall back to empty string if product_offering has no value
            var po2 = json2.attributes.product_offering ? json2.attributes.product_offering.value : "";

            // Consolidate only if both line items share the same product offering, and that value is not empty
            return po1 == po2 && po1 != "";

        }

        return false;

    },

    type: 'MyConsolidationService'

});
```

Output:

```
false
```

## ConsolidationService - canMergeEntity\(String contextType\)

Overridable method for specifying which child entity types can be merged from source JSONs into the target JSON. The base implementation returns false for all entity types if not overridden.

|Name|Type|Description|
|----|----|-----------|
|contextType|String|The key name of the array property on the entity JSON representing the child entity type. Examples: `"lineItems"`, `"characteristics"`, `"coveredProducts"`.|

<table id="table_cqd_1dh_53c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicate whether entities of this type can be merged from source to target.Valid values:

-   true: The system concatenates source arrays of this type into the target's corresponding array.
-   false: The system doesn't merge source arrays of this type into the target.

Default: false

</td></tr></tbody>
</table>The following example shows how to override canMergeEntity\(\) to enable merging for line items and covered products.

```
var MyConsolidationService = Class.create();

MyConsolidationService.prototype = Object.extendsObject(sn_l2c_core.ConsolidationService, {


    enableConsolidation: function() {

        return true;

    },


    canMergeEntity: function(contextType) {

        return contextType == "lineItems" || contextType == "coveredProducts";

    },


    type: 'MyConsolidationService'

});


var service = new MyConsolidationService();

gs.info("Can merge lineItems = " + service.canMergeEntity("lineItems"));

gs.info("Can merge characteristics = " + service.canMergeEntity("characteristics"));
```

Output:

```
Can merge lineItems = true
Can merge characteristics = false
```

## ConsolidationService - consolidate\(Object sourceJSON, Object targetJSON, Object additionalParams\)

Merges source entity JSON\(s\) into a target entity JSON and consolidates child entities within the merged result based on hash-based grouping and pairwise consolidation logic.

The consolidate\(\) method acts as the main entry point for consolidating JSONs. This method handles both single JSON and multiple JSONs, via the **items** array, as source input.

<table id="table_ych_wng_53c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

additionalParams

</td><td>

Object

</td><td>

Optional. Extra configuration parameters passed through to the consolidation methods. Stored on the instance as `this.additionalParams` and is accessible in all overridable methods. Can contain any custom key-value pairs needed by the implementing class.

</td></tr><tr><td>

sourceJSON

</td><td>

Object

</td><td>

Accepts the JSON output of the [LeadtoCashCore - Scoped](../../LeadtoCashCoreScoped/concept/LeadToCashCoreAPI.md#) createInstance\(\) or effect\(\) method. Can be a single entity JSON object, or a JSON object containing an items array of multiple entity JSONs.If sourceJSON doesn't contain an items array, the method treats it as a single entity and wraps it in an array automatically. Pass null or omit this parameter if only target consolidation is needed.

```
"sourceJSON": {
    "items": [Array]
}
```

</td></tr><tr><td>

sourceJSON.items

</td><td>

Array of Objects

</td><td>

Optional. Array of entity JSONs to merge into the target. Each item represents an entity with its attributes and child arrays. If this property exists, **items** is used directly as the list of source entities.```
"items": [
  {
  "attributes": {Object},
  "characteristics": [Array],
  "coveredProducts": [Array],
  "sys_id": "String",
  "table": "String"
  }
]
```

</td></tr><tr><td>

sourceJSON.items.attributes

</td><td>

Object

</td><td>

Key-value pairs representing the entity attributes. Each attribute is an object with a value property.```
"attributes": {
  "end_date": {"value": "String"},
  "product_offering": {"value": "String"},
  "quantity": {"value": "String"},
  "start_date": {"value": "String"}
}
```

Example: `{ "product_offering": { "value": "xr48..." }, "quantity": { "value": "5" } }`

</td></tr><tr><td>

sourceJSON.items.attributes.end\_date

</td><td>

String

</td><td>

End date of the attribute.Format: GlideDate value \(for example, 2026-01-01\)

</td></tr><tr><td>

sourceJSON.items.attributes.product\_offering

</td><td>

String

</td><td>

Name of the product offering associated with the attribute. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

sourceJSON.items.attributes.quantity

</td><td>

String

</td><td>

Number of product items purchased relative to the attribute.

</td></tr><tr><td>

sourceJSON.items.attributes.start\_date

</td><td>

String

</td><td>

Start date of the attribute.Format: GlideDate value \(for example, 2026-01-01\)

</td></tr><tr><td>

sourceJSON.items.characteristics

</td><td>

Array of Objects

</td><td>

Optional. Array of characteristic entity JSONs.```
"characteristics": [
  {
    "attributes": {Object},
    "sys_id": "String",
    "table": "String"
   }
]
```

</td></tr><tr><td>

sourceJSON.items.characteristics.attributes

</td><td>

Object

</td><td>

Attributes associated with the item characteristic. Each child property is a key-value pair representing the attribute. The attribute is an object with a value property.```
"attributes": {
   "characteristic": {Object},
   "value": {Object}
}
```

</td></tr><tr><td>

sourceJSON.items.characteristics.attributes.characteristic

</td><td>

Object

</td><td>

Key-value pair representing the characteristic associated with the attribute. **characteristic** is an object with a value property.```
"characteristic": {
    "value": "String"
}
```

</td></tr><tr><td>

sourceJSON.items.characteristics.attributes.value

</td><td>

Object

</td><td>

Key-value pair representing the attribute value associated with the parent characteristic. **value** is an object with a value property.```
"value": {
   "value": "String"
}
```

</td></tr><tr><td>

sourceJSON.items.characteristics.sys\_id

</td><td>

String

</td><td>

Sys\_id of the characteristic associated with the item.

</td></tr><tr><td>

sourceJSON.items.characteristics.table

</td><td>

String

</td><td>

Table location of the characteristic associated with the item.

</td></tr><tr><td>

sourceJSON.items.coveredProducts

</td><td>

Array of Objects

</td><td>

Optional. Array of covered product entity JSONs.```
coveredProducts: [
 {
  "sys_id": {Object},
  "table": "String",
  "attributes": {Object}
 }
]
```

</td></tr><tr><td>

sourceJSON.items.coveredProducts.sys\_id

</td><td>

Object

</td><td>

Sys\_id of the covered product record.```
sys_id: { 
  value: "String"
}
```

</td></tr><tr><td>

sourceJSON.items.coveredProducts.table

</td><td>

String

</td><td>

Table name containing the covered product record. For example, `sn_install_base_m2m_contract_sold_product`.

</td></tr><tr><td>

sourceJSON.items.coveredProducts.attributes

</td><td>

Object

</td><td>

Attributes of the covered product. Fields may vary based on the record.```
attributes: {
            sold_product: { value: "String" },
            contract: { value: "String" },
            service_contract_line: { value: "String" },
            entitlement: { value: "String" },
            install_base: { value: "String" },
            covering_sold_product: { value: "String" },
            date_added: { value: "String" },
            date_removed: { value: "String" }
  }
```

</td></tr><tr><td>

sourceJSON.items.coveredProducts.attributes.sold\_product

</td><td>

Object

</td><td>

Sold product record associated with this covered product.```
"sold_product": {
  "value": "String"
}
```

</td></tr><tr><td>

sourceJSON.items.coveredProducts.attributes.contract

</td><td>

Object

</td><td>

Parent contract record under which coverage is defined.```
"contract": {
  "value": "String"
}
```

</td></tr><tr><td>

sourceJSON.items.coveredProducts.attributes.service\_contract\_line

</td><td>

Object

</td><td>

Specific service contract line item linked to this covered product.```
"service_contract_line": {
  "value": "String"
}
```

</td></tr><tr><td>

sourceJSON.items.coveredProducts.attributes.entitlement

</td><td>

Object

</td><td>

Entitlement record governing the coverage terms.```
"entitlement": {
  "value": "String"
}
```

</td></tr><tr><td>

sourceJSON.items.coveredProducts.attributes.install\_base

</td><td>

Object

</td><td>

Install base record representing the deployed asset.```
"install_base": {
  "value": "String"
}
```

</td></tr><tr><td>

sourceJSON.items.coveredProducts.attributes.covering\_sold\_product

</td><td>

Object

</td><td>

Sold product providing coverage for this entry.```
"covering_sold_product": {
  "value": "String"
}
```

</td></tr><tr><td>

sourceJSON.items.coveredProducts.attributes.date\_added

</td><td>

Object

</td><td>

ISO 8601 date string indicating when the product was added to coverage.```
"date_added": {
  "value": "String"
}
```

</td></tr><tr><td>

sourceJSON.items.coveredProducts.attributes.date\_removed

</td><td>

Object

</td><td>

ISO 8601 date string indicating when the product was removed from coverage. Null or empty if currently active.```
"date_removed": {
  "value": "String"
}
```

</td></tr><tr><td>

sourceJSON.items.lineItems

</td><td>

Array of Objects

</td><td>

Optional. Array of child line item entity JSONs. Each child follows the same structure \(sys\_id, table, attributes, and nested children\).```
"lineItems": [
 {
   "attributes": {Object},
   "characteristics": [Array],
   "coveredProducts": [Array],
   "sys_id": "String",
   "table": "String"
  }
]
```

</td></tr><tr><td>

sourceJSON.items.lineItems.attributes

</td><td>

Object

</td><td>

Key-value pairs representing the entity attributes. Each attribute is an object with a value property. Follows the same structure as **sourceJSON.items.attributes**.```
"attributes": {
  "characteristic": {Object},
  "value": {Object}
}
```

</td></tr><tr><td>

sourceJSON.items.lineItems.characteristic

</td><td>

Object

</td><td>

Key-value pairs representing the characteristic of the line item. The characteristic is an object with a value property. Follows the same structure as **sourceJSON.items.characteristics**.```
"characteristics": [{
   "attributes": {Object},
   "sys_id": "String",
   "table": "String"
}]
```

</td></tr><tr><td>

sourceJSON.items.lineItems.coveredProducts

</td><td>

 

</td><td>

Array of covered product entity JSONs associated with the line item. Follows the same structure as **sourceJSON.items.coveredProducts**.```
coveredProducts: [
 {
  "sys_id": {Object},
  "table": "String",
  "attributes": {Object}
 }
]
```

</td></tr><tr><td>

sourceJSON.items.lineItems.sys\_id

</td><td>

 

</td><td>

Sys\_id of the entity JSONs line item.

</td></tr><tr><td>

sourceJSON.items.lineItems.table

</td><td>

 

</td><td>

Table location of the entity JSONs line item.

</td></tr><tr><td>

sourceJSON.items.sys\_id

</td><td>

String

</td><td>

Sys\_id of the source entity record.

</td></tr><tr><td>

sourceJSON.items.table

</td><td>

String

</td><td>

Table name of the source entity. Example: `sn_pss_core_service_contract_line`.

</td></tr><tr><td>

targetJSON

</td><td>

Object

</td><td>

Required. Target entity JSON to consolidate the source JSON into. Must not be null or empty. Follows the same object structure as the source entity \(**sourceJSON** parameter\).```
targetJSON={
  "attributes": {Object},
  "entitlement_characteristic": {Object},
  "sys_id": "String",
  "table": "String,
  "line_item": {Object}
  }
}
```

</td></tr><tr><td>

targetJSON.attributes

</td><td>

Object

</td><td>

Key-value pairs representing the target entity attributes. Each attribute is an object with a value property. Follows the same object structure as the source attributes \(**sourceJSON.items.attributes** parameter\).```
"attributes": {
  "end_date": {"value": "String"},
  "product_offering": {"value": "String"},
  "quantity": {"value": "String"},
  "start_date": {"value": "String"}
}
```

Example: `{ "product_offering": { "value": "xr48..." }, "quantity": { "value": "5" } }`

</td></tr><tr><td>

targetJSON.lineItems

</td><td>

Array of Objects

</td><td>

Optional. Array of child line item entity JSONs on the target. Follows the same object structure as **sourceJSON.items.lineItems**.```
"lineItems": {
    "sys_id": "String",
    "table": "String",
    "attributes": {Object},
    "characteristics": {Object}
  }
```

</td></tr><tr><td>

targetJSON.lineItems.attributes

</td><td>

Object

</td><td>

Key-value pairs representing the entity attributes. Each attribute is an object with a value property. Follows the same structure as **sourceJSON.items.attributes**.```
"attributes": {
  "characteristic": {Object},
  "value": {Object}
}
```

</td></tr><tr><td>

targetJSON.lineItems.characteristics

</td><td>

Object

</td><td>

Key-value pairs representing the characteristic of the line item. The characteristic is an object with a value property. Follows the same structure as **sourceJSON.items.characteristics**.```
"characteristic": {
  "value": "String"
}
```

</td></tr><tr><td>

targetJSON.lineItems.coveredProducts

</td><td>

 

</td><td>

Array of covered product entity JSONs associated with the line item. Follows the same structure as **sourceJSON.items.coveredProducts**.```
"coveredProducts": [Array]
```

</td></tr><tr><td>

targetJSON.lineItems.sys\_id

</td><td>

 

</td><td>

Sys\_id of the entity JSONs line item.

</td></tr><tr><td>

targetJSON.lineItems.table

</td><td>

 

</td><td>

Table location of the entity JSONs line item.

</td></tr><tr><td>

targetJSON.sys\_id

</td><td>

String

</td><td>

Sys\_id of the target entity record.

</td></tr><tr><td>

targetJSON.table

</td><td>

String

</td><td>

Table name of the target entity. Example: `sn_pss_core_service_contract`

</td></tr></tbody>
</table><table id="table_zch_wng_53c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Consolidated JSON result. The merged and consolidated entity JSON contains all attributes from the target and merged/consolidated child arrays.Returns targetJSON if consolidation is disabled or sourceJSON is invalid.

Returns null if targetJSON is null or empty.

</td></tr></tbody>
</table>The following example shows how to invoke the consolidate method via LeadToCashService. It consolidates a source entity JSON containing line items into a target entity JSON. Line items with the same product offering are consolidated.

This example instantiates `LeadToCashService` directly for simplicity, but in production use, your custom subclass should be registered via the extension point and invoked through PrimitiveUtil.

**Note:** MyConsolidationService is a custom script include that needs to be created by extending ConsolidationService. The logic for the overridable methods \(enableConsolidation\(\), getHashConfig\(\), canConsolidateEntity\(\), canMergeEntity\(\), canConsolidateJSONs\(\), overrideAttributeValues\(\)\) needs to be added within MyConsolidationService. MyLeadToCashService extends LeadToCashService and returns MyConsolidationService from getConsolidationService\(\).

```
var sourceToTargetConfigID = "sn_cont_ent_wf_contract_to_quote";

var util = new sn_l2c_core.LeadToCashService(sourceToTargetConfigID);

var sourceJSON = {
    "items": [{
        "sys_id": "a1b2c3d4e5f6",
        "table": "sn_pss_core_service_contract_line",
        "attributes": {
            "product_offering": {
                "value": "po_001"
            },
            "quantity": {
                "value": "5"
            },
            "start_date": {
                "value": "2026-01-01"
            },
            "end_date": {
                "value": "2026-12-31"
            }
        },
        "characteristics": [{
            "sys_id": "ch_001",
            "table": "sn_pss_core_entitlement_characteristic",
            "attributes": {
                "characteristic": {
                    "value": "speed"
                },
                "value": {
                    "value": "100mbps"
                }
            }
        }],
        "coveredProducts": []
    }]
};

var targetJSON = {
    "sys_id": "t1a2b3c4d5e6",
    "table": "sn_quote_mgmt_core_quote",
    "attributes": {
        "account": {
            "value": "acct_001"
        }
    },
    "lineItems": [{
        "sys_id": "li_001",
        "table": "sn_quote_mgmt_core_quote_line_item",
        "attributes": {
            "product_offering": {
                "value": "po_001"
            },
            "quantity": {
                "value": "3"
            },
            "start_date": {
                "value": "2026-03-01"
            },
            "end_date": {
                "value": "2026-11-30"
            }
        },
        "characteristics": [{
            "sys_id": "ch_002",
            "table": "sn_pss_core_entitlement_characteristic",
            "attributes": {
                "characteristic": {
                    "value": "speed"
                },
                "value": {
                    "value": "100mbps"
                }
            }
        }],
        "coveredProducts": []
    }]
};

var additionalParams = {};
var output = util.consolidate(sourceJSON, targetJSON, additionalParams);
gs.info("Consolidated output = " + JSON.stringify(output));
```

Output:

```
{
  "sys_id": "t1a2b3c4d5e6",
  "table": "sn_quote_mgmt_core_quote",
  "attributes": {
    "account": {
      "value": "acct_001"
    }
  },
  "lineItems": [
    {
      "sys_id": "li_001",
      "table": "sn_quote_mgmt_core_quote_line_item",
      "attributes": {
        "product_offering": {
          "value": "po_001"
        },
        "quantity": {
          "value": "8"
        },
        "start_date": {
          "value": "2026-01-01"
        },
        "end_date": {
          "value": "2026-12-31"
        }
      },
      "characteristics": [
        {
          "sys_id": "ch_002",
          "table": "sn_pss_core_entitlement_characteristic",
          "attributes": {
            "characteristic": {
              "value": "speed"
            },
            "value": {
              "value": "100mbps"
            }
          }
        }
      ],
      "coveredProducts": []
    }
  ]
}
```

The following example shows how to invoke the consolidate method with null sourceJSON. In this case, only the child entities within the targetJSON are consolidated. This is useful when the target already contains duplicate line items that need to be merged.

```
var sourceToTargetConfigID = "sn_cont_ent_wf_contract_to_quote";

var util = new sn_l2c_core.LeadToCashService(sourceToTargetConfigID);

var targetJSON = {
    "sys_id": "t1a2b3c4d5e6",
    "table": "sn_quote_mgmt_core_quote",
    "attributes": {
        "account": {
            "value": "acct_001"
        }
    },
    "lineItems": [{
            "sys_id": "li_001",
            "table": "sn_quote_mgmt_core_quote_line_item",
            "attributes": {
                "product_offering": {
                    "value": "po_001"
                },
                "quantity": {
                    "value": "5"
                }
            },
            "characteristics": [],
            "coveredProducts": []
        },
        {
            "sys_id": "li_002",
            "table": "sn_quote_mgmt_core_quote_line_item",
            "attributes": {
                "product_offering": {
                    "value": "po_001"
                },
                "quantity": {
                    "value": "3"
                }
            },
            "characteristics": [],
            "coveredProducts": []
        }
    ]
};

var output = util.consolidate(null, targetJSON, {});

gs.info("Consolidated output = " + JSON.stringify(output));
```

Output:

```
{
  "sys_id": "t1a2b3c4d5e6",
  "table": "sn_quote_mgmt_core_quote",
  "attributes": {
    "account": {
      "value": "acct_001"
    }
  },
  "lineItems": [
    {
      "sys_id": "li_001",
      "table": "sn_quote_mgmt_core_quote_line_item",
      "attributes": {
        "product_offering": {
          "value": "po_001"
        },
        "quantity": {
          "value": "8"
        }
      },
      "characteristics": [],
      "coveredProducts": []
    }
  ]
}
```

## ConsolidationService - enableConsolidation\(\)

Overridable method that controls whether consolidation is enabled for this service instance. The base implementation returns false if not overridden. Implementing classes must override this method to return true to enable consolidation.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_lsg_jzg_53c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the service has successfully enabled consolidation.Valid values:

-   true: Service is enabled for consolidation.
-   false: Service isn't enabled for consolidation.

Default: false

</td></tr></tbody>
</table>The following example shows how to override enableConsolidation\(\) in a custom ConsolidationService.

**Note:** MyConsolidationService is a custom script include that must be created by extending ConsolidationService.

```
var MyConsolidationService = Class.create();

MyConsolidationService.prototype = Object.extendsObject(sn_l2c_core.ConsolidationService, {
    enableConsolidation: function() {
        return true;
    },

    type: 'MyConsolidationService'
});


var service = new MyConsolidationService();

var isEnabled = service.enableConsolidation();

gs.info("Consolidation enabled = " + isEnabled);
```

Output:

```
Consolidation enabled = true
```

## ConsolidationService - getHashConfig\(\)

Overridable method that returns the hash configuration for grouping entities before consolidation. The configuration specifies which attributes and child context types generate an MD5 hash for each entity. Entities with the same hash are grouped for pairwise consolidation. The base implementation returns an empty object when not overridden.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rcw_zdh_53c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

A JSON object mapping table names to their hash configuration. Each table entry contains: 1.  attributes \(Array of Strings\): Attribute field names whose values are included in the hash.
2.  childContextTypes \(Array of Strings\): Optional. Child table names whose hash values are recursively included in the parent hash.

Expected return format: `{ "table_name": { "attributes": ["field1", "field2"], "childContextTypes": ["child_table_name"] } }`

When the hash configuration for a table is an empty object `{}`, all entities of that type are consolidated into a single entity.

When the hash configuration for a table isn't found \(undefined or null\), an error is logged and entities are returned unchanged. The base implementation returns an empty object when not overridden.

</td></tr></tbody>
</table>The following example shows how to override getHashConfig\(\) to define hash attributes for contract lines and entitlement characteristics.

```
var MyConsolidationService = Class.create();

MyConsolidationService.prototype = Object.extendsObject(sn_l2c_core.ConsolidationService, {


    enableConsolidation: function() {

        return true;

    },


    getHashConfig: function() {

        return {

            "sn_quote_mgmt_core_quote_line_item": {

                "attributes": ["product_offering"],

                "childContextTypes": ["sn_pss_core_entitlement_characteristic"]

            },

            "sn_pss_core_entitlement_characteristic": {

                "attributes": ["characteristic", "option", "value"]

            },

            "sn_pss_core_covered_product": {

                "attributes": ["sold_product"]

            }

        };

    },


    type: 'MyConsolidationService'

});


var service = new MyConsolidationService();

var config = service.getHashConfig();

gs.info("Hash config = " + JSON.stringify(config));
```

Output:

```
Hash config = {
    "sn_quote_mgmt_core_quote_line_item": {
        "attributes": ["product_offering"],
        "childContextTypes": ["sn_pss_core_entitlement_characteristic"]
    },
    "sn_pss_core_entitlement_characteristic": {
        "attributes": ["characteristic", "option", "value"]
    },
    "sn_pss_core_covered_product": {
        "attributes": ["sold_product"]
    }
}
```

## ConsolidationService - getPrimary\(Object json1, Object json2\)

Overridable method to determine the primary JSON when two JSONs are being consolidated. For non-overridden attributes, the primary JSON's attribute values are used on the consolidated result. The base implementation returns json1 if not overridden.

|Name|Type|Description|
|----|----|-----------|
|json1|Object|First entity JSON to consolidate. Contains sys\_id, table, attributes, and child arrays.|
|json2|Object|Second entity JSON to consolidate. Contains sys\_id, table, attributes, and child arrays.|

|Type|Description|
|----|-----------|
|Object|The selected primary JSON. This JSON's attributes become the default values on the consolidated result. Must be either json1 or json2. The base implementation returns json1 if not overridden.|

The following example shows how to override getPrimary\(\) to select the entity with the earlier start date as primary.

```
// Custom ConsolidationService with getPrimary override
var MyConsolidationService = Class.create();

MyConsolidationService.prototype = Object.extendsObject(sn_l2c_core.ConsolidationService, {

    enableConsolidation: function() {
        return true;
    },

    getPrimary: function(json1, json2) {
        var date1 = json1.attributes.start_date ? json1.attributes.start_date.value : "";
        var date2 = json2.attributes.start_date ? json2.attributes.start_date.value : "";
        return date1 <= date2 ? json1 : json2;
    },

    type: 'MyConsolidationService'
});

// json1 — earlier start date
var json1 = {
    sys_id: { value: "a1b2c3d4e5f6" },
    table: "sn_pss_core_service_contract_line",
    attributes: {
        product_offering: { value: "po_abc123" },
        quantity: { value: "5" },
        start_date: { value: "2024-01-01" }
    }
};

// json2 — later start date
var json2 = {
    sys_id: { value: "f6e5d4c3b2a1" },
    table: "sn_pss_core_service_contract_line",
    attributes: {
        product_offering: { value: "po_abc123" },
        quantity: { value: "3" },
        start_date: { value: "2024-06-01" }
    }
};

var result = new MyConsolidationService().getPrimary(json1, json2);
```

Output:

```
// result === json1 → true
// "2024-01-01" <= "2024-06-01" is true, so json1 (earlier start date) is returned

{
    sys_id: { value: "a1b2c3d4e5f6" },
    table: "sn_pss_core_service_contract_line",
    attributes: {
        product_offering: { value: "po_abc123" },
        quantity: { value: "5" },
        start_date: { value: "2024-01-01" }
    }
}
```

## ConsolidationService - overrideAttributeValues\(Object json1, Object json2, Object consolidatedJSON\)

Overridable method, called after two JSONs are consolidated, for updating attributes on the consolidated JSON. The base implementation is a no-op if not overridden.

Common use cases include quantity summation, date range calculation \(earliest start / latest end\), term recalculation, and consolidated\_from tracking.

|Name|Type|Description|
|----|----|-----------|
|json1|Object|First entity JSON that was consolidated. This is the primary JSON \(as determined by getPrimary\(\)\). Contains original attributes before consolidation.|
|json2|Object|Second entity JSON that was consolidated. This is the secondary JSON. Contains original attributes before consolidation.|
|consolidatedJSON|Object|The result JSON after merging. Modify this object's attributes directly to apply custom logic. Initially contains a deep copy of the primary JSON's attributes with merged child arrays.|

|Type|Description|
|----|-----------|
|void|This method doesn't return a value. Modify the **consolidatedJSON** object directly.|

The following example shows how to override overrideAttributeValues\(\) to sum quantities and calculate date ranges when consolidating line items.

```
var MyConsolidationService = Class.create();

MyConsolidationService.prototype = Object.extendsObject(sn_l2c_core.ConsolidationService, {

    enableConsolidation: function() {

        return true;

    },

    overrideAttributeValues: function(json1, json2, consolidatedJSON) {

        // Sum quantities from both entities; fall back to 0 if quantity has no value
        var qty1 = parseInt(json1.attributes.quantity ? json1.attributes.quantity.value : "0");
        var qty2 = parseInt(json2.attributes.quantity ? json2.attributes.quantity.value : "0");
        consolidatedJSON.attributes.quantity = {
            "value": String(qty1 + qty2)
        };

        // Use the earliest start date; fall back to empty string if start_date has no value
        var start1 = json1.attributes.start_date ? json1.attributes.start_date.value : "";
        var start2 = json2.attributes.start_date ? json2.attributes.start_date.value : "";
        consolidatedJSON.attributes.start_date = {
            "value": start1 <= start2 ? start1 : start2
        };

        // Use the latest end date; fall back to empty string if end_date has no value
        var end1 = json1.attributes.end_date ? json1.attributes.end_date.value : "";
        var end2 = json2.attributes.end_date ? json2.attributes.end_date.value : "";
        consolidatedJSON.attributes.end_date = {
            "value": end1 >= end2 ? end1 : end2
        };

        // Record the sys_ids of the source entities that were merged into this consolidated result
        var consolidatedFrom = [];
        if (json1.sys_id) consolidatedFrom.push(json1.sys_id);
        if (json2.sys_id) consolidatedFrom.push(json2.sys_id);
        consolidatedJSON.attributes.consolidated_from = {
            "value": consolidatedFrom.join(",")
        };

    },

    type: 'MyConsolidationService'

});
```

## ConsolidationService - postHierarchyConsolidation\(Object consolidatedJSON\)

Overridable method that applies final modifications to the consolidated JSON after hierarchy consolidation is complete. The base implementation is a no-op if not overridden.

The system calls this method on the final consolidated result in the consolidate\(\) method, and also on each result entity within processHashGroup\(\).

|Name|Type|Description|
|----|----|-----------|
|consolidatedJSON|Object|Fully processed consolidated JSON object after all merging and consolidation is complete. Modify this object directly to apply final transformations.|

|Type|Description|
|----|-----------|
|void|This method doesn't return a value. Modify the **consolidatedJSON** object directly.|

The following example shows how to override postHierarchyConsolidation\(\) to set a flag on the consolidated entity.

```
var MyConsolidationService = Class.create();

MyConsolidationService.prototype = Object.extendsObject(sn_l2c_core.ConsolidationService, {


    enableConsolidation: function() {

        return true;

    },


    postHierarchyConsolidation: function(consolidatedJSON) {

        if (consolidatedJSON && consolidatedJSON.attributes) {

            consolidatedJSON.attributes.is_consolidated = {
                "value": "true"
            };

        }

    },


    type: 'MyConsolidationService'

});
```

## ConsolidationService - preProcess\(Object sourceJSON, Object targetJSON, Object additionalParams\)

Overridable method called before merge and consolidation for performing custom pre-processing tasks such as bulk map creation or caching lookup data.

Store computed results on the `this` object \(for example, `this.targetHeaderId = "sample_sys_id"`\). This method doesn't return any value.

|Name|Type|Description|
|----|----|-----------|
|sourceTarget|Object|Output of sourceJSON to consolidate. Accepts the JSON output of the [LeadtoCashCore - Scoped](../../LeadtoCashCoreScoped/concept/LeadToCashCoreAPI.md#) createInstance\(\) or effect\(\) method. Can be a single entity JSON object, or a JSON object containing an items array of multiple entity JSONs. Can be null or empty.|
|targetJSON|Object|Required. Target entity JSON for consolidation.|
|additionalParams|Object|Optional. Additional data passed from the caller.|

|Type|Description|
|----|-----------|
|void|This method doesn't return any value. Store computed results on the `this` object for use in subsequent consolidation steps.|

The following example shows how to override preProcess\(\) to cache a target header ID for use during consolidation.

```
var MyConsolidationService = Class.create();
MyConsolidationService.prototype = Object.extendsObject(sn_l2c_core.ConsolidationService, {

    enableConsolidation: function() {
        return true;
    },

    preProcess: function(sourceJSON, targetJSON, additionalParams) {
        // Cache the target entity's sys_id for use in subsequent consolidation steps
        this.targetHeaderId = targetJSON.sys_id;
        // If sourceJSON and sourceJSON.items are both present, store the item count; otherwise default to 0
        this.sourceCount = sourceJSON && sourceJSON.items ? sourceJSON.items.length : 0;
    },

    type: 'MyConsolidationService'
});
```

