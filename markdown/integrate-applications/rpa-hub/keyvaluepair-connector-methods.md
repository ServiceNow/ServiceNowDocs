---
title: KeyValuePair connector methods
description: The Keyvalue pair connector methods perform various actions on key value pairs. In an automation flow, the methods are connected with other methods and components. To use the methods, you must first expose them.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Keyvalue pair, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# KeyValuePair connector methods

The Keyvalue pair connector methods perform various actions on key value pairs. In an automation flow, the methods are connected with other methods and components. To use the methods, you must first expose them.

## Add

Adds a keyvalue pair.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Key|Name of the key.|Data in|String|None|Yes|
|Value|Value of the key.|Data in|Object|None|Yes|
|IgnoreDuplicates|If the value is True, the method ignores a duplicate key. Else, if the value is False, the method returns an error message.|Data in|Boolean|None|No|

## Clear

Clears all keyvalue pairs.

## ContainsKey

Returns True if the specified key exists, else, returns False.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Key|Name of the key.|Data in|String|None|Yes|
|Return|Returns True if the specified key exists, else, returns False.|Data out|Boolean|Not applicable|Not applicable|

## ContainsValue

Returns True if the specified key value exists, else, returns False.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Value|Name of the key value.|Data in|String|None|Yes|
|Return|Returns True if the specified key value exists, else, returns False.|Data out|Boolean|Not applicable|Not applicable|

## Count

Returns the total count of keyvalue pairs.

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the total count of keyvalue pairs.|Data out|Integer|Not applicable|Not applicable|

## Delete

Removes the specified key.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Key|Name of the key.|Data in|String|None|Yes|

## GetItem

Returns the value of the specified key.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Key|Name of the key.|Data in|String|None|Yes|
|Return|Returns the value of the key.|Data out|Object|Not applicable|Not applicable|

## GetItems

Returns the values of multiple keys. You must first configure the keys in the method.

To configure, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Click the add keys icon \(![Add keys icon.](../image/add-image-icon.png)\).
3.  Enter the key name.
4.  Update the key data type from the list.
5.  Repeat the steps to set multiple key names.
6.  Click **OK**.

    A Data out port is created with each key name you set.


|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Key|Returns the value of the key.|Data out|Object|Not applicable|Not applicable|

## GetItemsByIndex

Returns the key values based on their index. You must first configure the indexes in the method.

To configure, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Click the add indexes icon \(![Add keys icon.](../image/add-image-icon.png)\).
3.  Enter the key index.
4.  Update the key data type from the list.
5.  Repeat the steps to set multiple key indexes.
6.  Click **OK**.

    A Data out port is created with each key index you set.


|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Key index|Returns the value of the key.|Data out|Object|Not applicable|Not applicable|

## ParseFromText

Parses the specified text into key value pairs. It can create multiple keyvalue pairs.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Text|Text comprising the keys and values that the method parses.|Data in|String|None|Yes|
|ItemSeparator|Separator between two keyvalue pairs.|Data in|String|None|Yes|
|KeyValueSeparator|Separator between the key and its value.|Data in|String|None|Yes|
|ClearBeforeParse|If True, clears any existing keyvalue pair before parsing.|Data in|Boolean|None|No|

## Reverse

Reverses the key indexes.

**Tip:** After executing the method, you can see the output by executing the GetItemsByIndex method.

## SetData

Need information.

## SetItem

Updates the value of a key.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Key|Name of the key.|Data in|String|None|Yes|
|Value|Updated value of the key.|Data in|Object|None|Yes|

**Tip:** Test the updated value by executing the GetItemsByIndex method.

## SetItems

Updates the values of the specified keys. You must first configure the keys in the method.

To configure the keys, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Click the add keys icon \(![Add keys icon.](../image/add-image-icon.png)\).
3.  Enter the key name.
4.  Update the key data type from the list.
5.  Repeat the steps to set multiple key names.
6.  Click **OK**.

    A Data in port is created with each key name you set.


To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Key|Updated value of the key.|Data in|Object|None|Yes|

**Tip:** Test the updated value by executing the GetItemsByIndex method.

## SetItemsByIndex

Updates the values of the keys based on the specified indexes. You must first configure the indexes in the method.

To configure the indexes, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Click the add indexes icon \(![Add keys icon.](../image/add-image-icon.png)\).
3.  Enter the key index.
4.  Update the key data type from the list.
5.  Repeat the steps to set multiple key indexes.
6.  Click **OK**.

    A Data in port is created with each key index you set.


|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Key Index|Index of the key.|Data in|Object|None|Yes|

**Tip:** Test the updated value by executing the GetItemsByIndex method.

## ToJSON

Renders the keyvalue pairs to the JSON format.

## ToText

Renders the keyvalue pairs to the text format.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|ValuesOnly|If True, the method renders only the values of the keys, else, renders the keyvalue pair.|Data in|Boolean|None|No|
|Return|Returns the keyvalue pair to the text format.|Data out|String|Not applicable|Not applicable|

**Parent Topic:**[Keyvalue pair](../concept/keyvaluepair.md)

