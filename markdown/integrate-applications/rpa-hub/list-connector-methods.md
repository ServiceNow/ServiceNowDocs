---
title: List connector methods
description: The List connector methods perform various actions on list items as part of an automation workflow. You must first expose the methods before using.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [List, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# List connector methods

The List connector methods perform various actions on list items as part of an automation workflow. You must first expose the methods before using.

## Add

Adds a single list item.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Item|Name of the list item.|Data in|Object|None|Yes|

## AddList

Adds a list of items.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|Notes|
|---------|-----------|--------------|---------|-------------|----------|-----|
|List|List of items.|Data in|Object|None|Yes|You can pass the list items from a variable or an appropriate component.|

## Contains

Returns the Boolean value based on whether a list item exists.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Item|Name of the list item that the method searches.|Data in|Object|None|Yes|
|Return|Returns True if list item found, else, returns False.|Data out|Boolean|Not applicable|Not applicable|

## Count

Returns the total count of list items added.

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the total count of list items added.|Data out|Integer|Not applicable|Not applicable|

## FindByProperty

Finds a list item based on the specified key and value. You must create at least one key value pair list item before executing this method.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Prop|The key in the key value pair.|Data in|String|None|Yes|
|Value|The value in the key value pair.|Data in|String|None|Yes|
|Found|Returns True if list item found, else, returns False.|Data out|Boolean|Not applicable|Not applicable|
|Item|if the Found parameter is True, the method returns the list item.|Data out|Object|Not applicable|Not applicable|

## FindText

Finds text or regex in the list items based on the specified filter and returns the total occurrences of the text and the text itself.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

<table id="table_tjd_l2r_4tb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th><th>

Default value

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

SearchText

</td><td>

Text that the method searches in the list items.

</td><td>

Data in

</td><td>

String

</td><td>

None

</td><td>

Yes

</td></tr><tr><td>

FindBy

</td><td>

Option to indicate whether the method searches a text or regex.

</td><td>

Data in

</td><td>

String

</td><td>

None

</td><td>

Yes

</td></tr><tr><td>

MatchType

</td><td>

Option to indicate whether the type of match will be:-   An exact match
-   Match case
-   Containing the specified characters.

</td><td>

Data In

</td><td>

String

</td><td>

None

</td><td>

Yes

</td></tr><tr><td>

Count

</td><td>

Returns the total occurrences of the match.

</td><td>

Data out

</td><td>

Integer

</td><td>

Not applicable

</td><td>

Not applicable

</td></tr><tr><td>

Outlist

</td><td>

Returns the list of matches.

</td><td>

Data out

</td><td>

List

</td><td>

Not applicable

</td><td>

Not applicable

</td></tr></tbody>
</table>## GetItem

Returns a list item based on its index value.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Index|Index value of the list item.|Data in|Integer|None|Yes|
|Return|Returns the list item.|Data out|Object|Not applicable|Not applicable|

## GetItems

Returns the list items based on their index values. You must configure the index values first.

To configure, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Click the add index icon \(![Add index icon.](../image/add-image-icon.png)\).
3.  Enter the index value.
4.  Update the data type of the index value.
5.  Repeat the steps to add more index values.
6.  Click **OK**.

    A data out port is created with each index value. The data out port returns the list item corresponding to the index value.


## GetList

Returns all list items and lists created.

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the list items and lists.|Data out|Array|None|Not applicable|

## Remove

Removes the specified list item.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Item|List item the method removes.|Data in|Object|None|Yes|

## RemoveAll

Removes all list items added.

## Reverse

Reverses the order of the index values of the list items.

## SetItems

Updates the values of the list items. To use the method, you must first configure the method.

To configure, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Click the add index icon \(![Add index icon.](../image/add-image-icon.png)\).
3.  Enter the index value.
4.  Update the data type of the index value.
5.  Repeat the steps to add more index values.
6.  Click **OK**.

    A data in port is created with each index value.


To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Item|Accepts the value of the list items.|Data in|Object|None|Yes|

## Sort

Sorts the list items.

## ToArray

Returns the list items in the form of an array. You must add more than one list item before executing this method.

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the list items in the form of an array list.|Data out|Array list|Not applicable|Not applicable|

**Parent Topic:**[List](list-connector.md)

