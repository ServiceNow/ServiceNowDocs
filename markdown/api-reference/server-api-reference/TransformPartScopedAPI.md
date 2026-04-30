---
title: TransformPart - Scoped, Global
description: The TransformPart API provides methods to specify details of the transform to be done.Add the specified number to the value in each time stamp.Aggregate the selected metric series into one series containing the average value for each time stamp.Create a result set that for each time stamp returns specified number of bottom values. This method results in 'count' number of series. Each value retains the label of its source series.Replace the value in any time stamp that is greater than the specified value with the specified value.Mark this transform for collection.Aggregate the selected metric series into one series containing the number of values for each time stamp.Divide the value in each time stamp by the specified number.Create a series using the specified aggregator for the specified time.Replace the value in any time stamp that is less than the specified value with the specified value.Create series made up of the value that the specified percentage of values is below. Returns a series for each fraction in the specified array.Return the part of the result relevant to this transform.Specify a field by which to group data. To specify multiple fields, run successive calls individually.pull this one too? \(see transformer\); check to see if this one's necessary Example uses models. Reserve for future when model customer doc is ready \(not available at this time\)Create a data value for a NaN data item by interpolating from adjacent data values.Perform an Interquartile range transform.Add a label for the resulting series.Returns at most the specified number of values, starting at the most recent non-NaN value.Run a logarithm on the value in each time stamp where the result is the log of the specified base for the time stamp value.Returns a series with the maximum value for each time stamp.Create a series containing the median of values for each time stamp across a set of series.Specify the metric field to be used in the transform.Returns a series with the minimum value for each time stamp.Multiply the value in each time stamp by the specified number.Partition the series into intervals of the same duration.Specify the number of data points to include in the result.Specify the minimum and maximum number of samples to include in the result.Specify an aggregator to use to create a result set of the specified size. The aggregator can be LAST, AVG, MIN, or MAX.Specify an aggregator to use to create a result set over the specified duration. The aggregator can be LAST, AVG, MIN, or MAX.Round the value in each time stamp to the specified precision.Create a series containing the standard deviation of values for each time stamp across a set of series.Subtract the specified number from the value in each time stamp.Aggregate the selected metric series into one series containing the sum of all values for each time stamp.Create a result set that for each time stamp returns the specified number of top values. This method results in 'count' number of series. Each value retains the label of its source series.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 13
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# TransformPart - Scoped, Global

The TransformPart API provides methods to specify details of the transform to be done.

You can call this class in scoped and global server scripts. When using the TransformPart class, use the `sn_clotho` namespace identifier.

There is no constructor for this class. TransformPart objects are returned by many Transformer and TransformPart methods.

The methods of this class define the transforms to be done. The actual transformation is done when the execute\(\) method is called on the Transformer object.

The order the TransformPart methods are called is important.

-   You must call the metric\(\) method before calling a transform method.
-   You cannot use the metric\(\) or groupBy\(\) methods after calling a transform method.
-   Intermediate transforms are not returned in a result unless the collect\(\) method is called for the intermediate result you want.

    ```
    // where tp is a TransformPart object
    // example 1
    tp.avg().add(2);
    var tr = tp.execute(); 
    // tr contains avg+2, but not avg
     
    // example 2
    tp.avg().add(2);
    tp.avg();
    var tr = tp.execute(); 
    // tr contains both avg and avg + 2
    
    // example 3
    tp.avg().collect().add(2);
    var tr = tp.execute(); 
    // tr contains both avg and avg + 2
    ```


This class is part of the MetricBase application.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TransformPart - add\(Number constant\)

Add the specified number to the value in each time stamp.

|Name|Type|Description|
|----|----|-----------|
|constant|Number|The number to add to the value in each time stamp.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - avg\(\)

Aggregate the selected metric series into one series containing the average value for each time stamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - bottom\(Number count\)

Create a result set that for each time stamp returns specified number of bottom values. This method results in 'count' number of series. Each value retains the label of its source series.

|Name|Type|Description|
|----|----|-----------|
|count|Number|The number of series to return. The series are labeled 0 to count - 1.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - ceil\(Number ceiling\)

Replace the value in any time stamp that is greater than the specified value with the specified value.

|Name|Type|Description|
|----|----|-----------|
|ceiling|Number|The maximum allowed value for any time stamp.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - collect\(\)

Mark this transform for collection.

Transforms that are part of a chain, but not the last transform, are by default not collected. A collected transform is returned as part of the transform result.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - count\(\)

