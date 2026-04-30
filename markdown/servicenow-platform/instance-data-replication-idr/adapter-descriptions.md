---
title: Adapter descriptions for Instance Data Replication
description: Adapters modify the producer data before inserting the data on consumer instances in Instance Data Replication \(IDR\).
locale: en-US
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Reference, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Adapter descriptions for Instance Data Replication

Adapters modify the producer data before inserting the data on consumer instances in Instance Data Replication \(IDR\).

## Adapter fields

Each adapter has **Name** and **Description** fields. The name appears in the Adapter column. Use the **Description** field to explain the purpose of the data conversion.

## Calculation adapter

Use the calculation adapter on the producer data to specify the operation and the value that is used in the operation.

<table id="table_hcx_ytp_qfb"><thead><tr><th>

Parameter and value

</th><th>

Source data

</th><th>

Adapter output

</th></tr></thead><tbody><tr><td>

**Operation**: Multiply**Constant Value**: 1.08

</td><td>

10

</td><td>

10.80

</td></tr><tr><td>

**Operation**: Max**Constant Value**: 1000

</td><td>

1020

</td><td>

1000

</td></tr><tr><td>

**Operation**: Floor**Constant Value**: 0

</td><td>

5.5

</td><td>

5

</td></tr></tbody>
</table>**Max** specifies the highest and **Min** specifies the lowest possible values. Values above or below those limits are set to those limits. Value types such as **int** and **long** have maximum and minimum values. Values above or below those limits cause precision errors.

## Concatenate String adapter

Use the concatenate string adapter to append a specified string to the source data.

|Parameter and value|Source data|Adapter output|
|-------------------|-----------|--------------|
|**String**: \_v2|Patch10236|Patch10236\_v2|

## Fixed-width format adapter

