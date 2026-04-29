---
title: Rules
description: Learn how to create and manage rules to deliver dynamic configuration experiences. Define conditions and actions to show or hide fields, display messages, calculate values, and generate bills of material \(BOMs\). Explore rule types, including visibility, message, inclusion, exclusion, determination, and product actions, to efficiently build intelligent, responsive configurations.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [The CPQ Configurator, CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Rules

Learn how to create and manage rules to deliver dynamic configuration experiences. Define conditions and actions to show or hide fields, display messages, calculate values, and generate bills of material \(BOMs\). Explore rule types, including visibility, message, inclusion, exclusion, determination, and product actions, to efficiently build intelligent, responsive configurations.

As the end user navigates through the configuration experience and populates information, rules provide its dynamic elements: hiding and showing content, calculating values, delivering recommendations and messages, and building the bill of materials \(BOM\).

With a focus on administering rules in the administration user interface, this article discusses the two components of rules, conditions and actions, and the six action types available in CPQ. Much like other elements in the application, the UI is a good place to add or edit small numbers of rules. When many rules need manipulation, we recommend using the Matrix Loader. For more information, see [Matrix Loader: CSV rules upload](matrix_loader_csv_rules_upload.md).

In the administration UI, rules are accessible in two ways:

-   Global rules: In the navigation pane, click **Rules**. The rule list administration page displays all rules defined in the environment. If your task is to add new rules, this is the only place in the Admin UI where you can initiate a new rule.
-   Rules associated with a single blueprint: Click **Blueprints**, and then click a blueprint. Click the Rules tab to view the rules. Click a rule to open it.

## Conditions

CPQ rule conditions consist of a logical expression. At runtime, the rules engine executes the rule if the expression evaluates true.

The administrator can define several kinds of conditions:

-   Any Condition Is Met: ORs the defined logical expressions.
-   All Conditions Are Met: ANDs the defined logical expressions.
-   Always \(Action Input Change\): Runs the rule whenever the end user alters a relevant input.
-   Custom Logic is Met: Allows the administrator to define custom logic, including ANDs and ORs, among expressions.
-   Advanced Function: Enables the administrator to write a script to define the rule condition.

## Actions

The actions section of a rule defines the tasks the rule accomplishes when it runs \(when its condition evaluates true\). CPQ, unlike other engines, allows multiple actions and action types under one condition. This is a handy organizational feature that consolidates all tasks that need to be performed in the same scenario in one rule. The consolidation of multiple tasks with one condition also increases the efficiency with which the rules engine evaluates and accomplishes tasks. Increased efficiency translates to performance that the end user can see.

On the rule administration page, review the Actions section located below the summary and conditions area.

-   List of actions: actions defined in this rule. Filter input allows you to find action\(s\) quickly, particularly when many actions are defined.
-   Action editor pane: Allows Admin to review and edit the action selected in the list of actions.
-   Add New Action button: define a new action for this rule. Six available action types are displayed in the action editor pane.

## Hiding actions

Hiding actions hide an entire field from view to the end user. Use hiding actions to focus the end user’s attention, presenting only those fields that are relevant to the solution being configured. A hidden field retains its value.

## Message actions

Message actions provide contextual information as the end user works through the configuration. The message is located relative to a designated field in the layout. Four message types are available.

|Message type|Example|Notes|
|------------|-------|-----|
|Info|![info message](../images/cpq-rules-message-type-example-info.png)|No effect on configuration experience beyond message|
|Warning|![warning message](../images/cpq-rules-message-type-example-warning.png)|No effect on configuration experience beyond message|
|Error|![error message](../images/cpq-rules-message-type-example-error.png)|Disables the Quote button so the user cannot move forward until the error state is alleviated.|
|Custom|Look is determined by user|The user can control whether this has no effect on configuration experience beyond message of if it disables the Quote button so the user cannot move forward until the error state is alleviated.|

## Inclusion/exclusion actions

Control picklist field options using inclusion and exclusion actions. The two action types allow the administrator to define the set of field options in the most convenient manner possible. Both inclusion and exclusion rules may operate on the same picklist field. For a picklist, the displayed options are determined as follows:

1.  Inclusion rules are applied to the set of options defined in the picklist field. If no inclusion rules are defined for the field, all of the picklist options continue past this step. The result of this step is the included set of picklist options.
2.  The included set is then evaluated against any exclusion rules that apply. The result is the ‘displayed setʼ of options.

Picklist options that are eliminated as a result of inclusion/exclusion actions can either be removed or disabled from the picklist menu of options visible to the end user.

During runtime, if a picklist option is selected \(either by an end user or via determination action\), but inclusion/exclusion rules later determine that it is an invalid option, users can specify what happens if currently selected options become excluded. The user may choose to leave the selections unchanged, deselect the selections, or to deselect the selections and then select the first valid option instead. The Quote button is disabled until the end user corrects this error state.

## Determination actions

A determination action programmatically sets the value of a field. The administrator can choose whether the determined value is soft-set or read-only \(forceset\).

If an end user changes the value of a field that had been soft-set by a determination rule, CPQ displays a message to the user reminding them of the recommended value. The message does not limit the user from quoting the configuration; it is informational only. If the user reverts the value of the field to the determination-recommended value, the message goes away. The Admin can choose not to display this message.

## Product actions

Product actions result in additions to the bill-of-material \(BOM\). When the BOM Type is set to Sales, a simple product action displays the product to the user as a line in the shopping cart. These sales BOM items are transferred to the Salesforce Quote Line Editor \(SFDC QLE\) when the configuration is quoted. If the BOM Type is set to Manufacturing, administrators usually do not show these lines to end users in the shopping cart. Manufacturing BOM items, however, are recorded and transferred to the SFDC Configuration Line Item object for communication with ERP and provisioning applications downstream.

<table id="table_usc_hd4_khc"><thead><tr><th>

Input

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Product

</td><td>

When BOM Type = Sales, the value in Product can be a 15-18 digit &lt;SFDC Product2 Id&gt; with format, 01t5f0000001tElAAI. CPQ pulls product code, description, and price from the SFDC Product2 record, or &lt;SFDC Product2 Product Code&gt;, or External ID depending on environment Product Id field settings.

 When BOM Type = Manufacturing, four options are available:

-   &lt;SFDC Product2 Id&gt;
-   &lt;SFDC Product2 Product Code&gt;
-   External ID
-   A valid string composed of letters, numbers, spaces, and the following special characters:`{}[]()|\~`_^@?<=>;:/.-,+*ʼ&%$#”!`

</td></tr><tr><td>

Quantity

</td><td>

&lt;positive integer&gt;

</td></tr><tr><td>

BOM Type

</td><td>

Sales: display in shopping cart. Quote pushes the item to the SFDC QLE and Configuration Line Items objects.

 Manufacturing: usually not shown to the end user. Quote pushes the item to the SFDC Configuration Line Items object.

 All: All BOM types display in shopping cart. Quote pushes the Sales and Manufacturing items to the Configuration Line Items object and Sales to the SFDC QLE object.

</td></tr><tr><td>

Mandatory

</td><td>

TRUE: end user is unable to delete the item from the shopping cart.

 FALSE: end user is allowed to delete the item from the shopping cart.

</td></tr></tbody>
</table>## Advanced product actions

If your use case requires multilevel bills of material \(BOMs\), setting a dynamic quantity, or product attribution beyond that available in simple product actions, an advanced product action is necessary. The advanced product action allows you to write a script that outputs records to the ProductList object.

The following matrix describes available ProductList attributions.

<table id="table_mgx_224_khc"><thead><tr><th>

ProductList.&lt;param&gt;

</th><th>

ReqOpt

</th><th>

Valid Values

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

bomType

</td><td>

R

</td><td>

Sales, Manufacturing, All

</td><td>

In Salesforce- integrated use cases, Manufacturing items are only written to LGK\_\_Configurat ionLineItem\_\_c; Sales items are written to the QLE and LGK\_\_Configurat ionLineItem\_\_c

</td></tr><tr><td>

description

</td><td>

O

</td><td>

&lt;text&gt;

</td><td>

 

</td></tr><tr><td>

extended

</td><td>

O

</td><td>

&lt;JSON object&gt; consisting of key : value pairs \(see note 1\)

</td><td>

If populated, this information transfers to LGK\_Extended\_I nformation\_\_c on the Configuration Line Item object in Salesforce, after the user clicks the Quote button

</td></tr><tr><td rowspan="8">

id

</td><td rowspan="8">

R

</td><td colspan="2">

When SF-integrated use case AND bomType = Sales…

</td></tr><tr><td>

Product2.Id, Product2.ProductCode, or External Id

</td><td>

See note 2

</td></tr><tr><td colspan="2">

When Headless/eCommerce AND bomType = Sales…

</td></tr><tr><td>

ProductId or ProductCode

</td><td>

See note 2

</td></tr><tr><td colspan="2">

When SF-integrated AND bomType = Manufacturing…

</td></tr><tr><td>

&lt;text&gt;, Product2.Id, Product2.ProductCode, or External Id

</td><td>

Administrators may add items not stored in Product2. If referencing records stored in Product2, note 2 applies

</td></tr><tr><td colspan="2">

When Headless/eCommerce AND bomType = Manufacturing…

</td></tr><tr><td>

&lt;text&gt;, ProductId or ProductCode

</td><td>

Admins may add items not stored in the Product object. If referencing records stored in Product, note 2 applies

</td></tr><tr><td>

level

</td><td>

O

</td><td>

&lt;integer&gt;

</td><td>

Optional; for Admin reference; does not drive app logic

</td></tr><tr><td>

notes

</td><td>

O

</td><td>

&lt;text&gt;

</td><td>

 

</td></tr><tr><td>

orderNumber

</td><td>

O

</td><td>

&lt;integer&gt;

</td><td>

Populate this parameter with numerical values that determine the sequence number of lines. Note: the ProductList object is filled by all product actions that trigger in the the blueprint. Limited to 28 digits.

</td></tr><tr><td>

parentProduct

</td><td>

O

</td><td>

&lt;text&gt;

</td><td>

If populated, must match uniqueIdentifier of parent line. In SF- integrated use cases, the top-most parentProduct is the Configurable Product. Set this value to the Product2.Id or Product2.ProductCode of the Configurable Product.

</td></tr><tr><td>

price

</td><td>

O

</td><td>

&lt;float&gt;

</td><td>

Negative and zero allowed. If unassigned, CPQ retrieves the base price from the product master.

</td></tr><tr><td>

qty

</td><td>

O

</td><td>

&lt;float&gt;

</td><td>

Negative and zero allowed. If unassigned, defaults to 1.

</td></tr><tr><td>

selectionType

</td><td>

O

</td><td>

Required, Optional

</td><td>

If left unpopulated, defaults to Required

</td></tr><tr><td>

uniqueIdentifier

</td><td>

R

</td><td>

&lt;unique text&gt;

</td><td>

String that uniquely identifies this line from others in this configuration session \(see Unique Identifier attribute section below\)

</td></tr><tr><td>

uom

</td><td>

O

</td><td>

&lt;text&gt;

</td><td>

Unit of measure

</td></tr></tbody>
</table>**Note:**

1.  The ProductList.extended parameter can take a shallow JSON object. Example: `{ “key1”: “val1”, “key2”: “val2” }` Also, the Admin can define the extended key : value pairs for a ProductList record using JavaScript. Examples:`ProductList.extended[“key”] = “val”; ProductList.extended.key = “val”;`
2.  To simplify the migration of product data between test and production environments, particularly in SF-integrated environments, administrators can request product actions to reference a ProductCode or External Id rather than ProductId. In the CPQ Admin, go to the Utilities menu in the navigation pane, and then click **Settings**. You can then set the Product Id field to Product Code, Partner Id, or External Id. If considering migrating from ProductId to ProductCode after go-live, you must coordinate the setting change with the values referenced in your Product actions and the implicit product actions in any picklist extension data you have defined.

## Unique Identifier attribute

CPQ passes the unique identifier of a product in CPQ to the Unique Line Id field on the quote line in Salesforce, allowing users to assign unique IDs to specific Salesforce quote lines.

When using the parentProduct and uniqueIdentifier attributes for product hierarchy, if two child products have the same parent product and Product ID but need to be displayed separately in the BOM, each requires a unique “uniqueIdentifier”. This ensures that the UI treats them as unique products when listing them.

See the following sample script to observe how item hierarchy, differentiating parent items via uniqueIdentifier, bomTypes, and iterating through ProductList records can work: [Adv Product Action: Sample Hierarchical BOM](https://docs.google.com/document/d/1DmVwr1NTJyFLWM0RJB4wUWcA7fI-Jg4iikv9Cji3OVI/edit?usp=sharing).

**Related topics**  


[Quote line unique IDs](quote_line_unique_ids.md)

