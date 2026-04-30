---
title: Creating set aggregates
description: You can collect the average, count, maximum, minimum, and sum of the data in any field in a set by using a set aggregate.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 5
breadcrumb: [Configure sets, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Creating set aggregates

You can collect the average, count, maximum, minimum, and sum of the data in any field in a set by using a set aggregate.

Set aggregates collect the data for each field in the set and output the result. Options include average, count, maximum, minimum, and sum. For example, a sum aggregate on a number field called Quantity will store the sum of all Quantity field values in the set. These aggregates function as a field outside of the set, can be used in global rules, and can be displayed anywhere in the layout.

To create an aggregate, open a set, scroll to the subfield that you want to aggregate, and click **Create New Aggregate**. You can then choose the aggregate type and give the new aggregate a name.

You can add the aggregate to the layout just like any other field, and deploy.

![Set layout](../images/cpq-sets-aggregates-1.png)

Below is the new sum aggregate during runtime:

![Create set screen](../images/cpq-sets-aggregates-2.png)

**Note:** The Sandwich Sum aggregate represents the sum of the Quantity field. This is not to be confused with the Sandwich Size of 3, which is the number of rows in the set.

Although the five aggregate types seem straightforward, there are important details about how they function with Boolean fields, picklist fields, and fields that have blank values. The following sections clarify these particulars.

## The Count aggregate

This aggregate can cause the most confusion. Count can be defined as “count the number of times the field has defined values in the set.” It tallies instances of the following types of values:

-   Non-blank
-   Non-zero
-   Non-false

For both single-select and multi-select picklists, the count aggregate is based on how many indexes have a value selected. The Count aggregate for the following sample field would be 2, because indexes 1 and 2 have values. Indexes 3, 4, and 5 donʼt count because they are blank.

![The Count aggregate](../images/cpq-sets-aggregates-5.png)

**Note:** For multi-select picklists, it does not matter how many values are selected—it counts as one.

## Number field

![Number field](../images/cpq-sets-aggregates-3.png)

The count aggregate on this field would be 3 \(from index 1, 2, and 3\).

## Boolean field

![Boolean field](../images/cpq-sets-aggregates-4.png)

The count aggregate on this would be 2.

## The Average, Minimum, Maximum, and Sum aggregates

An average aggregate runs on all iterations of the number field in the set, including zero values. This is in contrast to count aggregates, which ignore zero number values.

![The Average, Minimum, Maximum, and Sum aggregates](../images/cpq-sets-aggregates-7.png)

In this number field, indexes 1, 2, 3, and 4 add up to a quantity of 8. Since Index 3 with the 0 value is included, 4 is the divisor and the average is 8/4=2.

This “including-zero” behavior is true for Sum aggregates, Minimum aggregates, and Maximum aggregates as well. In the example above, the minimum aggregate value is 0 since that is the smallest value.

An average aggregate on a Boolean field will usually be in decimal form. It lets the user know what percentage of the indexes are selected as true. In the following Boolean field, three of the six indexes' Select Option values are true, and the resulting aggregate is 0.5.

![The Average, Minimum, Maximum, and Sum aggregates](../images/cpq-sets-aggregates-8.png)

A sum aggregate will show the number of Boolean fields marked as true. In the example provided, the aggregate is 3.

A maximum aggregate will be 0 unless one of the Boolean fields is selected, in which case it will be 1.

A minimum aggregate will be 0 unless all of the Boolean fields are selected, in which case it will be 1.

## Aggregates on picklist subfields

Four of the five aggregates \(average, minimum, maximum and sum\) work only on number values, not text. So if you add one of these aggregates on a set field that is a picklist, you will get an error once you deploy and select a text field option.

For example, suppose two fields were created. Both fields had the same field options, but one is a single-select picklist and one is a multi-select picklist. Here are the field options:

![Aggregates on picklist subfields](../images/cpq-sets-aggregates-9.png)

The fourth field option uses the word “four” instead of the number 4. As noted above, when deployed and “four” is selected, an error message occurs:

![Aggregates on picklist subfields](../images/cpq-sets-aggregates-10.png)

But if we select the numeric based options, the aggregates work.

![Aggregates on picklist subfields](../images/cpq-sets-aggregates-11.png)

In the following single-select picklist field, there are four indexes. The picklist “Toast Time” has the option label displayed as text, but behind the scenes, the option value is numeric.

![Aggregates on picklist subfields](../images/cpq-sets-aggregates-12.png)

The four values selected are “One Minute” \(1\), ”Two Minutes” \(2\), blank, and “Five Minutes” \(5\). By applying each of the aggregates to the single-select picklist field, the result is:

-   Sum: 8 = 1 + 2 + 0 + 5
-   Maximum: 5 \(the largest field option value selected\)
-   Minimum: 1 \(The blank index does not apply to the minimum\)
-   Average: 2.66 = \(1 + 2 + 5\) / 3 \(The blank index does not count toward the total and the divisor\)
-   Count: 3 \(The blank value does not apply to a count aggregate\)

Keep in mind that blank picklist values count towards the minimum, maximum, sum, and average aggregates.

In the following picklist field, Toast Time has been converted into a multi-select picklist. The four indexes have the following option values: \[1, 5\], \[2\], \[ \], and \[2, 5\].

![Aggregates to the field](../images/cpq-sets-aggregates-18.png)

By applying each of the aggregates to the field, the results are:

-   Sum: 15 = \(1 + 5\) + 2 + 0 + \(2 + 5\)
-   Maximum: 5 \(Still the largest value selected in the picklist. It is not the combined value in the index. To accomplish that, create a field and a rule in the set to add the multi-select picklist values together\)
-   Minimum: 0 \(The blank row applies to the minimum\)
-   Average: 3.75 = \[\(1 + 5\) + 2 + 0 + \(2 + 5\)\] / 4 \(The blank row counts towards the total and the divisor. The divisor is the number of indexes, not the number of picklist field options selected\)
-   Count: 3 \(The blank value does not apply to a count aggregate\)

Remember: The average, minimum, maximum and sum aggregates only work for picklist fields if the field option values are of number type. If the field option values are of text type, users will experience an error in runtime.

The following field is the field set up for the examples in this topic. Note that the Comparison Type is Number, and the values are numbers.

![Aggregates to the field](../images/cpq-sets-aggregates-28.png)

**Related topics**  


[Using sets in layouts](layouts-sets.md)

