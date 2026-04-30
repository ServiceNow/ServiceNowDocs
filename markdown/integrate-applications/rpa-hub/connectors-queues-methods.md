---
title: Queue connector methods
description: The Queue connector methods enable you to create and manage work items for queues in the RPA Hub.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Queue, RPA Hub, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Queue connector methods

The Queue connector methods enable you to create and manage work items for queues in the RPA Hub.

## Prerequisites

1.  Assign the bot process to the automation project by using the **Assign bot process** option from the **Design** tab of RPA Desktop Design Studio to access the work items. For more information, see [Assign bot process to an automation project](../task/assign-bot-process.md).
2.  Set the QueueName property by doing the following steps:
    1.  In the RPA Desktop Design Studio, navigate to **Toolbox** &gt; **RPA Hub** &gt; **Queue**.
    2.  Drag the Queue connector under Global Objects in the Project Explorer.
    3.  Double-click the Queue connector.
    4.  Under the Properties pane, in the QueueName property, enter the name of the Queue.

        **Note:** The name of the Queue must be the same as that defined in RPA Hub.


## CreateJSONWorkItem

Creates a work item for the queue in the JSON format.

-   **Input**

    [Name](queue-connector-method-parameters.md#parameter-input-createjsonworkitem-name)

    [Priority](queue-connector-method-parameters.md#parameter-input-createjsonworkitem-priority)

-   **Output**

    [WorkItemId](queue-connector-method-parameters.md#parameter-output-createjsonworkitem-workitemid)

    [IsNameExists](queue-connector-method-parameters.md#parameter-output-createjsonworkitem-isnameexists)


To create the key-value pairs in a JSON object, do the following actions:

1.  On the CreateJSONWorkItem method bar, click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Enter the criteria as given in the table.

<table id="table_lnf_rwb_wbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

CONFIGURATION

</td></tr><tr><td colspan="2">

INPUT FIELDS

</td></tr><tr><td>

Type

</td><td>

The type of the work item. For example, for an accounting system queue, savings and current are types of accounts.

To configure the input field, see [Configure port properties](../task/configure-input-port-properties.md).

</td></tr><tr><td>

Stage

</td><td>

Updates the stage of the work item. Custom field to maintain different stages of the transaction.

</td></tr><tr><td>

SLA

</td><td>

Service Level Agreement \(SLA\) of the work item completion.

</td></tr><tr><td class="sub-head" colspan="2">

JSON PROPERTIES

</td></tr><tr><td colspan="2">

JSON PATH NOTATIONS

</td></tr><tr><td>

Name

</td><td>

Key-value pair \(JSON content\) for the request content. To add a key, do the following:

1.  Click the add key icon \(![Add key icon.](../image/add-image-icon.png)\).
2.  Enter the key name in the field.
3.  To add more keys, repeat the previous steps.
4.  To pass the value to these fields, see [Configure port properties](../task/configure-input-port-properties.md).


</td></tr><tr><td>

Sensitive

</td><td>

Sensitive content that is passed when the work item is created. Select this option as sensitive, then the data is encrypted and stored in the **Sensitive Request Content** field in the new work item in RPA Hub. For more information about the work item form, see [Work item form in RPA Hub](../../rpa-hub/reference/work-queue-form.md).

With this functionality, you can pass sensitive information through queues.

For example, if you want customer data to be encrypted in the queue, you must use the **Sensitive** field to store customer details such as credit card number, address, and so on.

</td></tr></tbody>
</table>3.  Click **OK**.

## CreateStringWorkItem

Creates a work item in a queue in the RPA Hub by accepting a string.

-   **Input**

    [RequestContent](queue-connector-method-parameters.md#paramater-input-CreateStringWorkItem-requestcontent)

    [Name](queue-connector-method-parameters.md#parameter-input-createjsonworkitem-name)

-   **Output**

    [WorkItemId](queue-connector-method-parameters.md#parameter-output-createjsonworkitem-workitemid)

    [IsNameExists](queue-connector-method-parameters.md#parameter-output-createjsonworkitem-isnameexists)


To specify additional criteria for creating string work items, do the following steps.

1.  On the CreateStringWorkItem method bar, click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Enter the criteria as given in the table.

<table id="table_ast_sdc_wbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

INPUT FIELDS

</td></tr><tr><td>

SensitiveRequestContent

</td><td>

Stores sensitive content in encrypted format in the new work item. To configure the input field, see [Configure port properties](../task/configure-input-port-properties.md).

With this functionality, you can pass sensitive information through queues.

For example, if you want customer data to be encrypted in the queue, you must use the **SensitiveRequestContent** field to store customer details such as credit card number, address, and so on.

</td></tr><tr><td>

Stage

</td><td>

Updates the stage of the work item. Custom field to maintain different stages of the transaction.

</td></tr><tr><td>

Type

</td><td>

The type of the work item. For example, for an accounting system queue, savings and current are types of accounts.

To configure the input field, see [Configure port properties](../task/configure-input-port-properties.md).

</td></tr><tr><td>

SLA

</td><td>

Service Level Agreement \(SLA\) of the work item completion.

</td></tr></tbody>
</table>3.  Click **OK**.

## GetWorkItems

Returns the count and the details of the work items created under the queue based on the criteria you specify. The method provides a default criterion already but you can specify additional criteria.

-   **Input**

    [Limit](queue-connector-method-parameters.md#parameter-input-getworkitem-limit)

-   **Output**

    [TotalCount](queue-connector-method-parameters.md#parameter-output-getworkitem-totalcount)


To specify additional criteria for identifying and getting work items, do the following steps.

1.  Click the method settings icon \(![Method settings icon](../image/component-settings-icon.png)\).
2.  Configure the filters, as required. No filter is mandatory.

<table id="table_pkh_1dn_psb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

INPUT FILTERS

</td></tr><tr><td>

Name

</td><td>

Name of the work item. You can specify one of the following filters:-   **Equals**: Name of the work item is exactly equal to the criteria you specify.
-   **Contains**: Name of the work item contains characters you specify.
-   **StartsWith**: The name of the work item starts with the characters you specify.
-   **EndsWith**: The name of the work item starts with the characters you specify.


</td></tr><tr><td>

Type

</td><td>

Type of the work item in string format. You can specify one of the following filters:-   **Equals**: Type of the work item is exactly equal to the criteria you specify.
-   **Contains**: Type of the work item contains characters you specify.
-   **StartsWith**: The type of the work item starts with the characters you specify.
-   **EndsWith**: The type of the work item starts with the characters you specify.


</td></tr><tr><td>

Status

</td><td>

Status of the work item.

</td></tr><tr><td>

Stage

</td><td>

Updates the stage of the work item. Custom field to maintain different stages of the transaction.

</td></tr><tr><td>

Priority

</td><td>

Priority of execution:-   **Critical**
-   **High**
-   **Medium**
-   **Low**
The assigned robot executes the bot process as per the defined priority in the work queue. The default priority is always **High**.

</td></tr><tr><td>

DateType

</td><td>

Date type of the work item. If you provide inputs to this field, you must also provide inputs to the **FromData** and **ToDate** fields also.

</td></tr><tr><td>

FromDate

</td><td>

If the method is picking work items within a date range, starting date in the range.

</td></tr><tr><td>

ToDate

</td><td>

If the method is picking work items within a date range, ending date in the range.

</td></tr><tr><td>

Offset

</td><td>

Number of work items that will be retrieved after the set limit. For example, if the limit is 20, the next picked work item starts from 21.

</td></tr><tr><td class="sub-head" colspan="2">

OUT FIELDS

</td></tr><tr><td>

OutRecords

</td><td>

Returns the details of the work items in an object form.

</td></tr></tbody>
</table>3.  Click **OK**.

    **Note:** A Data In port is created with each field you configure.


## PickWorkItem

Enables a robot to pick a work item based on the given criteria. You can also configure additional criteria for the work item to be picked.

queryConditions included in the PickWorkItem component are considered for calculating the number of robots required to complete an unattended bot process execution, if the bot process is enabled with robot pool. For more information about calculating the number of robots, see [Calculate the number of robots in RPA Hub](../../rpa-hub/task/calculate-robots.md). For more information about robot pool concepts, see [Robot pool in RPA Hub](../../rpa-hub/concept/robot-pool-rpa.md).

-   **Input**

    [Priority](queue-connector-method-parameters.md#parameter-input-createjsonworkitem-priority)

-   **Output**

    [WorkItemId](queue-connector-method-parameters.md#parameter-output-createjsonworkitem-workitemid)

    [RequestContent](queue-connector-method-parameters.md#paramater-input-CreateStringWorkItem-requestcontent)


To specify additional criteria for picking work items, do the following steps.

1.  Click the method settings icon \(![Method settings icon](../image/component-settings-icon.png)\).
2.  Enter the criteria as given in the table.

<table id="table_ewl_yqn_psb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

CONFIGURATION

</td></tr><tr><td colspan="2">

INPUT FILTERS

</td></tr><tr><td>

Name

</td><td>

Name of the work item based on the following filters.-   **Equals**: Name of the work item is exactly equal to the criteria you specify.
-   **Contains**: Name of the work item contains characters you specify.
-   **StartsWith**: The name of the work item starts with the characters you specify.
-   **EndsWith**: The name of the work item starts with the characters you specify.
 Selection exposes a Data In port.

</td></tr><tr><td>

Type

</td><td>

Type of the work item based on the following filters. -   **Equals**: Type of the work item is exactly equal to the criteria you specify.
-   **Contains**: Type of the work item contains characters you specify.
-   **StartsWith**: The type of the work item starts with the characters you specify.
-   **EndsWith**: The type of the work item starts with the characters you specify.
 Selection exposes a Data In port.

</td></tr><tr><td>

Stage

</td><td>

Stage of the work item work item based on the following filters. -   **Equals**: Stage of the work item is exactly equal to the criteria you specify.
-   **Contains**: Stage of the work item contains characters you specify.
-   **StartsWith**: Stage of the work item starts with the characters you specify.
-   **EndsWith**: Stage of the work item starts with the characters you specify.
 Selection exposes a Data In port.

</td></tr><tr><td>

Status

</td><td>

Status of the work item for the robot to select.

</td></tr><tr><td colspan="2">

OUT FIELDS

</td></tr><tr><td>

Name

</td><td>

Data out port that returns the name of the work item.

</td></tr><tr><td>

Type

</td><td>

Data out port that returns the type of the work item.

</td></tr><tr><td>

Remarks

</td><td>

Data out port that returns remarks on the work item.

</td></tr><tr><td>

Stage

</td><td>

Data out port that returns the stage of the work item.

</td></tr><tr><td>

RequestContent

</td><td>

String content for the work item. Picks the stored content when the work item is created.

</td></tr><tr><td>

SensitiveRequestContent

</td><td>

The sensitive content from this field is picked, decrypted and passed to the RPA Desktop Design Studio or robots.

</td></tr><tr><td class="sub-head" colspan="2">

JSON PROPERTIES

</td></tr><tr><td>

JSON PATH NOTATIONS

</td><td>

Data out port that returns the JSON path notation of a work item.Click the add key icon \(![Add key icon.](../image/add-image-icon.png)\) to add a key name.

JSON can be passed in both **RequestContent** and **SensitiveRequestContent** fields.

While picking work item, the JSON data is picked from a work item. For example, if a key-value pair "City: Mumbai" \(City is key and Mumbai is value\) is in the **RequestContent** field and "City: Delhi" \(City is key and Delhi is value\) is created in **SensitiveRequestContent** field. When you try to pick the same work item, since the key is same for both fields, the **SensitiveRequestContent** field is given precedence and that output is retrieved from this field.

</td></tr></tbody>
</table>3.  Click **OK**.

## ReleaseWorkItem

Releases a work item that has been accepted and executed by a bot. You must execute PickWorkItem method before executing this method.

-   **Input**

    [WorkItemId](queue-connector-method-parameters.md#parameter-output-createjsonworkitem-workitemid)

-   **Output**

    [Return](queue-connector-method-parameters.md#parameter-output-releaseworkitem-return)


## UpdateWorkItem

Enables a robot to update a work item after picking it with the PickWorkItem method based on specified criteria. You can configure additional criteria for the work item to be updated. You must execute PickWorkItem method before executing this method.

-   **Inputs**

    [WorkItemId](queue-connector-method-parameters.md#parameter-output-createjsonworkitem-workitemid)

    [RequestContent](queue-connector-method-parameters.md#paramater-input-CreateStringWorkItem-requestcontent)

    [ReleaseMode](queue-connector-method-parameters.md#parameter-input-updateworkitem-releasemode)

    [Priority](queue-connector-method-parameters.md#parameter-input-createjsonworkitem-priority)

    [Status](queue-connector-method-parameters.md#parameter-input-pickworkitem-status)

    [Exception Type](queue-connector-method-parameters.md#parameter-input-exception-type)


To specify additional criteria for updating work items, do the following steps.

1.  Click the method settings icon \(![Method settings icon](../image/component-settings-icon.png)\).
2.  Enter the criteria as given in the table.

<table id="table_kvt_vtn_psb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

CONFIGURATION

</td></tr><tr><td colspan="2">

INPUT FIELDS

</td></tr><tr><td>

Stage

</td><td>

Updates the stage of the work item. Custom field to maintain different stages of the transaction.

</td></tr><tr><td>

DeferredTill

</td><td>

Option to specify a time duration during which the same work item will not be picked. For example, 5 minutes.

</td></tr><tr><td>

Name

</td><td>

Name of the work item.

</td></tr><tr><td>

Type

</td><td>

The type of the work item. For example, for an accounting system queue, savings and current are types of accounts.

To configure the input field, see [Configure port properties](../task/configure-input-port-properties.md).

</td></tr><tr><td>

Remarks

</td><td>

Supporting remarks on the work item.

</td></tr><tr><td>

SLA

</td><td>

Service Level Agreement \(SLA\) of the work item completion.

</td></tr><tr><td>

ResponseContent

</td><td>

String content for the work item. Updates the stored content of a work item.

</td></tr><tr><td>

SensitiveRequestContent

</td><td>

Updates the sensitive content of a work item.

</td></tr><tr><td class="sub-head" colspan="2">

JSON PROPERTIES

</td></tr><tr><td colspan="2">

JSON PATH NOTATIONS

</td></tr><tr><td>

Name

</td><td>

Key-value pair \(JSON content\) for the request content. To add a key, do the following:

1.  Click the add key icon \(![Add key icon.](../image/add-image-icon.png)\).
2.  Enter the key name in the field.
3.  To add more keys, repeat the previous steps.
4.  To pass the value to these fields, see [Configure port properties](../task/configure-input-port-properties.md).


</td></tr><tr><td>

Sensitive

</td><td>

Sensitive content is updated for a work item. With this functionality, you can pass sensitive information through queues.

For example, if you want customer data to be encrypted in the queue, you must use the **Sensitive** field to store customer details such as credit card number, address, and so on.

When you add a key-value pair "City: Mumbai" in **SensitiveRequestContent** field and add another key-value pair "Country: India" in JSON Path Notation and the UpdateWorkItem is executed. Then, in the **SensitiveRequestContent** field, the output is combined to "City: Mumbai" and "Country: India".

</td></tr></tbody>
</table>
**Parent Topic:**[Queue](../concept/queue-connector.md)

