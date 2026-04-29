---
title: Using expressions in Cloud Provisioning and Governance
description: Expressions in policy actions can set or override values. Expressions in blueprints can access attributes of resources and can map values to request form fields. Expressions are available in resource blocks, blueprints, policies, and anywhere that Cloud Provisioning and Governance allows scripts.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Create a cloud policy, Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Using expressions in Cloud Provisioning and Governance

Expressions in policy actions can set or override values. Expressions in blueprints can access attributes of resources and can map values to request form fields. Expressions are available in resource blocks, blueprints, policies, and anywhere that Cloud Provisioning and Governance allows scripts.

## Using expressions

Expressions can hold the values for information that is dynamically generated in the system, such as the values for the selections users make on the Cloud User Portal. Expressions are available in resource blocks, blueprints, policies, and anywhere that Cloud Provisioning and Governance allows scripts.

-   **Using expressions in resource blocks**

    Each resource block operation uses an expression to hold a value for each parameter. The expression can use hard-coded values, data from the stack that the user provisions in the Cloud User Portal, data in the CMDB, and data that is derived from scripts. By default, Cloud Provisioning and Governance generates a set of parameters and their expressions for each resource block operation.

    For example, the parameter **Location**, which holds the datacenter that a resource belongs to, uses the expression `${parameter.Location}`

    ![Location parameter for a resource block](../image/parameters-for-resource-blocks.png "Expressions in a resource block")

-   **Using expressions in blueprints**

    Blueprints can use expressions to map input parameters for each operation on a resource block. By default, the blueprint displays the same parameters and values that are specified in the resource block.

    You can access blueprint attributes with expressions. The expression in the **Mapping** column defines blueprint attributes for each operation in a step. For example, the **Location** attribute, which appears on the stack request form, is accessible through the `{$parameter.Location}` expression. The Location parameter with the `${parameter.Location}` value appears on the **Inputs** tab when you select a blueprint operation.

    ![The Location parameter and expression](../image/rb-operation-parameter.png "Expressions in a blueprint")

-   **Using expressions in policy actions**

    Policy actions can use expressions to override parameter values that users submit in a request form on the Cloud User Portal. You can also access and override user data in stack operations. For example, use the following expression to rename a stack: `formData.Stackname = "your-naming-convention";`.

    ![Policy example script](../image/policy-script-example.png "Expressions in a policy script")


You can access blueprint attributes with expressions. The expression in the **Mapping** column defines blueprint attributes for each operation in a step. For example, the **Location** attribute, which appears on the request form for a virtual machine, is accessed in the following expression: `{$parameter.Location}`.

## Expression types

-   **Definitional expressions**

    Definitional expressions are a form of early binding \(or static binding\). These bindings refer to compile-time binding and are evaluated when the user submits the stack request form \(when stack or resource provisioning starts\). Definitional expressions do not have access to the data that is generated during Orchestration. Definitional expressions are enclosed in curly braces. For example: `${parameter.CloudAccount}`

-   **Runtime expressions**

    Runtime expressions are a form of late binding \(or dynamic binding\). These bindings refer to runtime binding and have access to the data that is created during Orchestration \(for example, stack items\). Runtime expressions are evaluated when called during an Orchestration run. Runtime expressions are typically used for dot-walking to data in tables. Runtime expressions are enclosed in parentheses. For example: `$(Stack.items[VM1].attributes[node_id])`

-   **Definitional/Runtime expressions**

    Some expressions include both definitional and runtime expressions.

-   **Complex expressions**

    You can nest expressions of any type within other expressions.


## Definition expression syntax and examples

Allowable syntax uses a dollar sign and curly braces. These types are available:

-   `${parameter.}`. Use this kind of expression to retrieve values from input attributes of processes like blueprint provisions. Data is not fetched from tables.
-   `${Stack.items[]}`. Use this syntax to access attributes of specific items in a stack.
-   `${randomNumber}`. Use this syntax to generate a random number. For example, you can provision a VM with a random node name or stack name.

|Example|Description|
|-------|-----------|
|$\{parameter.BillingCode\}|This expression shows how a billing code parameter appears in a blueprint.|
|$\{parameter.formData.CatalogAttributeType\}|This expression takes a catalog attribute that is submitted by a user while the user fills out the form for a catalog item in the Cloud User Portal.|
|$\{parameter.userData.userId\}|This expression takes the ID of a user while the user fills out the form for a catalog item in the Cloud User Portal.|
|$\{Stack.items\[Virtual Server\].attributes\[sys\_id\]\}|This expression gets the sys\_id of a virtual server that is apart of a stack. Virtual Server is the alias of a resource block used in the stack.|