Aggregate the selected metric series into one series containing the number of values for each time stamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - div\(Number constant\)

Divide the value in each time stamp by the specified number.

|Name|Type|Description|
|----|----|-----------|
|constant|Number|The number by which to divide the value of each time stamp.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - filter\(Object aggregator, Object duration\)

Create a series using the specified aggregator for the specified time.

<table id="table_rn2_btj_4bb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aggregator

</td><td>

Object

</td><td>

Can be:-   AVG
-   CHISQUARE
-   LAST
-   MAX
-   MEDIAN
-   MIN
-   STDDEV

 For definitions of these options, see [MetricBase transforms](https://www.servicenow.com/docs/access?context=metricbase-transforms&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

</td></tr><tr><td>

duration

</td><td>

Object

</td><td>

Time period for the series.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|TransformPart|TransformPart object that you can use to specify transform characteristics.|

## TransformPart - floor\(Number floor\)

Replace the value in any time stamp that is less than the specified value with the specified value.

|Name|Type|Description|
|----|----|-----------|
|floor|Number|The minimum value for any time stamp.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - fractiles\(Array fractions\)

Create series made up of the value that the specified percentage of values is below. Returns a series for each fraction in the specified array.

The value in a time stamp in a returned series is the value at which the specified fraction of the samples for that time stamp is below. For example, if the fraction is 0.5, then the value in the time stamp is the value where half the values in the input series are below \(median\).

|Name|Type|Description|
|----|----|-----------|
|fractions|Array of numbers|The fractions to use on the input series.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics. Contains one series for each fraction specified.|

```
// returns a single series containing the median for each time stamp, which
// means that half a time stamp's values are below the returned value 
fractiles([.5]) 
// returns four series, one series for each of the 25%, 50%, 75%, and 100% quartiles 
fractiles([.25, .5, .75, 1])
// returns the median, 95% percentile, the max value
fractiles([.50, .95, 1]) 
```

## TransformPart - getResult\(\)

Return the part of the result relevant to this transform.

The collect\(\) method must be called before the execute\(\) method, and the execute\(\) method must be called before calling the getResult\(\) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|TransformResult|Contains the transform results associated with this part of the transform.|

```
var t = new sn_clotho.Transformer(drones);
t.metric("mb_demo_mt_altitude");
var avgTform = t.avg();
t.execute();
var avgTformResult = avgTform.getResult();
```

## TransformPart - groupBy\(String field\)

Specify a field by which to group data. To specify multiple fields, run successive calls individually.

**Note:** The groupBy\(\) method cannot be called after a transform has been run.

|Name|Type|Description|
|----|----|-----------|
|field|String|Name of a field in the table by which to group the transform results.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

The following example shows how to group altitude average metrics by fleet and model fields.

```
transformer.groupBy("fleet,model").metric("mb_demo_mt_altitude").avg().label('%g:fleet: - %g:model:');

var transformPart = transformer.groupBy("fleet,model")

transformPart.metric("mb_demo_mt_altitude").avg().label('%g:fleet: - %g:model:');
```

## TransformPart - interpolate\(Object count\)

Create a data value for a NaN data item by interpolating from adjacent data values.

|Name|Type|Description|
|----|----|-----------|
|count|Object|Specifies the number of data samples in each direction to check for a non NaN value. If if a non NaN value is not found, NaN is used.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - iqr\(\)

Perform an Interquartile range transform.

Creates a result set of four series.

-   IQR, the median of all entries
-   IQR range, below Q1-1.5IQR, or above Q3+1.5IQR
-   Q1, the median of the smallest half of entries
-   Q3, the median of the largest half of entries

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - label\(String label\)

Add a label for the resulting series.

|Name|Type|Description|
|----|----|-----------|
|label|String|The label for the transform results.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - limit\(Object count\)

Returns at most the specified number of values, starting at the most recent non-NaN value.

|Name|Type|Description|
|----|----|-----------|
|count|Object|A number of time stamps.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - log\(Number base\)

Run a logarithm on the value in each time stamp where the result is the log of the specified base for the time stamp value.

|Name|Type|Description|
|----|----|-----------|
|base|Number|The base for the logarithm calculation.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - max\(\)

Returns a series with the maximum value for each time stamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - median\(\)

Create a series containing the median of values for each time stamp across a set of series.

If there are n series in the TranformPart object, then if n is odd, the \(n / 2 + 1\) value for a time stamp is the median. If n is even, the average of the \(n / 2\) and \(n / 2 + 1\) values for a time stamp is the median.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - metric\(String metric\)

Specify the metric field to be used in the transform.

You can specify multiple metrics to be used in the transform. The metric\(\) method cannot be called after the transform has been run.

|Name|Type|Description|
|----|----|-----------|
|metric|String|Name of the metric field.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - min\(\)

Returns a series with the minimum value for each time stamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - mul\(Number constant\)

Multiply the value in each time stamp by the specified number.

|Name|Type|Description|
|----|----|-----------|
|constant|Number|The number by which to multiply the value of each time stamp.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - partition\(String aggregator, GlideDateTime duration, GlideDateTime base\)

Partition the series into intervals of the same duration.

|Name|Type|Description|
|----|----|-----------|
|aggregator|String|The aggregator to use. Can be min, max, avg, or last.|
|duration|GlideDateTime or an ISO 8601 formatted string|The interval length.|
|base|GlideDateTime or an ISO 8601 formatted string|The zero offset for partitioning. For example, if you partition by day \(24h\), then set the base to Monday at midnight in your time zone. If you partition by 30 days, then set the base to 1st day of the most recent month.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - resample\(Number count\)

Specify the number of data points to include in the result.

Aligns a series with a fixed number of data points in the given range. If the original series has more data points than specified, multiple values are averaged. If the original series has fewer data points than specified, data points are added by interpolating data points between existing data points.

You can use the resample\(\) method to reduce the number of samples in the result to more closely match the number of samples you are going to display.

|Name|Type|Description|
|----|----|-----------|
|count|Number|The number of samples to include in the result.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - resample\(Number min, Number max\)

Specify the minimum and maximum number of samples to include in the result.

This method is useful when you are showing series with different time periods \(granularities\).

This method determines the average number of points per series and if that fits between the specified minimum and maximum, each series is resampled to that average number of points. If the calculated average is greater than the maximum specified or smaller than the minimum specified, the specified maximum or minimum is used.

|Name|Type|Description|
|----|----|-----------|
|min|Number|The minimum number of samples to include in the result. If not enough samples are available, interpolation is used to create samples.|
|max|Number|The maximum number of samples to include in the result.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - resample\(String aggregator, Number numValues\)

Specify an aggregator to use to create a result set of the specified size. The aggregator can be LAST, AVG, MIN, or MAX.

You can use the resample\(\) method to reduce the number of samples in the result to more closely match the number of samples you are going to display.

<table id="table_cfh_23j_qcb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aggregator

</td><td>

String

</td><td>

Can be LAST, AVG, MIN, or MAX.

</td></tr><tr><td>

numValues

</td><td>

Number

</td><td>

The number of samples to include in the result set.When the number of values requested is greater than the number of values in the data for the requested time period, interpolate\(\) is used to add values between existing points to reach the requested number of values.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - resample\(String aggregator, GlideDuration duration\)

Specify an aggregator to use to create a result set over the specified duration. The aggregator can be LAST, AVG, MIN, or MAX.

Resamples the underlying data to the requested period.

-   When the time series is stored at a 1 minute interval and `resample(AVG, new GlideDuration("1:00"))` is called, the result will have one data point at every hour reflecting the average of the previous 60 values.
-   When the period requested is smaller than the period of the data, interpolation is used to calculate the intervening data points.

You can use the resample\(\) method to reduce the number of samples in the result to more closely match the number of samples you are going to display.

|Name|Type|Description|
|----|----|-----------|
|aggregator|String|Can be LAST, AVG, MIN, or MAX.|
|duration|GlideDuration|The time period for the result set.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - round\(Number precision\)

Round the value in each time stamp to the specified precision.

Performs this calculation on each value.

```
(v / precision) * precision
```

|Name|Type|Description|
|----|----|-----------|
|precision|Number|The value to be used in the rounding calculation.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - stddev\(\)

Create a series containing the standard deviation of values for each time stamp across a set of series.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - sub\(Object constant\)

Subtract the specified number from the value in each time stamp.

|Name|Type|Description|
|----|----|-----------|
|constant|Object|The number to subtract from the value in each time stamp.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - sum\(\)

Aggregate the selected metric series into one series containing the sum of all values for each time stamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

## TransformPart - top\(Number count\)

Create a result set that for each time stamp returns the specified number of top values. This method results in 'count' number of series. Each value retains the label of its source series.

|Name|Type|Description|
|----|----|-----------|
|count|Number|The number of series to return. The series are labeled 0 to count - 1.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify transform characteristics.|