Use the fixed-width format adapter to reformat fixed-width input data. Use `#` to represent any positive integer, `@` to represent any character, and `\` as the literal escape character.

<table id="table_vhj_yvp_qfb"><thead><tr><th>

Parameter and value

</th><th>

Source data

</th><th>

Adapter output

</th></tr></thead><tbody><tr><td>

**Match**: \#\#\#\#\#\#\#\#\#\#**Output**: \(\#\#\#\) \#\#\#-\#\#\#\#

</td><td>

7605551212

</td><td>

\(760\) 555-1212

</td></tr><tr><td>

**Match**: \#\#\#\#\#**Output**: \#\#\#.\#\#

</td><td>

10000

</td><td>

100.00

</td></tr><tr><td>

**Match**: \#\#\\,\#\#\#**Output**: \#\#\#\#\#

</td><td>

10,000

</td><td>

10000

</td></tr></tbody>
</table>## Map adapter

Use the map adapter for comma-separated pairs of literals to map source-to-target conversions. Matches must be exact. For example, PRB=TASK would not convert PRB1000 to TASK1000.

|Parameter and value|Source data|Adapter output|
|-------------------|-----------|--------------|
|**Map**: PRB=TASK, done=complete|PRB|TASK|
|**Map**: PRB=TASK, done=complete|done|complete|
|**Map**: PRB=TASK, done=complete|PRB1000|\(no mapping\)|

## Pattern adapter

Use the pattern adapter for regular expressions to identify input patterns. Use parentheses in the **Regex** to identify groups. In **Output Pattern**, use `$` to specify groups. `$0` represents the entire input, `$1` represents the first group, `$2` represents the second group, and so on. You can also insert, prefix, and append literal characters, including spaces so they appear in the adapter output.

<table id="table_h5n_dxp_qfb"><thead><tr><th>

Parameter and value

</th><th>

Source data

</th><th>

Adapter output

</th></tr></thead><tbody><tr><td>

**Regex**: \(.\*\),\(.\*\)

 **Output pattern**: $2 $1

</td><td>

Smith, John

</td><td>

John Smith

</td></tr><tr><td>

**Regex**: \(ABC\[a-zA-z\]\[a-zA-z\]\)\(ABC\[a-zA-z\]\[a-zA-z\]\)

 **Output pattern**: $1 $0

</td><td>

ABCDEABCFG

</td><td>

ABCDE ABCDEABCFG

</td></tr><tr><td>

**Regex**: \(ABC\[a-zA-z\]\[a-zA-z\]\)\(ABC\[a-zA-z\]\[a-zA-z\]\)

 **Output pattern**: $1 release $0

</td><td>

ABCDEABCFG

</td><td>

ABCDE release ABCDEABCFG

</td></tr></tbody>
</table>In the second example, the match is ABC followed by two letters, followed by `ABC` and two letters. `$1` of this input is `ABCDE`. `$2` of this input is `ABCFG`. `$0` is the entire input string. So `$1 $0` is `ABCDE ABCDEABCFG`.

## Replace adapter

Use the replace adapter to replace a specified input string or substring with a specified string. Use `$` to replace only some of the occurrences of the string. `$1` replaces only the first occurrence; `$2` replaces only the second. Use curly braces to replace the first N occurrences. For example, `${3}` replaces the first three occurrences.

<table id="table_ghm_nyp_qfb"><thead><tr><th>

Parameter and value

</th><th>

Source data

</th><th>

Adapter output

</th></tr></thead><tbody><tr><td>

**Find**: London

 **Replace**: Madrid

</td><td>

The product is London. The product is London. The product is London.

</td><td>

The product is Madrid. The product is Madrid. The product is Madrid.

</td></tr><tr><td>

**Find**: $2 London

 **Replace**: Madrid

</td><td>

The product is London. The product is London. The product is London.

</td><td>

The product is London. The product is Madrid. The product is London.

</td></tr><tr><td>

**Find**: $\{2\} London

 **Replace**: Madrid

</td><td>

The product is London. The product is London. The product is London.

</td><td>

The product is Madrid. The product is Madrid. The product is London.

</td></tr></tbody>
</table>## Split adapter

Use the split adapter to break a string into two or more strings using a specified delimiter made up of letters, numbers, or special characters \(no spaces\). In **Output Pattern**, use `$` to specify groups. `$0` represents the entire input, `$1` represents the first group, `$2` represents the second group, and so on. You can repeat a group in an output pattern, for example, `$2, $1, $1`. Multiple instances of a delimiter in source data create three or more groups.

<table id="table_hxv_jkq_qfb"><thead><tr><th>

Parameter and value

</th><th>

Source data

</th><th>

Adapter output

</th></tr></thead><tbody><tr><td>

**Delimiter**: -

 **Output Pattern**: $2, $1

</td><td>

John-Smith

</td><td>

Smith, John

</td></tr><tr><td>

**Delimiter**: -

 **Output Pattern**: $2, $1, $1

</td><td>

John-Harry-Smith

</td><td>

Harry, John, John

</td></tr><tr><td>

**Delimiter**: -

 **Output Pattern**: $3

</td><td>

John-Harry-Smith

</td><td>

Smith

</td></tr></tbody>
</table>## Task number adapter

Use the task number adapter to add a prefix or suffix to a task number or replace the task number's prefix.

<table id="table_mx4_xs1_sfb"><thead><tr><th>

Parameter and value

</th><th>

Source data

</th><th>

Adapter output

</th></tr></thead><tbody><tr><td>

**Modification**: Replace

 **Number Prefix**: PRB

 **New Number Prefix**: STRY

</td><td>

PRB80899

</td><td>

STRY80899

</td></tr><tr><td>

**Modification**: Add Prefix

 **Prefix**: STRY

</td><td>

08099

</td><td>

STRY80899

</td></tr></tbody>
</table>## Time zone conversion adapter

Use the time zone conversion adapter to convert one time zone to another.

|Parameter and value|Source data|Adapter output|
|-------------------|-----------|--------------|
|**Output time zone**: PDT|07:00:00 am GMT|00:00:00 am PDT|

**Parent Topic:**[Instance Data Replication reference](../concept/reference-instance-data-replication.md)

**Related topics**  


[Data privacy in Instance Data Replication](../concept/data-privacy-consumers-idr.md)

[Excluded tables in Instance Data Replication](IDR-excluded-tables.md)

[Domain separation and IDR](instance-data-replication-domain-separation.md)

[Instance Data Replication system properties](instance-data-replication-properties.md)

[Instance Data Replication roles](instance-data-replication-roles.md#)

