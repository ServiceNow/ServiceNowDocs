---
title: CSVParser - Scoped
description: The CSVParser API provides methods for parsing comma-separated value \(CSV\) formatted records into an object or an array.Parses passed in CSV formatted content into an array.Parses passed in CSV formatted content into an object.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CSVParser- Scoped

The CSVParser API provides methods for parsing comma-separated value \(CSV\) formatted records into an object or an array.

This API runs in the `sn_impex` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CSVParser - parseLineToArray\(String cvsLine, String delimiter, String quoteCharacter\)

Parses passed in CSV formatted content into an array.

<table id="table_jn5_hkt_kjb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

csvLine

</td><td>

String

</td><td>

CSV content to parse.

</td></tr><tr><td>

delimiter

</td><td>

String

</td><td>

Optional. Character used to delineate the fields in the source CSV content.Default: Comma ','

</td></tr><tr><td>

quoteCharacter

</td><td>

String

</td><td>

Optional. Character used as the quote character in the source CSV content. Default: Double quote '"'

</td></tr></tbody>
</table><table id="table_kn5_hkt_kjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

Array containing the parsed values for each element in the passed-in CSV content.For example:

 ```
{
Joe,
Smith,
470 W Carmen, Chicago IL, 60640
}
```

</td></tr></tbody>
</table>This example shows simple CSV formatted content parsed into a returned array.

```
var csvLine = '\"Joe\",\"Smith\",\"1470 W Carmen, Chicago IL, 60640\"';
var delimiter = ',';
var quoteCharacter = '"';

var x = new sn_impex.CSVParser().parseLineToArray(csvLine, delimiter, quoteCharacter);

gs.log(x[0]);
gs.log(x[1]);
gs.log(x[2]);

```

Output:

```
Joe
Smith
1470 W Carmen, Chicago IL, 60640
```

## CSVParser - parseLineToObject\(String cvsLine, Array headers, String delimiter, String quoteCharacter\)

Parses passed in CSV formatted content into an object.

<table id="table_k54_fgt_kjb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

csvLine

</td><td>

String

</td><td>

CSV content to parse.

</td></tr><tr><td>

headers

</td><td>

Array of Strings

</td><td>

Headers associated with the CSV content. These headers must be specified in the same order as the corresponding content in **csvLine**. For example, `var headers = ['first_name', 'last_name', 'address'];`

</td></tr><tr><td>

delimiter

</td><td>

String

</td><td>

Optional. Character used to delineate the fields in the source CSV content.Default: Comma ','

</td></tr><tr><td>

quoteCharacter

</td><td>

String

</td><td>

Optional. Character used as the quote character in the source CSV content. Default: Double quote '"'

</td></tr></tbody>
</table><table id="table_l54_fgt_kjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing the header and corresponding value for each element in the passed-in CSV content.For example:

 ```
{
first_name: Joe,
last_name: Smith,
address: 1470 W Carmen, Chicago IL, 60640
}
```

</td></tr></tbody>
</table>This example shows CSV formatted content parsed into a returned object.

```
var csvLine = '\"Joe\",\"Smith\",\"1470 W Carmen, Chicago IL, 60640\"';
var headers = ['first_name', 'last_name', 'address'];
var delimiter = ',';
var quoteCharacter = '"';

var x = new sn_impex.CSVParser().parseLineToObject(csvLine, headers, delimiter, quoteCharacter);

gs.log(x.first_name);
gs.log(x.last_name);
gs.log(x.address);

```

Output:

```
Joe
Smith
1470 W Carmen, Chicago IL, 60640
```

This example shows an exception response because of an invalid pass of the header parameter.

```
var csvLine = '\"Joe\",\"Smith\",\"1470 W Carmen, Chicago IL, 60640\"';
var headers = null;
var delimiter = ',';
var quoteCharacter = '"';
try {
var x = new sn_impex.CSVParser().parseLineToObject(csvLine, headers, delimiter, quoteCharacter);

gs.log(x.first_name);
gs.log(x.last_name);
gs.log(x.address);
}
catch(ex) {
      gs.info(ex.message);
}

```

Output:

```
CSVParser: Header list is empty: no thrown error
*** Script: CSVParser: Header list is empty
```

