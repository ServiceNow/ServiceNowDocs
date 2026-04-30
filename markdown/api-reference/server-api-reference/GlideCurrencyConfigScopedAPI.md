---
title: GlideCurrencyConfig - Scoped
description: The GlideCurrencyConfig API provides methods to retrieve various configuration information for FX Currency fields.Instantiates a GlideCurrencyConfig object that enables the retrieval of global default FX Currency configuration information.Instantiates a GlideCurrencyConfig object that enables the retrieval of the configuration information for a specific FX Currency field.Returns the aggregation source value for an FX Currency field.Returns the field used as the source of the date and time for the currency conversion.Returns the number of digits to display for an FX Currency field.Returns the currency code used to convert the FX Currency value when it appears in lists and reports.Returns the rate table field used as a rate table filter for an FX Currency field.Returns the target table field used to filter the rate table records for an FX Currency field.Returns the rate table used to convert currency for an FX Currency field.Returns the reference currency for an FX Currency field.Returns the reference currency source for an FX Currency field.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideCurrencyConfig- Scoped

The GlideCurrencyConfig API provides methods to retrieve various configuration information for FX Currency fields.

You can acquire information for a specific FX Currency field by calling the [GlideCurrencyConfig\(Object ed\)](GlideCurrencyConfigScopedAPI.md#) constructor, which associates a specific FX Currency field to the instantiated object. When calling the various GlideCurrencyConfig\(\) methods, if a record exists in the FX Currency Configuration \[fx\_configuration\] table for the FX Currency field, the requested value is passed back. If a record or field is not available, the default value is passed back. You can also acquire the default FX Currency configuration values by calling the [GlideCurrencyConfig\(\)](GlideCurrencyConfigScopedAPI.md#) constructor.

For additional information on FX Currency configuration, see [Setting up and operating FX Currency fields](https://www.servicenow.com/docs/access?context=fx-currency&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

This class runs is in the `sn_currency` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideCurrencyConfig - GlideCurrencyConfig\(\)

Instantiates a GlideCurrencyConfig object that enables the retrieval of global default FX Currency configuration information.

When calling the available methods on this type of GlideCurrencyConfig object, the return values are the FX Currency global defaults from system properties. If a global default is not defined in system properties, a hard-coded default is returned \(this can also be an empty value if not configured\).

This object does not provide configuration information for a specific FX Currency field. To retrieve specific FX Currency field information, use the [GlideCurrencyConfig\(Object ed\)](GlideCurrencyConfigScopedAPI.md#) constructor.

For more information, see [Configuring FX Currency global settings](https://www.servicenow.com/docs/access?context=fx-currency-configure&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

```api-constructor
var cur_config = new sn_currency.GlideCurrencyConfig();
```

## GlideCurrencyConfig - GlideCurrencyConfig\(Object ed\)

Instantiates a GlideCurrencyConfig object that enables the retrieval of the configuration information for a specific FX Currency field.

When calling the available methods on this type of GlideCurrencyConfig object, the return values are from the FX Currency Configuration \[fx\_configuration\] record associated with the FX Currency field, if a record exists. If a record does not exist, default values are returned.

For more information, see [Configuring FX Currency global settings](https://www.servicenow.com/docs/access?context=fx-currency-configure&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|ed|GlideElementDescriptor|GlideElementDescriptor object of the FX Currency field to associate with the GlideCurrencyConfig object.|

```api-constructor
var grCurr = new GlideRecord('my_FXCurrency_table');
var curr_field = grCurr.getElement('currency');
var ed = curr_field.getED();
var cur_config = new sn_currency.GlideCurrencyConfig(ed);
```

## GlideCurrencyConfig - getAggregationSource\(\)

Returns the aggregation source value for an FX Currency field.

If called on an existing FX Currency field that has a corresponding FX Currency Configuration \[fx\_configuration\] record, returns the value of the Aggregation Source \(aggregation\_source\) field. Otherwise, if a new record, returns a default value.

For more information on aggregation source, see [Specify the table field and its currency display parameters](https://www.servicenow.com/docs/access?context=configure-fx-currency-field-behavior&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_zvy_j1r_sjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Source of values for aggregations. The returned value depends on the constructor used to instantiate the object.-   GlideCurrencyConfig\(Object ed\): If an fx\_configuration record exists, returns the aggregation\_source field from the fx\_configuration record that is associated with the FX Currency field specified by the GlideElementDescriptor passed in the constructor. If no fx\_configuration record, follows the GlideCurrencyConfig\(\) rules.
-   GlideCurrencyConfig\(\): If set, returns the value in the glide.currency2.aggregation\_source field in system properties. Otherwise, returns a hard-coded default of `reference`.

 Possible values:

-   default
-   as\_entered
-   reference

</td></tr></tbody>
</table>This code example returns the default aggregation source.

```
var cur_config = new sn_currency.GlideCurrencyConfig();
var curr_agg_source = cur_config.getAggregationSource();
```

This code example returns the aggregation source for a specific FX Currency field.

```
var grCurr = new GlideRecord('my_FXCurrency_table');
var curr_field = grCurr.getElement('currency');
var ed = curr_field.getED();
var cur_config = new sn_currency.GlideCurrencyConfig(ed);
var curr_agg_source = cur_config.getAggregationSource();
```

## GlideCurrencyConfig - getConversionDateSource\(\)

Returns the field used as the source of the date and time for the currency conversion.

If called on an existing FX Currency field that has a corresponding FX Currency Configuration \[fx\_configuration\] record, returns the value of the Conversion Date Source \(conversion\_date\_source\) field. Otherwise, if a new record, returns "null".

For more information on the Conversion Date Source field, see [Identify the rate table and date source for currency conversions](https://www.servicenow.com/docs/access?context=configure-fx-currency-field-behavior&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ddl_yyq_sjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Field in the record used as the conversion date source. The returned value depends on the constructor used to instantiate the object.-   GlideCurrencyConfig\(Object ed\): If an fx\_configuration record exists, returns the conversion\_date\_source field from the fx\_configuration record that is associated with the FX Currency field specified by the GlideElementDescriptor passed in the constructor. If no fx\_configuration record, follows the GlideCurrencyConfig\(\) rules.
-   GlideCurrencyConfig\(\): Returns `null`.

</td></tr></tbody>
</table>This code example returns the conversion date source for a specific FX Currency field.

```
var grCurr = new GlideRecord('my_FXCurrency_table');
var curr_field = grCurr.getElement('currency');
var ed = curr_field.getED();
var cur_config = new sn_currency.GlideCurrencyConfig(ed);
var curr_conv_date_src = cur_config.getConversionDateSource();
```

## GlideCurrencyConfig - getDisplayDigits\(\)

Returns the number of digits to display for an FX Currency field.

If called on an existing FX Currency field that has a corresponding FX Currency Configuration \[fx\_configuration\] record, returns the value of the Display Digits \(display\_digits\) field. Otherwise, if a new record, returns a default value.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qxs_myp_sjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number of digits to display for the FX Currency field. The returned value depends on the constructor used to instantiate the object.-   GlideCurrencyConfig\(Object ed\): If an fx\_configuration record exists, returns the value of the display\_digits field in the FX Currency Configuration \[fx\_configuration\] record that is associated with the FX Currency field specified by the GlideElementDescriptor passed in the constructor. If no fx\_configuration record, follows the GlideCurrencyConfig\(\) rules.
-   GlideCurrencyConfig\(\): If set, returns the value of the glide.currency2.display\_digits property in system properties. Otherwise, returns `-1`.

</td></tr></tbody>
</table>This code example returns the default number of display digits.

```
var cur_config = new sn_currency.GlideCurrencyConfig();
var curr_display_digits = cur_config.getDisplayDigits();
```

This code example returns the display digits for a specific FX Currency field.

```
var grCurr = new GlideRecord('my_FXCurrency_table');
var curr_field = grCurr.getElement('currency');
var ed = curr_field.getED();
var cur_config = new sn_currency.GlideCurrencyConfig(ed);
var curr_display_digits = cur_config.getDisplayDigits();
```

## GlideCurrencyConfig - getDisplayValue\(\)

Returns the currency code used to convert the FX Currency value when it appears in lists and reports.

If called on an existing FX Currency field that has a corresponding FX Currency Configuration \[fx\_configuration\] record, returns the value of the Display Value Currency \(display\_value\) field. Otherwise, if a new record, returns a default value.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ftg_bsk_qjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Currency code to use to display the FX Currency field. The returned value depends on the constructor used to instantiate the object.-   GlideCurrencyConfig\(Object ed\): If an fx\_configuration record exists, returns the display\_value field, which contains the currency code, from the fx\_configuration record that is associated with the FX Currency field specified by the GlideElementDescriptor passed in the constructor. If no fx\_configuration record, follows the GlideCurrencyConfig\(\) rules.
-   GlideCurrencyConfig\(\): If set, returns the value of the glide.currency2.display\_value property in system properties. Otherwise, returns `as_entered`.

 Possible values:

-   default: Global default. This is the value in the glide.currency2.display\_digits property.
-   as\_entered: Currency value as entered by the user.
-   in\_session\_currency: Currency value converted to the session currency. Session currency is based on the user's locale.
-   in\_reference\_currency: Reference value if computed and stored. Otherwise, the currency value converted to the reference currency.

</td></tr></tbody>
</table>This code example returns the default currency code.

```
var cur_config = new sn_currency.GlideCurrencyConfig();
var curr_display_value = cur_config.getDisplayValue();
```

This code example returns the display currency code for a specific FX Currency field.

```
var grCurr = new GlideRecord('my_FXCurrency_table');
var curr_field = grCurr.getElement('currency');
var ed = curr_field.getED();
var cur_config = new sn_currency.GlideCurrencyConfig(ed);
var curr_display_value = cur_config.getDisplayValue();
```

## GlideCurrencyConfig - getRateFilterRateTableField\(\)

Returns the rate table field used as a rate table filter for an FX Currency field.

If called on an existing FX Currency field that has a corresponding FX Currency Configuration \[fx\_configuration\] record, returns the value of the Rate Table Field \(rate\_filter\_rate\_table\_field\). Otherwise, if a new record, returns a default value.

For more information on rate table filters, see [Select the rate and target table fields used for filtering](https://www.servicenow.com/docs/access?context=configure-fx-currency-field-behavior&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_olm_5cr_sjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Field in the rate table used to filter the rate table records. The returned value depends on the constructor used to instantiate the object.-   GlideCurrencyConfig\(Object ed\): If an fx\_configuration record exists, returns the rate\_filter\_rate\_table\_field from the fx\_configuration record that is associated with the FX Currency field specified by the GlideElementDescriptor passed in the constructor. If no fx\_configuration record, follows the GlideCurrencyConfig\(\) rules.
-   GlideCurrencyConfig\(\): Returns `null`.

</td></tr></tbody>
</table>This code example returns the rate table field used to filter rate table records for a specific FX Currency field.

```
var grCurr = new GlideRecord('my_FXurrency_table');
var curr_field = grCurr.getElement('currency');
var ed = curr_field.getED();
var cur_config = new sn_currency.GlideCurrencyConfig(ed);
var curr_reference_currency = cur_config.getRateFilterRateTableField();
```

## GlideCurrencyConfig - getRateFilterTargetTableField\(\)

Returns the target table field used to filter the rate table records for an FX Currency field.

If called on an existing FX Currency field that has a corresponding FX Currency Configuration \[fx\_configuration\] record, returns the value of the Target Table Field \(rate\_filter\_target\_table\_field\). Otherwise, if a new record, returns a default value.

For more information on rate table filters, see [Select the rate and target table fields used for filtering](https://www.servicenow.com/docs/access?context=configure-fx-currency-field-behavior&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_a2y_gcr_sjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Field in the target table used/to use to filter the rate table. The returned value depends on the constructor used to instantiate the object.-   GlideCurrencyConfig\(Object ed\): If an fx\_configuration record exists, returns the rate\_filter\_target\_table\_field from the fx\_configuration record that is associated with the FX Currency field specified by the GlideElementDescriptor passed in the constructor. If no fx\_configuration record, follows the GlideCurrencyConfig\(\) rules.
-   GlideCurrencyConfig\(\): Returns `null`.

</td></tr></tbody>
</table>This code example returns the default rate filter, target table field.

```
var cur_config = new sn_currency.GlideCurrencyConfig();
var curr_rate_filter = cur_config.getRateFilterTargetTableField();
```

This code example returns the rate filter, target table field for a specific FX Currency field.

```
var grCurr = new GlideRecord('my_FXCurrency_table');
var curr_field = grCurr.getElement('currency');
var ed = curr_field.getED();
var cur_config = new sn_currency.GlideCurrencyConfig(ed);
var curr_rate_filter = cur_config.getRateFilterTargetTableField();
```

## GlideCurrencyConfig - getRateTable\(\)

Returns the rate table used to convert currency for an FX Currency field.

If called on an existing FX Currency field that has a corresponding FX Currency Configuration \[fx\_configuration\] record, returns the value of the Rate Table Field \(rate\_filter\_rate\_table\_field\). Otherwise, if a new record, returns a default value.

For more information on FX Currency rate tables, see [Identify the rate table and date source for currency conversions](https://www.servicenow.com/docs/access?context=configure-fx-currency-field-behavior&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ntg_knq_sjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Name of the rate table used to perform the currency conversion. The returned value depends on the constructor used to instantiate the object.-   GlideCurrencyConfig\(Object ed\): If an fx\_configuration record exists, returns the rate\_table\_field field from the fx\_configuration record that is associated with the FX Currency field specified by the GlideElementDescriptor passed in the constructor. If no fx\_configuration record, follows the GlideCurrencyConfig\(\) rules.
-   GlideCurrencyConfig\(\): If set, returns the value of the glide.currency2.system\_rate\_table property from system properties. Otherwise, returns `fx_system_rate`.

</td></tr></tbody>
</table>Returns the default rate table.

```
var cur_config = new sn_currency.GlideCurrencyConfig();
var curr_rate_table = cur_config.getRateTable();
```

Returns the rate table used for a specific FX Currency field.

```
var grCurr = new GlideRecord('my_FXCurrency_table');
var curr_field = grCurr.getElement('currency');
var ed = curr_field.getED();
var cur_config = new sn_currency.GlideCurrencyConfig(ed);
var curr_rate_table = cur_config.getRateTable();
```

## GlideCurrencyConfig - getReferenceCurrency\(\)

Returns the reference currency for an FX Currency field.

If called on an existing FX Currency field that has a corresponding FX Currency Configuration \[fx\_configuration\] record, returns the value of the Reference Currency \(reference\_currency\) field. Otherwise, if a new record, returns a default value.

For more information on reference currency, see [Set the reference currency](https://www.servicenow.com/docs/access?context=configure-fx-currency-field-behavior&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_tmf_qqq_sjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Reference currency as an ISO currency code. The returned value depends on the constructor used to instantiate the object.-   GlideCurrencyConfig\(Object ed\): If an fx\_configuration record exists, returns the reference\_currency field from the fx\_configuration record that is associated with the FX Currency field specified by the GlideElementDescriptor passed in the constructor. If no fx\_configuration record, follows the GlideCurrencyConfig\(\) rules.
-   GlideCurrencyConfig\(\): If set, returns the value of the glide.currency2.default\_reference\_currency system property. Otherwise the method applies the following rules, in the specified order, to determine the reference currency code:
    -   If the glide.system.reference\_currency system property is set to true, uses the value in the glide.system.reference\_currency.code system property.
    -   The value in the glide.system.locale system property \(which implies a currency\).
    -   Default locale of the Java Virtual Machine on which the instance is running.

</td></tr></tbody>
</table>This code example returns the default reference currency.

```
var cur_config = new sn_currency.GlideCurrencyConfig();
var curr_reference_currency = cur_config.getReferenceCurrency();
```

This code example returns the reference currency for a specific FX Currency field.

```
var grCurr = new GlideRecord('my_FXCurrency_table');
var curr_field = grCurr.getElement('currency');
var ed = curr_field.getED();
var cur_config = new sn_currency.GlideCurrencyConfig(ed);
var curr_reference_currency = cur_config.getReferenceCurrency();
```

## GlideCurrencyConfig - getReferenceCurrencySource\(\)

Returns the reference currency source for an FX Currency field.

If called on an existing FX Currency field that has a corresponding FX Currency Configuration \[fx\_configuration\] record, returns the value \(dot-walk path\) of the Reference Currency Source \(reference\_currency\_source\) field. Otherwise, if a new record, returns a default value.

For more information on reference currency source, see [Set the reference currency](https://www.servicenow.com/docs/access?context=configure-fx-currency-field-behavior&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_zsb_swq_sjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Dot-walk path of the field used/to use as the reference currency. The returned value depends on the constructor used to instantiate the object.-   GlideCurrencyConfig\(Object ed\): If an fx\_configuration record exists, returns the reference\_currency\_source field from the fx\_configuration record that is associated with the FX Currency field specified by the GlideElementDescriptor passed in the constructor. If no fx\_configuration record, follows the GlideCurrencyConfig\(\) rules.
-   GlideCurrencyConfig\(\): Returns `null`.

</td></tr></tbody>
</table>This code example returns the default reference currency source.

```
var cur_config = new sn_currency.GlideCurrencyConfig();
var curr_reference_currency = cur_config.getReferenceCurrencySource();
```

This code example returns the reference currency source for a specific FX Currency field.

```
var grCurr = new GlideRecord('my_FXCurrency_table');
var curr_field = grCurr.getElement('currency');
var ed = curr_field.getED();
var cur_config = new sn_currency.GlideCurrencyConfig(ed);
var curr_reference_currency = cur_config.getReferenceCurrencySource();
```

