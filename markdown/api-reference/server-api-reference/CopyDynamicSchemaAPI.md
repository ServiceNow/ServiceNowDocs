---
title: CopyDynamicSchemaAPI - Scoped, Global
description: The CopyDynamicSchemaAPI class provides methods and extension points for duplicating dynamic schema metadata.Creates and returns a CopyDynamicSchemaAPI object used to execute the copy operation. This method is provided in the DynamicSchemaCopyController class.Preset enabling users to skip the copying of attributes during the copy operation.Preset enabling users to skip the copying of all choice overrides during the copy operation.Preset enabling users to skip the copying of all choice sets and choices during the copy operation. All copied elements that would’ve linked to the copied choice set or choice will link to the original choice set or choice instead.Generates and returns a unique transaction ID for each copy operation you start. This ID is used to track the operation and is passed to extension points for validation and custom logic. This method is provided in the DynamicSchemaCopyController class.Starts the copy process for dynamic schema components and returns a transaction ID for identifying the copy operation. This method is provided in the DynamicSchemaCopyController class.Extension point method allowing custom names for a copy or an auto-generated name if empty or null. This extension point method is provided in the DynamicSchemaCopyController JavaScript class.Extension point method for creating custom copy operations by allowing users to specify whether a particular record should be copied. The method returns true if the record is to be copied and false if it should be skipped.Extension point method used to verify the transaction ID of the copy operation before returning the matching verification key from getCopyApi\(\), ensuring relevance to the extension point implementation. This extension point method is provided in the DynamicSchemaCopyController class.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CopyDynamicSchemaAPI- Scoped, Global

The CopyDynamicSchemaAPI class provides methods and extension points for duplicating dynamic schema metadata.

The CopyDynamicSchemaAPI API accepts a specified dynamic category as input and proceeds to copy all associated metadata through an asynchronous background process. Metadata includes child categories, category members, attributes, choice sets, choices, and choice overrides.

For example, metadata schema is used to describe product characteristics like color, screen size, or network speed. These characteristics change over time, and the schema helps track those changes across versions for things like tech support or warranties. The CopyDynamicSchemaAPI allows you to duplicate these volumes of metadata in a single request.

This API provides a transaction ID and verification key for security purposes and to ensure that your logic only applies to authorized operations. This API additionally allows for customized naming and partial duplication by indicating which records to skip in the copy process. Should any part of the copy process fail, the system automatically initiates a rollback to reverse all changes made during the operation.

## Requirements

This API requires the Dynamic Schema Support \(com.glide.dynamic\_schema\) plugin and the Admin or dynamic\_schema\_writer role to access it.

## Extension point methods

The copyDynamicSchema API supports a JavaScript class called DynamicSchemaCopyController, which implements three **optional** extension‑point methods that you define using custom logic. If you choose to implement the extension points, you must first create and define it before calling any API methods. Runtime invocation of extension point methods happens after your script calls runAsync\(\).

**Note:** Presets \(skipAttributes\(\), skipChoiceSets\(\), skipChoiceOverrrides\(\)\) take precedence over extension method behavior.

These extension point methods define whether the copy process applies to the current transaction, whether a particular record is copied or skipped, and what the new copy name is. This allows you to control whether to skip certain metadata, rename items, enforce business rules, or avoid copying sensitive information.

If no extension points are provided, the API copies everything \(unless the API is called with any of the skip methods, for example skipAttributes\(\)\) and generates names for the copied elements.

The extension point methods are as follows:

1.  [CopyDynamicSchemaAPI - verifyCopyOperation\(String transactionId\)](CopyDynamicSchemaAPI.md#) - Called before copying each major component type. Must return the same verification key supplied to getCopyApi\(\). If the method returns null, the extension point logic is ignored for this operation.
2.  [CopyDynamicSchemaAPI - shouldCopy\(Object recordData\)](CopyDynamicSchemaAPI.md#) - If false, skips the copy of that record.
3.  [CopyDynamicSchemaAPI - getCopyName\(Object recordData\)](CopyDynamicSchemaAPI.md#) - Creates a custom or auto-generated name for the copy.

## CopyDynamicSchemaAPI workflow

The following workflow shows the order in which to call CopyDynamicSchemaAPI methods in your scripts:

**Note:** If you choose to implement any extension point methods, you must first define them before calling the following API methods.

1.  [CopyDynamicSchemaAPI - getCopyApi\(String categoryToCopy, String verificationKey\)](CopyDynamicSchemaAPI.md#) - Creates an object used later in the copy operation and validates inputs.
2.  [CopyDynamicSchemaAPI - skipAttributes\(\)](CopyDynamicSchemaAPI.md#), [CopyDynamicSchemaAPI - skipChoiceSets\(\)](CopyDynamicSchemaAPI.md#), [CopyDynamicSchemaAPI - skipChoiceOverrides\(\)](CopyDynamicSchemaAPI.md#) - Presets to optionally skip attributes, choices, choice sets, and choice overrides during the copy operation. Must be called before runAsync\(\).
3.  [CopyDynamicSchemaAPI - getTransactionId\(\)](CopyDynamicSchemaAPI.md#) - Used to store the transaction ID so your extension point can recognize this specific copy operation.
4.  [CopyDynamicSchemaAPI - runAsync\(\)](CopyDynamicSchemaAPI.md#) - Starts the asynchronous copy process and triggers the extension points for each record being copied. Returns the transaction ID.
5.  After runAsync\(\), the system runs the extension point methods you may have previously defined: verifyCopyOperation\(\), shouldCopy\(\), getCopyName\(\).

If any step fails, the API rolls back the entire transaction. You can monitor the operation's status in the Progress Worker \[sys\_progress\_worker\] table, Name column with a name format like `Copy Dynamic Schema – <transaction ID>`.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CopyDynamicSchemaAPI - getCopyApi\(String categoryToCopy, String verificationKey\)

Creates and returns a CopyDynamicSchemaAPI object used to execute the copy operation. This method is provided in the DynamicSchemaCopyController class.

<table id="table_rlv_v5c_xgc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

categoryTocopy

</td><td>

String

</td><td>

The namespace name that uniquely identifies the given category to copy from.Example: `"tech_store/u_device_specs/u_mobile_devices"`

Table: Dynamic Categories \[dynamic\_categories\], \(Computed\) Namespaced Name column

**Note:** You may need to manually add this column to your table view using the gear icon.

</td></tr><tr><td>

verificationKey

</td><td>

String

</td><td>

Verification key to authorize the copy operation. See [CopyDynamicSchemaAPI - getTransactionId\(\)](CopyDynamicSchemaAPI.md#) for more information.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|A CopyDynamicSchemaAPI object used to get the transaction ID, perform the copy, or configure a preset strategy. Only returns null if unauthorized. Throws an exception if invalid or category isn't found.|

The following example script shows how to use getCopyApi\(\) to get a CopyDynamicSchemaAPI object that allows you to duplicate an existing category. To do this, the example calls getCopyApi\(\) with the target category's namespaced name \(`tech_store/u_device_specs`\) where `u_mobile_devices` is the name, and with a verification key \(`verification_key`\).

```
var api = DynamicSchemaAPI.get().getCopyApi("tech_store/u_device_specs/u_mobile_devices", "verification_key"); 

api.runAsync();
```

This script returns a CopyDynamicSchemaAPI object. Output:

```
{CopyDynamicSchemaAPI@13721}
```

With this object, you can monitor the operation, configure presets as needed, and initiate the copy process using additional copyDynamicSchema API methods.

## CopyDynamicSchemaAPI - skipAttributes\(\)

Preset enabling users to skip the copying of attributes during the copy operation.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Returns a CopyDynamicSchemaAPI object with attributes omitted. Used to get the transaction ID, perform the copy, or configure a preset strategy. Only returns null if unauthorized. Throws an exception if invalid or category isn't found.|

The following example demonstrates how to use skipAttributes\(\) to skip the copying of attributes. Category members are still copied, but link to the original attribute as attributes themselves aren't copied. Additionally, any choices or choice overrides associated solely with attributes aren't included.

```
var api = DynamicSchemaAPI.get().getCopyApi("tech_store/u_device_specs/u_mobile_devices", "verification_key"); 

api.skipAttributes().runAsync(); 
```

Output:

```
{CopyDynamicSchemaAPI@13721}
```

## CopyDynamicSchemaAPI - skipChoiceOverrides\(\)

Preset enabling users to skip the copying of all choice overrides during the copy operation.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Returns a CopyDynamicSchemaAPI object with choice overrides omitted. Used to get the transaction ID, perform the copy, or configure a preset strategy. Only returns null if unauthorized. Throws an exception if invalid or category isn't found.|

The following example demonstrates how to use skipChoiceOverrides\(\). When this preset is applied, no choice overrides will be copied.

```
var api = DynamicSchemaAPI.get().getCopyApi("tech_store/u_device_specs/u_mobile_devices", "verification_key"); 

api.skipChoiceOverrides().runAsync();
```

Output:

```
{CopyDynamicSchemaAPI@13721}
```

## CopyDynamicSchemaAPI - skipChoiceSets\(\)

Preset enabling users to skip the copying of all choice sets and choices during the copy operation. All copied elements that would’ve linked to the copied choice set or choice will link to the original choice set or choice instead.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Returns a CopyDynamicSchemaAPI object with choice sets and choices omitted. Used to get the transaction ID, perform the copy, or configure a preset strategy. Only returns null if unauthorized. Throws an exception if invalid or a category isn't found.|

The following example demonstrates how to use skipChoiceSets\(\). When this preset is applied to skip choice sets or choices in the copy operation. Choice overrides are still copied, but link to the original choice as choices themselves aren't copied.

```
var api = DynamicSchemaAPI.get().getCopyApi("tech_store/u_device_specs/u_mobile_devices", "verification_key"); 

api.skipChoiceSets().runAsync();
```

Output:

```
{CopyDynamicSchemaAPI@13721}
```

## CopyDynamicSchemaAPI - getTransactionId\(\)

Generates and returns a unique transaction ID for each copy operation you start. This ID is used to track the operation and is passed to extension points for validation and custom logic. This method is provided in the DynamicSchemaCopyController class.

The transaction ID is used by extension points like getCopyName\(\) to ensure that custom logic only applies to the correct copy transaction. You can store this ID in a custom table to reference it later or to coordinate with other scripts.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wqx_wvc_xgc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Transaction ID that can be used to identify the copy operation. You can check the status of the copy operation in the Progress Worker \[sys\_progress\_worker\] table, Name column.Naming format: Copy Dynamic Schema - &lt;transaction ID&gt;

</td></tr></tbody>
</table>The following example shows how to use getTransactionId\(\) to retrieve and store a transaction ID before copying a dynamic schema. The user calls getTransactionId\(\) to obtain the transaction ID and store it in a custom table. When the extension point implementation is invoked during the copy process, it can check against stored transaction IDs to determine whether it should provide custom naming logic or return null to ignore the transaction.

```
var api = DynamicSchemaAPI.get().getCopyApi("tech_store/u_device_specs/u_mobile_devices", "verification_key"); 
var id = api.getTransactionId(); 

var gr = new GlideRecord("u_copy_transactions"); 
gr.initialize(); 
gr.setValue("u_transaction_id", id); 
gr.insert(); 

api.runAsync(); 
```

Output returns the unique transaction ID:

```
“9a8e0f92ff5032103c16ffffffffff82”
```

## CopyDynamicSchemaAPI - runAsync\(\)

Starts the copy process for dynamic schema components and returns a transaction ID for identifying the copy operation. This method is provided in the DynamicSchemaCopyController class.

The runAsync\(\) method runs the copy operation asynchronously in the background, and calls the extension points, getCopyName\(\), shouldCopy\(\), and verifyCopyOperation\(\), during the copy process to customize naming and security. To view the status of the copy operation, see the Progress Worker \[sys\_progress\_worker\] table, Name column with a naming format of `Copy Dynamic Schema - <transaction ID>`.

If any part of the copy fails, the API automatically rolls back all changes to maintain data consistency.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ifr_2wc_xgc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Transaction ID used to identify the copy operation. The copy process is asynchronous, but you can check the status of the copy operation in the Progress Worker \[sys\_progress\_worker\] table, Name column with a naming format of `Copy Dynamic Schema - <transaction ID>`.The copying behavior depends on the extension point implementation and the skip method presets. Components are only skipped if the skip\(\) method presets are called or if the extension point shouldCopy\(\) returns false.

</td></tr></tbody>
</table>The following example script shows how to initiate a dynamic schema copy operation using the runAsync\(\) method where `tech_store/u_device_specs/u_mobile_devices` is the unique name of the category to copy and `verification_key` is a verification key. After obtaining the copy API instance and storing the transaction ID for extension point reference, runAsync\(\) begins the copy process for all schema components \(categories, category members, attributes, choice sets, choices, and choice overrides\).

```
var api = DynamicSchemaAPI.get().getCopyApi("tech_store/u_device_specs/u_mobile_devices", "verification_key"); 

api.runAsync();
```

Outputs the transaction ID:

```
“9a8e0f92ff5032103c16ffffffffff82”
```

## CopyDynamicSchemaAPI - getCopyName\(Object recordData\)

Extension point method allowing custom names for a copy or an auto-generated name if empty or null. This extension point method is provided in the DynamicSchemaCopyController JavaScript class.

<table id="table_fb1_1fz_13c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

recordData

</td><td>

Object

</td><td>

Object containing record metadata: -   `name`: record name
-   `namespaced_name`: namespace + record name
-   `table_name`: table name
-   `sys_id`: unique system ID

</td></tr></tbody>
</table><table id="table_gb1_1fz_13c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Proposed name for this copy.Possible errors:

-   Name is more than 60 characters.
-   Copy name already exists.

</td></tr><tr><td>

String \(empty or null\)

</td><td>

Autogenerated name for this copy.

</td></tr></tbody>
</table>This example shows an implementation of the extension point. After the shouldCopy\(\) method returns `true` to confirm the user's intent to copy the record, the user provides a custom name for the copy by defining getCopyName\(\). For example, the user can append "\_copy" to the original name as a chosen label, or allow the system to automatically generate a name.

```
var DynamicSchemaCopyController = Class.create(); 
DynamicSchemaCopyController.prototype = { 
 
    initialize: function() {}, 

    verifyCopyOperation: function(transactionId) { 
        var transactionIdExist = new GlideRecord('u_copy_transactions'); 
        transactionIdExist.addQuery('u_transaction_id', transactionId); 
        transactionIdExist.query(); 
 
        if (transactionIdExist.hasNext()) { 
            return 'verification_key'; 
        } 
        else { 
            return null; 
        } 
    }, 
 
    shouldCopy: function(recordData) { 
        var namespacedNameSkip = [ 
            'tech_store/u_device_specs/u_phone', 
            'tech_store/u_device_specs/u_storage' 
        ]; 
        var recordNamespacedName = String(recordData.get('namespaced_name')); 
        if (namespacedNameSkip.includes(recordNamespacedName)) { 
            return false; 
        } 
        return true; 
    }, 
 
    getCopyName: function(recordData) { 
        return String(recordData.get('name') + '_copy'); 
    }, 
 
    type: 'DynamicSchemaCopyController' 

};
```

Output:

```
Record's name + "_copy"
```

## CopyDynamicSchemaAPI - shouldCopy\(Object recordData\)

Extension point method for creating custom copy operations by allowing users to specify whether a particular record should be copied. The method returns true if the record is to be copied and false if it should be skipped.

This extension point method is provided in the DynamicSchemaCopyController class, and provides flexibility for users to control which records are included in the copy process based on their requirements.

<table id="table_z44_mdz_13c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

recordData

</td><td>

Java HashMap

</td><td>

Java HashMap containing record metadata: -   name: record name
-   namespaced\_name: namespace + record name
-   table\_name: table name
-   sys\_id: unique system ID

</td></tr></tbody>
</table><table id="table_ap4_mdz_13c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Returns true if a copy should be made and false otherwise.Flag that indicates whether a copy should be made.

Valid values:

-   true: Make a copy.
-   false: Don't make a copy.

</td></tr></tbody>
</table>This example shows an implementation of the shouldCopy\(\) extension point. Once verification is complete, the method enables users to implement custom copying logic, allowing them to skip records according to criteria such as name, namespaced\_name, table, or sys\_id.

```
var DynamicSchemaCopyController = Class.create(); DynamicSchemaCopyController.prototype = { 
 
    initialize: function() {}, 

    verifyCopyOperation: function(transactionId) { 
        var transactionIdExist = new GlideRecord(‘u_copy_transactions’); 
        transactionIdExist.addQuery(‘u_transaction_id’, transactionId); 
        transactionIdExist.query(); 
 
        if (transactionIdExist.hasNext()) { 
            return ‘verification_key’; 
        } 
        else { 
            return null; 
        } 
    }, 
 
    shouldCopy: function(recordData) { 
        var namespacedNameSkip = [ 
            ‘tech_store/u_device_specs/u_phone’, 
            ‘tech_store/u_device_specs/u_storage’ 
        ]; 
        var recordNamespacedName = String(recordData.get(‘namespaced_name’)); 
        if (namespacedNameSkip.includes(recordNamespacedName)) { 
            return false; 
        } 
        return true; 
    }, 
 
    getCopyName: function(recordData) { 
        return String(recordData.get(‘name’) + ‘_copy’); 
    }, 
 
    type: 'DynamicSchemaCopyController' 

};
```

Returns `true` if the namespaced\_name isn’t equal to `tech_store/u_device_specs/u_phone` or `tech_store/u_device_specs/u_storage`.

## CopyDynamicSchemaAPI - verifyCopyOperation\(String transactionId\)

Extension point method used to verify the transaction ID of the copy operation before returning the matching verification key from getCopyApi\(\), ensuring relevance to the extension point implementation. This extension point method is provided in the DynamicSchemaCopyController class.

|Name|Type|Description|
|----|----|-----------|
|transactionId|String|A unique string that identifies each copy operation.|

|Type|Description|
|----|-----------|
|String|Verification key from getCopyApi\(\), or null if the transaction ID isn't relevant to this extension point.|

This example shows an implementation of the verifyCopyOperation\(\) extension point. The user is required to verify the transaction ID associated with the copy operation before returning the verification key. The verification key must correspond to the value provided as an argument to the getCopyApi\(\) method.

```
var DynamicSchemaCopyController = Class.create(); DynamicSchemaCopyController.prototype = { 
 
    initialize: function() {}, 

    verifyCopyOperation: function(transactionId) { 
        var transactionIdExist = new GlideRecord(‘u_copy_transactions’); 
        transactionIdExist.addQuery(‘u_transaction_id’, transactionId); 
        transactionIdExist.query(); 
 
        if (transactionIdExist.hasNext()) { 
            return ‘verification_key’; 
        } 
        else { 
            return null; 
        } 
    }, 
 
    shouldCopy: function(recordData) { 
        var namespacedNameSkip = [ 
            ‘tech_store/u_device_specs/u_phone’, 
            ‘tech_store/u_device_specs/u_storage’ 
        ]; 
        var recordNamespacedName = String(recordData.get(‘namespaced_name’)); 
        if (namespacedNameSkip.includes(recordNamespacedName)) { 
            return false; 
        } 
        return true; 
    }, 
 
    getCopyName: function(recordData) { 
        return String(recordData.get(‘name’) + ‘_copy’); 
    }, 
 
    type: 'DynamicSchemaCopyController' 

}; 
```

Output:

```
“verification_key”
```