## Runtime expression syntax and examples

Allowable syntax uses a dollar sign and parenthesis. These types are available:

-   `$(ci.tablename)` where `tablename` is a table in the system, usually a CI table in the CMDB. Use this syntax to access values of fields in the table.
-   `$(Stack.items[])`. Use this syntax to access attributes of specific items in a stack.

|Example|Description|
|-------|-----------|
|`$(ci.cmdb_ci_cloud_subnet[ sys_id=12231231231231231231].cidr)`|This expression dot walks to the Cloud Subnet table, finds the specific record with the given sys\_id, and takes the value from the `cidr` column.|
|`$(ci.sn_cmp _ip_pool[subnet=${parameter.formData.Subnet Id}])`|This expression combines runtime and definition type expressions. The equal sign = is used to evaluate a value for a match. The expression dot-walks to the IP Pool table and looks for the subnet that has the subnet ID that the user submitted.|
|`$(ci.cmdb_ci_cloud_subnet[${parameter.formData.SubnetId}].cidr)`|This expression combines runtime and definition type expressions. The expression takes the value of the **cidr** field from a subnet that the user chose during provisioning. The square brackets `[]` indicate that the expression dot-walks to the Cloud Subnet table and then looks at the subnet value that the user submitted on a blueprint provision. The expression grabs the **cidr** field value and then walks to the value in the **cidr** field of the sys\_id of the subnet.|
|$\(Stack.items\[Virtual Server\].attributes\[sys\_id\]\)|As in the definition expression example, this expression takes the sys\_id of a virtual server that is apart of a stack.|

## Example expression

`$(ci.cmdb_ci_nic[$(Script:CMPVMNICs.getNICs[arg=$(Stack.items[Virtual Server].attributes[sys_id])])].private_ip)`

