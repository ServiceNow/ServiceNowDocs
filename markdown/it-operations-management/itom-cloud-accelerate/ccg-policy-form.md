---
title: Cloud Configuration Governance Policy form
description: The Cloud Configuration Governance Policy form displays detailed information about the policy such as cloud provider, resource type, policy type, and policy violation reporting settings.
locale: en-US
release: australia
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Cloud Configuration Governance reference, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Configuration Governance Policy form

The Cloud Configuration Governance Policy form displays detailed information about the policy such as cloud provider, resource type, policy type, and policy violation reporting settings.

|Field|Description|
|-----|-----------|
|Policy name|Name that uniquely identifies the policy.|
|Description|Brief description of the policy.|

## Resource type

Define the resource type for which you want to create the policy.

<table id="table_jy1_mll_hsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cloud provider

</td><td>

Cloud that hosts the resources to be scanned.

</td></tr><tr><td>

Resource type

</td><td>

Cloud resource type to be scanned through the policy. If the required resource type is not available, you can create a resource type. For more information, see [Create a resource collector](../task/create-ccg-resource-collector.md).

</td></tr></tbody>
</table>## Policy condition

Define the policy type and the non-compliant resource configuration.

<table id="table_etw_nll_hsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Cloud Configuration Governance supports the following types:-   **Condition builder**: The no-code method for creating policies.
-   **Integration Hub Flow**: The low-code method for creating policies.
-   **Script**: The code-based method for creating policies.

 Select the show available keys icon \(![Show available keys icon.](../image/show-available-keys-icon.png)\) to view the list of all available configuration keys for the selected resource type. You can use any of the keys in the policy.

</td></tr><tr><td>

Condition

</td><td>

Conditions for reporting the non-compliant cloud resource configuration. Always specify the key and value in a pair. Use the **OR** operator and the **AND** operator to perform logical operations in the policy condition.

 **Syntax**

 ```
Key is <key_name>
<data_type> Value <condition> <value>

```

 For example,

 ```
Key is AWS:IAM:User:PasswordEnabled
Boolean Value is true

```

 This field appears only when **Condition Builder** is selected from the **Type** field.

</td></tr><tr><td>

Configuration key

</td><td>

Configuration keys for the policy.

 This field appears only when **Integration Hub Flow** is selected from the **Type** field.

</td></tr><tr><td>

Integration flow

</td><td>

The appropriate Integration Hub flow.

 This field appears only when **Integration Hub Flow** is selected from the **Type** field.

</td></tr><tr><td>

Condition script

</td><td>

Script that implements the policy conditions to identify and report the policy violations. Cloud Configuration Governance contains several scriptable objects and variables for use in the policy scripts. For more information see, [Scripting reference](ccg-scripting-reference.md).

 You can create script includes to externalize the decision making and reuse the code across different scripts. For more information on creating the script includes, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=australia&pubname=australia-api-reference&ft:locale=en-US).

 **Note:** If you create a custom audit result record through the script, then the **Audit Violation Reporting** configuration defined in the policy doesn’t take effect.

This field appears only when **Script** is selected from the **Type** field.

</td></tr></tbody>
</table>## Audit violation reporting

Define how Cloud Configuration Governance reports the policy violation.

<table id="table_zwp_qll_hsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Report violation as

</td><td>

Violation definition to be included in the audit violation report. Cloud Configuration Governance uses the violation definition to report the policy non-compliances.If an appropriate violation definition is not available, you can create one as follows:

1.  Select the lookup using list icon \(![Lookup using list icon.](../image/lookup-using-list.png)\).
2.  Select **New**.
3.  Enter a name that uniquely identifies the violation definition.

Cloud Configuration Governance includes the name of the violation definition in the audit issue report.

4.  Select the default severity for the violation definition.
5.  \(Optional\) Enter a brief description of the violation.

</td></tr><tr><td>

Severity

</td><td>

Severity level of the violation. If you do not select the severity level in the policy, Cloud Configuration Governance uses the default severity defined in the violation definition.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Configuration Governance reference](ccg-reference.md)

