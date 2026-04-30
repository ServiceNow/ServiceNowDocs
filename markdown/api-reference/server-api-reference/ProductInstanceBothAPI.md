---
title: ProductInstance - Scoped, Global
description: The ProductInstance API provides methods to generate a product instance identifier \(PID\), retrieve PID configuration data, and determine if a model category is a product instance.Generates the hashed value of the product instance and returns it.Gets the PID configuration associated with the model category based on the hierarchy and class name.Checks if a given model category is a product instance.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ProductInstance - Scoped, Global

The ProductInstance API provides methods to generate a product instance identifier \(PID\), retrieve PID configuration data, and determine if a model category is a product instance.

This API runs in the `sn_cmdb` namespace and requires the category\_manager or snc\_internal role. Access is also granted to users with access control lists \(ACLs\) for the Model Category \[cmdb\_model\_category\] table. You can view the ACLs in the Table \[sys\_db\_object\] table.

A PID is a unique identifier for a product instance and links asset, configuration item \(CI\), and an install base item \(IBI\) to synchronize updates between common product representations. A product instance is associated with assets of a particular model category.

Access to install base items requires the Customer Service Install Base Management \(com.snc.install\_base\) plugin.

See also:

-   [Model categories](https://www.servicenow.com/docs/access?context=c_ModelCategories&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)
-   [Product Instance feature in Hardware Asset Management](https://www.servicenow.com/docs/access?context=product-instance-for-assets&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)
-   [Create an install base item](https://www.servicenow.com/docs/access?context=create-install-base-item&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ProductInstance – generatePID\(String className, String modelCategorySysId, Object jsonKeyValues\)

Generates the hashed value of the product instance and returns it.

This method can be invoked many times without affecting the performance of the calling application. This method doesn’t modify any data in the database and caches the data required to compute the PID.

A product Instance Identifier \(PID\) is a unique identifier for a Product Instance and links assets, CIs, and install base items \(IBI\).

A PID is generated based on the following items defined in the Product Instance Identifier Configurations \[product\_instance\_identifier\_configuration\] table:

-   PID configurations \(read only\)
-   Order assigned to each configuration

See also [Product Instance feature in Hardware Asset Management](https://www.servicenow.com/docs/access?context=product-instance-for-assets&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US).

<table id="table_mxt_n4d_tzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

className

</td><td>

String

</td><td>

Table name for the PID to be generated.

</td></tr><tr><td>

modelCategorySysId

</td><td>

String

</td><td>

The sys\_id of the model category in the Model Categories \[cmdb\_model\_category\] table. For information, see [Model categories](https://www.servicenow.com/docs/access?context=c_ModelCategories&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US).

</td></tr><tr><td>

jsonKeyValues

</td><td>

Object

</td><td>

JSON key-value pair of PID parameters configured in the Product Instance Identifier Configurations \[product\_instance\_identifier\_configuration\] table.The key value pairs contain attribute names with their corresponding values. These values vary depending on the configuration properties defined for the PID.

</td></tr></tbody>
</table><table id="table_nxt_n4d_tzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information used to generate the PID.The object returns with an empty product\_instance\_id property value in the following conditions:

-   The PID is missing the required PID configuration attributes. The PID configuration is in the Product Instance Identifier Configurations \[product\_instance\_identifier\_configuration\] table.
-   The given class doesn’t have an associated product instance.

```
{
  "model_category_sysId": "String",
  "parameters": [Array],
  "product_instance_id": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.model\_category\_sysId

</td><td>

The sys\_id of the product category in the Model Categories \[cmdb\_model\_category\] table.This value might be different from the input value if the model category hierarchy was used to generate the PID.

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.parameters

</td><td>

List of parameters used to generate the PID and defined in the Product Instance Identifier Configurations \[product\_instance\_identifier\_configuration\] table.Data type: Array of Strings

</td></tr><tr><td>

&lt;Object&gt;.product\_instance\_id

</td><td>

PID in the product\_instance\_id field of an asset, CI, or install base item.The hashed value of the PID can be set on this property to synchronize common values in objects one of the following tables:

-   Assets \[alm\_asset\]
-   Configuration Items \[cmdb\_ci\]
-   Install Base Items \[sn\_install\_base\_item\]

Install base items require the Customer Service Install Base Management \(com.snc.install\_base\) plugin.

Data type: String

</td></tr></tbody>
</table>The following example shows how to create a PID for an asset in the Medical assets \[sn\_ent\_medical\_asset\] table. This table is included with the Customer Service Install Base Management \(com.snc.install\_base\) plugin.

```
var output = sn_cmdb.ProductInstance.generatePID('sn_ent_medical_asset', '4b8aa89a77710110dd5fca22fe5a9984', { "serial_number" : "SN1001"});
gs.info(JSON.stringify(output,null,'\t'));
```

Output:

```
{
  "model_category_sysId": "4b8aa89a77710110dd5fca22fe5a9984",
  "product_instance_id": "tw8QgznsS4cP3b4U0+rSbnbIWxirYpeVSquk3g81K/8=",
  "parameters": [
    "serial_number"
  ]
}
```

## ProductInstance – getPIDConfig\(String className, String modelCategorySysId\)

Gets the PID configuration associated with the model category based on the hierarchy and class name.

This method scans all the hierarchies for the model category and returns the PID configuration\(s\) for the first found model category.

|Name|Type|Description|
|----|----|-----------|
|className|String|Table name for the PID to be generated.|
|modelCategorySysId|String|The sys\_id of the model category in the Model Categories \[cmdb\_model\_category\] table. For information, see [Model categories](https://www.servicenow.com/docs/access?context=c_ModelCategories&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US).|

<table id="table_nxt_n4d_tzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

JSON object containing the PID configurations associated with the given class name and model category.```
{
  "model_category_sysId": "String",
  "configs": [Array]
}
```

</td></tr><tr><td>

&lt;Object&gt;.model\_category\_sysId

</td><td>

The sys\_id of the product category in the Model Categories \[cmdb\_model\_category\] table.This value might be different from the input value if the model category hierarchy was used to generate the PID.

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.configs

</td><td>

List of each configuration associated with the given model category.```

"configs": [
 {
  "configuration_order": Number,
  "parameters": [Array]
 }
]
```

Data type: Array

</td></tr><tr><td>

&lt;Object&gt;.configs.configuration\_order

</td><td>

Returns the order of the configuration defined in the Product Instance Identifier Parameters \[product\_instance\_identifier\_parameters\] table.Data type: Number

</td></tr><tr><td>

&lt;Object&gt;.configs.parameters

</td><td>

List of all the parameters associated with the configuration and its order.```
"parameters": [
  {
   "parameter_class_attribute_name": "String",
   "parameter_class_name": "String",
   "parameter_name": "String",
   "parameter_order": Number
  }
]
```

Data type: Array of Objects

</td></tr><tr><td>

&lt;Object&gt;.configs.parameters.parameter\_class\_attribute\_name

</td><td>

Parameter name associated with the parameter\_class\_name property. This string represents the name of the column corresponding to that class.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.configs.parameters.parameter\_class\_name

</td><td>

Class name associated with the parameter defined in the Product Instance Identifier Parameters \[product\_instance\_identifier\_parameters\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.configs.parameters.parameter\_name

</td><td>

Parameter name defined in the Product Instance Identifier Parameters \[product\_instance\_identifier\_parameters\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.configs.parameters.parameter\_order

</td><td>

Order of the parameter defined in the Product Instance Identifier Parameters \[product\_instance\_identifier\_parameters\] table.Data type: Number

</td></tr></tbody>
</table>The following example shows how to retrieve configuration details for a model category named in the in the Medical assets \[sn\_ent\_medical\_asset\] table. This table is included with the Customer Service Install Base Management \(com.snc.install\_base\) plugin.

```
var config = sn_cmdb.ProductInstance.getPIDConfig('sn_ent_medical_asset', '4b8aa89a77710110dd5fca22fe5a9984');
gs.info(JSON.stringify(config,null,'\t'));
```

Output:

```
{
  "model_category_sysId": "4b8aa89a77710110dd5fca22fe5a9984",
  "configs": [
    {
      "parameters": [
        {
          "parameter_class_attribute_name": "serial_number",
          "parameter_class_name": "sn_ent_medical_asset",
          "parameter_name": "serial_number",
          "parameter_order": 1
        }
      ],
      "configuration_order": 100
    },
    {
      "parameters": [
        {
          "parameter_class_attribute_name": "parent",
          "parameter_class_name": "sn_ent_medical_asset",
          "parameter_name": "parent_asset",
          "parameter_order": 1
        },
        {
          "parameter_class_attribute_name": "model_component_id",
          "parameter_class_name": "sn_ent_medical_asset",
          "parameter_name": "model_component_id",
          "parameter_order": 2
        }
      ],
      "configuration_order": 200
    }
  ]
}
```

## ProductInstance – isProductInstance\(String modelCategorySysId\)

Checks if a given model category is a product instance.

If both of the following conditions are met, the model category qualifies as a product instance:

-   The value of the model category's is\_model\_category flag is true.
-   The model category has a valid configuration defined for it in the Product Instance Identifier Configurations \[product\_instance\_identifier\_configuration\] table.

This method can be used in business rules before invoking the generatePID\(\) method.

|Name|Type|Description|
|----|----|-----------|
|modelCategorySysId|String|The sys\_id of the model category in the Model Categories \[cmdb\_model\_category\] table. For information, see [Model categories](https://www.servicenow.com/docs/access?context=c_ModelCategories&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US).|

<table id="table_nxt_n4d_tzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the model category provided is a product instance.Valid values:

-   true: The model category provided is a product instance.
-   false: The model category provided isn’t a product instance.

</td></tr></tbody>
</table>The following example shows how to determine whether the model category provided is a product instance.

```
var isProductInstance =  sn_cmdb.ProductInstance.isProductInstance('4b8aa89a77710110dd5fca22fe5a9984');
gs.info(isProductInstance);
```

Output:

```
true
```

