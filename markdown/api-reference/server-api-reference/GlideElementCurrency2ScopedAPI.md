---
title: GlideElementCurrency2 - Scoped
description: The GlideElementCurrency2 API provides methods to perform operations on Foreign Exchange \(FX\) Currency fields \(also known as Currency2\) within the current GlideRecord.Returns an FX Currency field display string, as entered by the user, from the associated GlideRecord.Returns the display value of an FX Currency field within the associated GlideRecord.Returns the reference currency value of an FX Currency field within the associated GlideRecord.Returns the session currency value of the associated FX Currency field within the current GlideRecord.Sets the display value of an FX Currency field with the specified currency value.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideElementCurrency2- Scoped

The GlideElementCurrency2 API provides methods to perform operations on Foreign Exchange \(FX\) Currency fields \(also known as Currency2\) within the current GlideRecord.

This API provides methods that enable you to perform the following:

-   Obtain the FX Currency field display string, as entered by the user.
-   Obtain the display value of an FX Currency field.
-   Obtain the reference currency value of an FX Currency field.
-   Obtain the session currency value of an FX Currency field.
-   Set the display value of an FX Currency field.

The GlideElementCurrency2 class has no constructor.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideElementCurrency2 - getAsEnteredDisplayValue\(\)

Returns an FX Currency field display string, as entered by the user, from the associated GlideRecord.

For additional information on FX Currency fields, see [Setting up and operating FX Currency fields](https://www.servicenow.com/docs/access?context=fx-currency&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Display currency string as entered by the user.|

This example shows how to call the method.

```
var tablename = 'my_currency2_table';
var setcur2 = new GlideRecord(tablename);
setcur2.initialize();
setcur2.currency_2_field.setDisplayValue('JPY;999999.1234');
setcur2.insert();
gs.info('As entered display value: ' + setcur2.currency_2_field.getAsEnteredDisplayValue());
```

Output:

```
As entered display value: ¥999,999.12
```

## GlideElementCurrency2 - getDisplayValue\(\)

Returns the display value of an FX Currency field within the associated GlideRecord.

Depending on how the display\_value is set in the FX Currency Configuration \[fx\_configuration\] table, the returned value may be the:

-   Currency value as entered by the user
-   Currency value converted to the session currency \(based on the user's locale\)
-   Currency value converted to the reference currency

For additional information on FX Currency and the configuration table, see [Configure FX Currency global settings](https://www.servicenow.com/docs/access?context=fx-currency-configure&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Display currency value|

This example shows how to call the method.

```
var tablename = 'my_FXcurrency_table';
var setcur2 = new GlideRecord(tablename);
setcur2.initialize();
setcur2.currency_2_field.setDisplayValue('JPY;999999.1234');
setcur2.insert();
gs.info('Display Value: ' + setcur2.currency_2_field.getDisplayValue());
```

Output:

```
Display Value: ¥999,999.12
```

## GlideElementCurrency2 - getReferenceDisplayValue\(\)

Returns the reference currency value of an FX Currency field within the associated GlideRecord.

Reference currency is the common currency into which all currency values in a field are converted. The currency code that the getReferenceDisplayValue\(\) method uses to derive the reference currency is based on the following:

-   If an instance record exists, then the method uses the value in the reference\_currency field of the FX Currency \[fx\_currency2\_instance\] table.
-   If an instance record does not exist, then the method uses the reference currency that would be set on the instance record when the instance record is eventually created \(in the following order\):
    -   If set, the **reference\_currency** in the FX Currency Configuration \[fx\_configuration\] table.
    -   If set, the **reference\_currency\_source** in the FX Currency Configuration \[fx\_configuration\] table.
    -   System default, system reference currency.

For additional information on the values in the FX Currency Configuration \[fx\_configuration\] table, see [Setting up and operating FX Currency fields](https://www.servicenow.com/docs/access?context=fx-currency&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Reference currency amount for the associated FX Currency display value.|

This example assumes the reference currency code is USD and uses the default conversion rate specified in the FX Currency Configuration \[fx\_configuration\] table. The output will change based on locale.

```
var tablename = 'my_currency2_table';
var setcur2 = new GlideRecord(tablename);
setcur2.initialize();
setcur2.currency_2_field.setDisplayValue('JPY;999999.1234');
setcur2.insert();
gs.info('Reference display value: ' + setcur2.currency_2_field.getReferenceDisplayValue());
```

Output:

```
Reference display value: $8,677.99
```

## GlideElementCurrency2 - getSessionDisplayValue\(\)

Returns the session currency value of the associated FX Currency field within the current GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Currency value converted to the session currency, which is based on the current user's locale.|

This example assumes the session locale is language code = eng and country code = USA, and uses the default conversion rate specified in the FX Currency Configuration \[fx\_configuration\] table. The output will change based on locale.

```
var tablename = 'my_currency2_table';
var setcur2 = new GlideRecord(tablename);
setcur2.initialize();
setcur2.currency_2_field.setDisplayValue('JPY;999999.1234');
setcur2.insert();
gs.info('Session display value: ' + setcur2.currency_2_field.getSessionDisplayValue());
```

Output:

```
Session display value: $8,677.99
```

## GlideElementCurrency2 - setDisplayValue\(String displayValue\)

Sets the display value of an FX Currency field with the specified currency value.

For additional information on FX Currency fields, see [Setting up and operating FX Currency fields](https://www.servicenow.com/docs/access?context=fx-currency&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

<table id="table_enw_5jd_fy" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

displayValue

</td><td>

String

</td><td>

Value to set in the FX Currency field in the format `<currency code>;<currency amount>`. You must format the `<currency amount>` field in the user's locale.For example, if the user's locale is USA/eng, the passed in `<currency amount>` would be 123.45. If the user's local is FRA/fre, the passed in `<currency amount>` would be 123,45.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to call the method.

```
var tablename = 'my_FXcurrency_table';
var setcur2 = new GlideRecord(tablename);
setcur2.initialize();
setcur2.currency_2_field.setDisplayValue('JPY;999,999.1234');
setcur2.insert();
```