-   **$\(ci**: Runtime expression to retrieve data from table.
-   **cmdb\_ci\_nic**: CI for NIC \(Network Interface Card\).
-   **$\(Script**: Script-based expression.
-   **CMPVMNICs**: Script include.
-   **getNICs**: Function inside a script include.
-   **arg**: Arguments to script include function. Arguments are separated by "," when there are multiple attributes.
-   **$\(Stack.items**: Runtime stack expression to retrieve stack item from a stack. Argument is the alias specified in blueprint.
-   **Virtual Server**: Alias of resource used in blueprint.
-   **$\(Stack.items\[Virtual Server\].attributes\[sys\_id\]\)**: Retrieve sys\_id of stack item \("Virtual Server"\) resource instance in a stack.
-   **private\_ip**: Attribute from cmdb\_ci\_nic. Replace with public IP if required.

## Expressions

<table id="table_o4w_1gt_kfb"><tbody><tr><td>

**Simple parameter mapping expression**

 This type of expression retrieves values from input attributes of processes, such as blueprint operations, resource blocks, and policies. Data is not fetched from tables. Maps values from one layer to another, such as from a Blueprint to a Resource to the Cloud API.

 -   Type: definitional
-   Syntax: `${parameter.}`
-   Examples:
    -   `${parameter.BillingCode}` returns the billing code.
    -   `${parameter.formData.CatalogAttributeType}` takes a catalog attribute that is submitted on the request form in the Cloud User Portal.
    -   `${parameter.userData.userId}` takes the ID of a user working on the request form in the Cloud User Portal.

</td></tr><tr><td>

**Stack item expression**

 A CI instance in the CMDB represents each stack item. Use Stack Item expressions to look up first-level properties on the CI that back the stack item or on the stack item itself.

 -   Type: definitional/runtime
-   Syntax: `${Stack.items[]}` or `$(Stack.items[])`
-   Examples:

`${Stack.items[VirtualServer1].attributes[sys_id]}` is a definitional type expression that gets the sys\_id of a virtual server in a stack. `VirtualServer1` is the alias of a resource block that is used in the stack.

`$(Stack.items[VirtualServer2].attributes[sys_id])` is a runtime type expression that takes the sys\_id of a virtual server that is a part of a stack.

`${Stack.items[vm1].attributes[node_id]}` reads the `node_id` attribute of the CI that was created for the VM. `vm1` is the stack item name \(or the alias of the resource in the blueprint\).

`$(Stack.items[vm1].status)` reads the status of the stack item.


</td></tr><tr><td>

**Property override expressions in policies**

 In policies, you can override properties by pulling a value from the system or by using a random number. You can use data from both the forms in the Cloud User Portal and from the user who performed the operation on the form.

 -   Type: definitional/runtime
-   Syntax: `${parameter.formData.xyz}` or `${this.parameter.userData.xyz}`
-   Examples:

The following value can set the stack name to **Stack\_Bob.Smith@company.com**: `Stack_${parameter.userData.userId}`

Set stack or table values using runtime expressions by taking the subnet from the IP Pools table:

`$(ci.sn_cmp _ip_pool[subnet=${parameter.formData.Subnet Id}])`

In scripts, you can assign values as follows:

`formData.App_Server_NodeName = "MyNodeName";`

`this.parameter.userData.userId == 'servicenowuserId';`

-   See also [Create a policy action script](../task/create-policy-script-1.md).

</td></tr><tr><td>

**Script expression**

 In the example, `VMProperties` is a script include with a function called `getIP`. A script expression is also an example of a complex expression \(the expression is nested\).

 -   Type: runtime
-   Syntax: `$(Script:scriptName.function[])`
-   Examples:

`$(Script:VMPropertiesUtil.getIP[ arg=$(Stack.items[VM1].attributes[object_id])])`

Expression for Private IP:`$(ci.cmdb_ci_nic[$(Script:CMPVMNICs.getNICs[arg=$(Stack.items[Virtual Server].attributes[sys_id])])].private_ip)`

Expression for Public IP: `$(ci.cmdb_ci_nic[$(Script:CMPVMNICs.getNICs[arg=$(Stack.items[Virtual Server].attributes[sys_id])])].public_ip)`

Expression to get the credential alias: `$(Script:CMPVMUtils.getCredentialAlias[arg=${Stack.items[Virtual Server].attributes[sys_id]}])`

Expression to get the IP address: `$(Script:CMPVMUtils.getReachableIp[arg=$(Stack.items[Virtual Server].attributes[sys_id])])`


</td></tr><tr><td>

**CI lookup expression**

 Accesses values of fields in a table, usually a CI table in the CMDB.

 -   Type: definitional/runtime
-   Syntax: `$(ci.tableName)`
-   Examples:

`$(ci.sn_cmp _ip_pool[subnet=${parameter.formData.Subnet Id}])` combines runtime and definition type expressions. The = operator evaluates a value for a match. The expression dot-walks to the IP Pool table and looks for the subnet that has the subnet ID that the user submitted.

`$(ci.cmdb_ci_cloud_subnet[${parameter.formData.SubnetId}].cidr)` takes the value of the `cidr` field from a subnet that the user specified during provisioning. The expression dot-walks to the Cloud Subnet table, looks at the subnet value that the user submitted on a blueprint provision, extracts the `cidr` field value, and then walks to the value in the `cidr` field of the sys\_id of the subnet.


</td></tr><tr><td>

**Random number expression**

 Generates a random number. For example, you can provision a VM with a random node name or stack name.

 -   Type: runtime
-   Syntax and example: `${randomNumber}`

</td></tr><tr><td>

**Scratchpad expression/Resource operation output attribute expression**

 Reads output attributes from one operation into another operation.

 -   Type: runtime
-   Syntax: varies
-   Example: To set/expose outputs from one operation:

`${Compute Interface.CreateNode.Output.resp.nodeId}`

To read the output attributes \(where `VM1.Provision` is the operation whose output attributes are read\):

`$(Outputs[VM1.Provision].NodeId)`


</td></tr><tr><td>

**Conditions in expressions**

 You can use conditional expressions in blueprint steps and resource operation steps to conditionally execute or skip the step. The conditional expressions are Javascript expressions and they support expression substitutions.

 -   Type: definitional/runtime
-   Syntax: varies
-   Examples:

‘$\{parameter.CloudAccount\}’==’Amazon Cloud Account’

‘$\(Stack.items\[vm1\].attributes\[node\_id\]\) ’== ’VM1’


</td></tr><tr><td>

**Complex expression**

 You can nest expressions. In the example, `${parameter.ServerID}` maps the sys\_id of the CI and is replaced before the outer expression is consumed.

 -   Type: any
-   Syntax: varies
-   Example: `$(ci.cmdb_ci_vm_instance[${parameter.ServerID}].name)`

</td></tr><tr><td>

**Order context**

 This expression is useful for life cycle operations and enables you to dot-walk on the order attributes as part of the **sn\_cmp\_order** table.

 -   Type: runtime
-   Syntax: `$(context.order.column_name)`
-   Examples:
    -   Request Item: `$(context.order.sc_req_item)`
    -   Dot-walk on request item object: `$(context.order.sc_req_item.number)`
    -   Mixed Expression \(Constant + Expression\): `"ram$(context.order.sc_req_item.number)"`

</td></tr></tbody>
</table>