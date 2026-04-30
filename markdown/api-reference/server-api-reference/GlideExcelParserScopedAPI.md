---
title: GlideExcelParser - Scoped, Global
description: The GlideExcelParser API parses .xlsx formatted Excel files and access file data in scripts.Creates an instance of GlideExcelParser.Close the connection to the input stream and release the document.Returns a list of column headers from the parsed document.Returns the error message when the parse\(\) method fails.Get the current row values and headers.Gets a list of all worksheet names in an Excel workbook.Gets table column types and max character length from a spreadsheet or CSV attachment.Moves to the next row.Parses an XLSX-formatted Excel document.Set the number of the header row to be retrieved.Return an empty value instead of null when an Excel cell is not present.Set the name of the sheet to be retrieved.Set the number of the Excel sheet to be retrieved.Defines an input source for parsing multiple times or parsing each worksheet in an Excel file.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 19
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideExcelParser - Scoped, Global

The GlideExcelParser API parses .xlsx formatted Excel files and access file data in scripts.

You can use the GlideExcelParser methods in global and scoped scripts. Use the `sn_impex` namespace identifier to create a GlideExcelParser object.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideExcelParser - GlideExcelParser\(\)

Creates an instance of GlideExcelParser.

The API name space identifier "sn\_impex" must be used when creating a GlideExcelParser object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var parser = new sn_impex.GlideExcelParser(); 
var attachment = new GlideSysAttachment();
// use attachment sys id of an excel file
var attachmentStream = attachment.getContentStream(<attachment sys id>);

parser.parse(attachmentStream); 

//retrieve the column headers
var headers = parser.getColumnHeaders();  
var header1 = headers[0]; 
var header2 = headers[1]; 

//print headers
gs.info(header1 + " " + header2); 

while(parser.next()) { 
  var row = parser.getRow(); 
  //print row value for both columns   
  gs.info(row[header1] + ' ' + row[header2]) 
}
```

## GlideExcelParser - close\(\)

Close the connection to the input stream and release the document.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example shows how to close the parser once all document management is complete.

```
// iterate over each row in the excel sheet
var attachment = new GlideSysAttachment();
var attachmentStream = attachment.getContentStream(<attachment sys id>);
var parser = new sn_impex.GlideExcelParser();
parser.parse(attachmentStream);
while (parser.next()) {
  // do something on each row
  var row = parser.getRow();
  gs.info(JSON.stringify(row));
}
parser.close(); // close the stream and release the document
```

## GlideExcelParser - getColumnHeaders\(\)

Returns a list of column headers from the parsed document.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|An array of strings of column headers from the parsed document.|

The following example shows how to parse an Excel file attachment multiple times to retrieve column headers and print values of each row for each worksheet. Results display column headers and values of three separate sheets in the Excel attachment.

```
var parser = new sn_impex.GlideExcelParser();

var attachment = new GlideSysAttachment();

// Use the attachment sys_id of an Excel file
var attachmentStream = attachment.getContentStream("<attachment_sys_id>");

// Set the source to be parsed
parser.setSource(attachmentStream);

// Get the worksheet names to be parsed in the Excel document
var list_sheet_name = parser.getSheetNames();

gs.info(" Sheet Names " + list_sheet_name.join(", "));

// Iterate over each worksheet in the Excel workbook
for (var i = 0; i < list_sheet_name.length; i++) {
    gs.info("**************************************************************************************");
    gs.info("Sheet name:    " + list_sheet_name[i]);

// Set the worksheet name to be parsed
    parser.setSheetName(list_sheet_name[i]);

// Parse each worksheet set using setSheetName()
    if (parser.parse()) {
        //retrieve the column headers
        var headers = parser.getColumnHeaders();
        var header1 = headers[0];
        var header2 = headers[1];
        var header3 = headers[2];

        //print headers
        gs.info(header1 + "\t||" + header2 + "\t||" + header3);

        // Iterate over each row in the worksheet
        while (parser.next()) {
            var row = parser.getRow();
            //print row value for both columns   
            gs.info(row[header1] + '\t|| ' + row[header2] + '\t||' + row[header3])
        }
    } else
        gs.info(parser.getErrorMessage());
}
```

Output:

```
*** Script:  Sheet Names Incident Table, sys_user Table, knowledge Table
*** Script: **************************************************************************************
*** Script: Sheet name:    Incident Table
*** Script: Number	||Opened	||Short description
*** Script: INC0010112	|| 2019-07-29 11:48:43	||Assessment :  ATF Assessor
*** Script: INC0010111	|| 2019-07-22 14:04:57	||ATF : Test1
*** Script: INC0009009	|| 2018-08-30 01:06:16	||Unable to access the shared folder.
*** Script: **************************************************************************************
*** Script: Sheet name:    sys_user Table
*** Script: User ID	||Name	||Email
*** Script: abel.tuter	|| Abel Tuter	||abel.tuter@example.com
*** Script: abraham.lincoln	|| Abraham Lincoln	||abraham.lincoln@example.com
*** Script: adela.cervantsz	|| Adela Cervantsz	||adela.cervantsz@example.com
*** Script: aileen.mottern	|| Aileen Mottern	||aileen.mottern@example.com
*** Script: alejandra.prenatt	|| Alejandra Prenatt	||alejandra.prenatt@example.com
*** Script: **************************************************************************************
*** Script: Sheet name:    knowledge Table
*** Script: Number	||Short description	||Author
*** Script: KB99999999	|| Microsoft Outlook Issues	||System Administrator
*** Script: KB0000033	|| Eclipse configuration for Android development	||System Administrator
*** Script: KB0000032	|| Getting Around in Windows	||System Administrator
*** Script: KB0000031	|| How can I find the MAC address of my Ethernet or
   wireless interface?	||Sam Sorokin
```

## GlideExcelParser - getErrorMessage\(\)

Returns the error message when the parse\(\) method fails.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The error message.|

## GlideExcelParser - getRow\(\)

Get the current row values and headers.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|The row headers are property names and the row values are property values.|

The following example shows how to parse an Excel file attachment multiple times to retrieve column headers and print values of each row for each worksheet. Results display column headers and values of three separate sheets in the Excel attachment.

```
var parser = new sn_impex.GlideExcelParser();

var attachment = new GlideSysAttachment();

// Use the attachment sys_id of an Excel file
var attachmentStream = attachment.getContentStream("<attachment_sys_id>");

// Set the source to be parsed
parser.setSource(attachmentStream);

// Get the worksheet names to be parsed in the Excel document
var list_sheet_name = parser.getSheetNames();

gs.info(" Sheet Names " + list_sheet_name.join(", "));

// Iterate over each worksheet in the Excel workbook
for (var i = 0; i < list_sheet_name.length; i++) {
    gs.info("**************************************************************************************");
    gs.info("Sheet name:    " + list_sheet_name[i]);

// Set the worksheet name to be parsed
    parser.setSheetName(list_sheet_name[i]);

// Parse each worksheet set using setSheetName()
    if (parser.parse()) {
        //retrieve the column headers
        var headers = parser.getColumnHeaders();
        var header1 = headers[0];
        var header2 = headers[1];
        var header3 = headers[2];

        //print headers
        gs.info(header1 + "\t||" + header2 + "\t||" + header3);

        // Iterate over each row in the worksheet
        while (parser.next()) {
            var row = parser.getRow();
            //print row value for both columns   
            gs.info(row[header1] + '\t|| ' + row[header2] + '\t||' + row[header3])
        }
    } else
        gs.info(parser.getErrorMessage());
}
```

Output:

```
*** Script:  Sheet Names Incident Table, sys_user Table, knowledge Table
*** Script: **************************************************************************************
*** Script: Sheet name:    Incident Table
*** Script: Number	||Opened	||Short description
*** Script: INC0010112	|| 2019-07-29 11:48:43	||Assessment :  ATF Assessor
*** Script: INC0010111	|| 2019-07-22 14:04:57	||ATF : Test1
*** Script: INC0009009	|| 2018-08-30 01:06:16	||Unable to access the shared folder.
*** Script: **************************************************************************************
*** Script: Sheet name:    sys_user Table
*** Script: User ID	||Name	||Email
*** Script: abel.tuter	|| Abel Tuter	||abel.tuter@example.com
*** Script: abraham.lincoln	|| Abraham Lincoln	||abraham.lincoln@example.com
*** Script: adela.cervantsz	|| Adela Cervantsz	||adela.cervantsz@example.com
*** Script: aileen.mottern	|| Aileen Mottern	||aileen.mottern@example.com
*** Script: alejandra.prenatt	|| Alejandra Prenatt	||alejandra.prenatt@example.com
*** Script: **************************************************************************************
*** Script: Sheet name:    knowledge Table
*** Script: Number	||Short description	||Author
*** Script: KB99999999	|| Microsoft Outlook Issues	||System Administrator
*** Script: KB0000033	|| Eclipse configuration for Android development	||System Administrator
*** Script: KB0000032	|| Getting Around in Windows	||System Administrator
*** Script: KB0000031	|| How can I find the MAC address of my Ethernet or
   wireless interface?	||Sam Sorokin
```

## GlideExcelParser - getSheetNames\(\)

Gets a list of all worksheet names in an Excel workbook.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|Array of strings as worksheet names ordered as positioned from left to right in the workbook. Results include any worksheets marked as hidden.|

The following example shows how to parse an Excel file attachment multiple times to retrieve column headers and print values of each row for each worksheet. Results display column headers and values of three separate sheets in the Excel attachment.

```
var parser = new sn_impex.GlideExcelParser();

var attachment = new GlideSysAttachment();

// Use the attachment sys_id of an Excel file
var attachmentStream = attachment.getContentStream("<attachment_sys_id>");

// Set the source to be parsed
parser.setSource(attachmentStream);

// Get the worksheet names to be parsed in the Excel document
var list_sheet_name = parser.getSheetNames();

gs.info(" Sheet Names " + list_sheet_name.join(", "));

// Iterate over each worksheet in the Excel workbook
for (var i = 0; i < list_sheet_name.length; i++) {
    gs.info("**************************************************************************************");
    gs.info("Sheet name:    " + list_sheet_name[i]);

// Set the worksheet name to be parsed
    parser.setSheetName(list_sheet_name[i]);

// Parse each worksheet set using setSheetName()
    if (parser.parse()) {
        //retrieve the column headers
        var headers = parser.getColumnHeaders();
        var header1 = headers[0];
        var header2 = headers[1];
        var header3 = headers[2];

        //print headers
        gs.info(header1 + "\t||" + header2 + "\t||" + header3);

        // Iterate over each row in the worksheet
        while (parser.next()) {
            var row = parser.getRow();
            //print row value for both columns   
            gs.info(row[header1] + '\t|| ' + row[header2] + '\t||' + row[header3])
        }
    } else
        gs.info(parser.getErrorMessage());
}
```

Output:

```
*** Script:  Sheet Names Incident Table, sys_user Table, knowledge Table
*** Script: **************************************************************************************
*** Script: Sheet name:    Incident Table
*** Script: Number	||Opened	||Short description
*** Script: INC0010112	|| 2019-07-29 11:48:43	||Assessment :  ATF Assessor
*** Script: INC0010111	|| 2019-07-22 14:04:57	||ATF : Test1
*** Script: INC0009009	|| 2018-08-30 01:06:16	||Unable to access the shared folder.
*** Script: **************************************************************************************
*** Script: Sheet name:    sys_user Table
*** Script: User ID	||Name	||Email
*** Script: abel.tuter	|| Abel Tuter	||abel.tuter@example.com
*** Script: abraham.lincoln	|| Abraham Lincoln	||abraham.lincoln@example.com
*** Script: adela.cervantsz	|| Adela Cervantsz	||adela.cervantsz@example.com
*** Script: aileen.mottern	|| Aileen Mottern	||aileen.mottern@example.com
*** Script: alejandra.prenatt	|| Alejandra Prenatt	||alejandra.prenatt@example.com
*** Script: **************************************************************************************
*** Script: Sheet name:    knowledge Table
*** Script: Number	||Short description	||Author
*** Script: KB99999999	|| Microsoft Outlook Issues	||System Administrator
*** Script: KB0000033	|| Eclipse configuration for Android development	||System Administrator
*** Script: KB0000032	|| Getting Around in Windows	||System Administrator
*** Script: KB0000031	|| How can I find the MAC address of my Ethernet or
   wireless interface?	||Sam Sorokin
```

## GlideExcelParser - getTableInfo\(\)

Gets table column types and max character length from a spreadsheet or CSV attachment.

**Note:** This method is restricted to scoped applications.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Returns attachment data as a map in which the key is column name. Values contain column type and maximum length of a character string in the column. Access return values using the getType\(\) and getLength\(\) methods.|

This example shows how to data from a 7-column spreadsheet attachment including row data such as 1, Meghan, 1/1/85, 1:00 AM, 10.00%, 224-432-8582, ½.

```
var attachmentSysId = "<sys_id>";
var headerRowNumber = 6;

var attachmentStream = new GlideSysAttachment().getContentStream(attachmentSysId);
var parser = new sn_impex.GlideExcelParser();
parser.setHeaderRowNumber(headerRowNumber);
if (!parser.parse(attachmentStream)) {
    throw "Attachment could not be parsed as an Excel Spreadsheet " + attachmentSysId;
}
var tableInfo = parser.getTableInfo();
for (var name in tableInfo) {
gs.info('Column Name : ' + name + ', Type : ' + tableInfo[name].getType() + ', Max Length : ' + tableInfo[name].getLength());
}
```

Output:

```
ProgressWorker: Attempted to get non-existent sys_progress_
worker record, inserted 81b0ca5ddb59730090c9ff9dbf9619c4
sn_appcreator: Column Name : My Number Col, Type : integer,
 Max Length : 1
sn_appcreator: Column Name : My String Col, Type : string, 
 Max Length : 650
sn_appcreator: Column Name : My Date Col, Type : glide_date,
 Max Length : 6
sn_appcreator: Column Name : My DateTime Col, Type : 
 glide_date_time, Max Length : 7
sn_appcreator: Column Name : My Percent Col, Type : decimal,
 Max Length : 6
sn_appcreator: Column Name : My Phone Col, Type : string, 
 Max Length : 12
sn_appcreator: Column Name : My Fraction Col, Type : decimal,
 Max Length : 3
```

## GlideExcelParser - next\(\)

Moves to the next row.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true if there is a next row, otherwise, returns false.|

The following example shows how to parse an Excel file attachment multiple times to retrieve column headers and print values of each row for each worksheet. Results display column headers and values of three separate sheets in the Excel attachment.

```
var parser = new sn_impex.GlideExcelParser();

var attachment = new GlideSysAttachment();

// Use the attachment sys_id of an Excel file
var attachmentStream = attachment.getContentStream("<attachment_sys_id>");

// Set the source to be parsed
parser.setSource(attachmentStream);

// Get the worksheet names to be parsed in the Excel document
var list_sheet_name = parser.getSheetNames();

gs.info(" Sheet Names " + list_sheet_name.join(", "));

// Iterate over each worksheet in the Excel workbook
for (var i = 0; i < list_sheet_name.length; i++) {
    gs.info("**************************************************************************************");
    gs.info("Sheet name:    " + list_sheet_name[i]);

// Set the worksheet name to be parsed
    parser.setSheetName(list_sheet_name[i]);

// Parse each worksheet set using setSheetName()
    if (parser.parse()) {
        //retrieve the column headers
        var headers = parser.getColumnHeaders();
        var header1 = headers[0];
        var header2 = headers[1];
        var header3 = headers[2];

        //print headers
        gs.info(header1 + "\t||" + header2 + "\t||" + header3);

        // Iterate over each row in the worksheet
        while (parser.next()) {
            var row = parser.getRow();
            //print row value for both columns   
            gs.info(row[header1] + '\t|| ' + row[header2] + '\t||' + row[header3])
        }
    } else
        gs.info(parser.getErrorMessage());
}
```

Output:

```
*** Script:  Sheet Names Incident Table, sys_user Table, knowledge Table
*** Script: **************************************************************************************
*** Script: Sheet name:    Incident Table
*** Script: Number	||Opened	||Short description
*** Script: INC0010112	|| 2019-07-29 11:48:43	||Assessment :  ATF Assessor
*** Script: INC0010111	|| 2019-07-22 14:04:57	||ATF : Test1
*** Script: INC0009009	|| 2018-08-30 01:06:16	||Unable to access the shared folder.
*** Script: **************************************************************************************
*** Script: Sheet name:    sys_user Table
*** Script: User ID	||Name	||Email
*** Script: abel.tuter	|| Abel Tuter	||abel.tuter@example.com
*** Script: abraham.lincoln	|| Abraham Lincoln	||abraham.lincoln@example.com
*** Script: adela.cervantsz	|| Adela Cervantsz	||adela.cervantsz@example.com
*** Script: aileen.mottern	|| Aileen Mottern	||aileen.mottern@example.com
*** Script: alejandra.prenatt	|| Alejandra Prenatt	||alejandra.prenatt@example.com
*** Script: **************************************************************************************
*** Script: Sheet name:    knowledge Table
*** Script: Number	||Short description	||Author
*** Script: KB99999999	|| Microsoft Outlook Issues	||System Administrator
*** Script: KB0000033	|| Eclipse configuration for Android development	||System Administrator
*** Script: KB0000032	|| Getting Around in Windows	||System Administrator
*** Script: KB0000031	|| How can I find the MAC address of my Ethernet or
   wireless interface?	||Sam Sorokin
```

## GlideExcelParser - parse\(InputStream inputStream\)

Parses an XLSX-formatted Excel document.

<table id="table_u2j_lch_4z" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

inputStream

</td><td>

[GlideScriptableInputStream](../../GlideScriptableInputStreamScoped/concept/c_GlideScriptableInpStrmScopedAPI.md)

</td><td>

Excel document provided as an input stream. **Note:** Do not set this value if using the [setSource\(\)](GlideExcelParserScopedAPI.md#) method to parse the same source multiple times.

</td></tr></tbody>
</table><table id="table_v2j_lch_4z" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates if the parse was successful.Valid values:

-   true: Document was successful parsed.
-   false: Document was not successfully parsed.

</td></tr></tbody>
</table>Example from a scripted REST API script where the Excel file is sent using an input stream in the request payload.

```
var parser = new sn_impex.GlideExcelParser();
parser.parse(request.body.dataStream); 
```

The following example shows how to parse an Excel file attachment multiple times to retrieve column headers and print values of each row for each worksheet. Results display column headers and values of three separate sheets in the Excel attachment.

```
var parser = new sn_impex.GlideExcelParser();

var attachment = new GlideSysAttachment();

// Use the attachment sys_id of an Excel file
var attachmentStream = attachment.getContentStream("<attachment_sys_id>");

// Set the source to be parsed
parser.setSource(attachmentStream);

// Get the worksheet names to be parsed in the Excel document
var list_sheet_name = parser.getSheetNames();

gs.info(" Sheet Names " + list_sheet_name.join(", "));

// Iterate over each worksheet in the Excel workbook
for (var i = 0; i < list_sheet_name.length; i++) {
    gs.info("**************************************************************************************");
    gs.info("Sheet name:    " + list_sheet_name[i]);

// Set the worksheet name to be parsed
    parser.setSheetName(list_sheet_name[i]);

// Parse each worksheet set using setSheetName()
    if (parser.parse()) {
        //retrieve the column headers
        var headers = parser.getColumnHeaders();
        var header1 = headers[0];
        var header2 = headers[1];
        var header3 = headers[2];

        //print headers
        gs.info(header1 + "\t||" + header2 + "\t||" + header3);

        // Iterate over each row in the worksheet
        while (parser.next()) {
            var row = parser.getRow();
            //print row value for both columns   
            gs.info(row[header1] + '\t|| ' + row[header2] + '\t||' + row[header3])
        }
    } else
        gs.info(parser.getErrorMessage());
}
```

Output:

```
*** Script:  Sheet Names Incident Table, sys_user Table, knowledge Table
*** Script: **************************************************************************************
*** Script: Sheet name:    Incident Table
*** Script: Number	||Opened	||Short description
*** Script: INC0010112	|| 2019-07-29 11:48:43	||Assessment :  ATF Assessor
*** Script: INC0010111	|| 2019-07-22 14:04:57	||ATF : Test1
*** Script: INC0009009	|| 2018-08-30 01:06:16	||Unable to access the shared folder.
*** Script: **************************************************************************************
*** Script: Sheet name:    sys_user Table
*** Script: User ID	||Name	||Email
*** Script: abel.tuter	|| Abel Tuter	||abel.tuter@example.com
*** Script: abraham.lincoln	|| Abraham Lincoln	||abraham.lincoln@example.com
*** Script: adela.cervantsz	|| Adela Cervantsz	||adela.cervantsz@example.com
*** Script: aileen.mottern	|| Aileen Mottern	||aileen.mottern@example.com
*** Script: alejandra.prenatt	|| Alejandra Prenatt	||alejandra.prenatt@example.com
*** Script: **************************************************************************************
*** Script: Sheet name:    knowledge Table
*** Script: Number	||Short description	||Author
*** Script: KB99999999	|| Microsoft Outlook Issues	||System Administrator
*** Script: KB0000033	|| Eclipse configuration for Android development	||System Administrator
*** Script: KB0000032	|| Getting Around in Windows	||System Administrator
*** Script: KB0000031	|| How can I find the MAC address of my Ethernet or
   wireless interface?	||Sam Sorokin
```

## GlideExcelParser - setHeaderRowNumber\(Number headerRowNumber\)

Set the number of the header row to be retrieved.

|Name|Type|Description|
|----|----|-----------|
|headerRowNumber|Number|The header row to be retrieved.|

|Type|Description|
|----|-----------|
|void| |

## GlideExcelParser - setNullToEmpty\(Boolean empty\)

Return an empty value instead of null when an Excel cell is not present.

|Name|Type|Description|
|----|----|-----------|
|empty|Boolean|When true, cells that are not present return an empty value. When false, cells that are not present return null.|

|Type|Description|
|----|-----------|
|void| |

## GlideExcelParser - setSheetName\(String sheetName\)

Set the name of the sheet to be retrieved.

If both setSheetNumber\(\) and setSheetName\(\) are set, setSheetName\(\) is used.

|Name|Type|Description|
|----|----|-----------|
|sheetName|String|The name of the sheet to be retrieved.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to parse an Excel file attachment multiple times to retrieve column headers and print values of each row for each worksheet. Results display column headers and values of three separate sheets in the Excel attachment.

```
var parser = new sn_impex.GlideExcelParser();

var attachment = new GlideSysAttachment();

// Use the attachment sys_id of an Excel file
var attachmentStream = attachment.getContentStream("<attachment_sys_id>");

// Set the source to be parsed
parser.setSource(attachmentStream);

// Get the worksheet names to be parsed in the Excel document
var list_sheet_name = parser.getSheetNames();

gs.info(" Sheet Names " + list_sheet_name.join(", "));

// Iterate over each worksheet in the Excel workbook
for (var i = 0; i < list_sheet_name.length; i++) {
    gs.info("**************************************************************************************");
    gs.info("Sheet name:    " + list_sheet_name[i]);

// Set the worksheet name to be parsed
    parser.setSheetName(list_sheet_name[i]);

// Parse each worksheet set using setSheetName()
    if (parser.parse()) {
        //retrieve the column headers
        var headers = parser.getColumnHeaders();
        var header1 = headers[0];
        var header2 = headers[1];
        var header3 = headers[2];

        //print headers
        gs.info(header1 + "\t||" + header2 + "\t||" + header3);

        // Iterate over each row in the worksheet
        while (parser.next()) {
            var row = parser.getRow();
            //print row value for both columns   
            gs.info(row[header1] + '\t|| ' + row[header2] + '\t||' + row[header3])
        }
    } else
        gs.info(parser.getErrorMessage());
}
```

Output:

```
*** Script:  Sheet Names Incident Table, sys_user Table, knowledge Table
*** Script: **************************************************************************************
*** Script: Sheet name:    Incident Table
*** Script: Number	||Opened	||Short description
*** Script: INC0010112	|| 2019-07-29 11:48:43	||Assessment :  ATF Assessor
*** Script: INC0010111	|| 2019-07-22 14:04:57	||ATF : Test1
*** Script: INC0009009	|| 2018-08-30 01:06:16	||Unable to access the shared folder.
*** Script: **************************************************************************************
*** Script: Sheet name:    sys_user Table
*** Script: User ID	||Name	||Email
*** Script: abel.tuter	|| Abel Tuter	||abel.tuter@example.com
*** Script: abraham.lincoln	|| Abraham Lincoln	||abraham.lincoln@example.com
*** Script: adela.cervantsz	|| Adela Cervantsz	||adela.cervantsz@example.com
*** Script: aileen.mottern	|| Aileen Mottern	||aileen.mottern@example.com
*** Script: alejandra.prenatt	|| Alejandra Prenatt	||alejandra.prenatt@example.com
*** Script: **************************************************************************************
*** Script: Sheet name:    knowledge Table
*** Script: Number	||Short description	||Author
*** Script: KB99999999	|| Microsoft Outlook Issues	||System Administrator
*** Script: KB0000033	|| Eclipse configuration for Android development	||System Administrator
*** Script: KB0000032	|| Getting Around in Windows	||System Administrator
*** Script: KB0000031	|| How can I find the MAC address of my Ethernet or
   wireless interface?	||Sam Sorokin
```

## GlideExcelParser - setSheetNumber\(Number sheetNumber\)

Set the number of the Excel sheet to be retrieved.

If both setSheetNumber\(\) and setSheetName\(\) are set, setSheetNumber\(\) is ignored.

|Name|Type|Description|
|----|----|-----------|
|sheetNumber|Number|The Excel sheet number to retrieve.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to use this method to specify the sheet number of an attached spreadsheet workbook to be read.

```
var parser = new sn_impex.GlideExcelParser(); 
var attachment = new GlideSysAttachment();

// Use the sys id of an Excel file in the sys_attachment table and copy the sys_id of attachment.
var attachmentStream = attachment.getContentStream('178e0511138b6300026e32228144b04e');

// Specify the sheet Number to be read, 0 denotes sheet 1, 1 denotes sheet 2, etc.
parser.setSheetNumber("0");   

parser.parse(attachmentStream);

// retrieve the column headers (tests if on the correct sheet)
var headers = parser.getColumnHeaders();
var header1 = headers[0];
var header2 = headers[1];
var header3 = headers[2];

// print headers
gs.info('Header 1 value = ' +header1);
gs.info('Header 2 value = ' +header2);
gs.info('Header 3 value = ' +header3);
```

Output:

```
Header 1 value = sys_id
Header 2 value = email
Header 3 value = undefined
```

## GlideExcelParser - setSource\(InputStream inputStream\)

Defines an input source for parsing multiple times or parsing each worksheet in an Excel file.

|Name|Type|Description|
|----|----|-----------|
|inputStream|[GlideScriptableInputStream](../../GlideScriptableInputStreamScoped/concept/c_GlideScriptableInpStrmScopedAPI.md)|Excel document provided as an input stream.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to parse an Excel file attachment multiple times to retrieve column headers and print values of each row for each worksheet. Results display column headers and values of three separate sheets in the Excel attachment.

```
var parser = new sn_impex.GlideExcelParser();

var attachment = new GlideSysAttachment();

// Use the attachment sys_id of an Excel file
var attachmentStream = attachment.getContentStream("<attachment_sys_id>");

// Set the source to be parsed
parser.setSource(attachmentStream);

// Get the worksheet names to be parsed in the Excel document
var list_sheet_name = parser.getSheetNames();

gs.info(" Sheet Names " + list_sheet_name.join(", "));

// Iterate over each worksheet in the Excel workbook
for (var i = 0; i < list_sheet_name.length; i++) {
    gs.info("**************************************************************************************");
    gs.info("Sheet name:    " + list_sheet_name[i]);

// Set the worksheet name to be parsed
    parser.setSheetName(list_sheet_name[i]);

// Parse each worksheet set using setSheetName()
    if (parser.parse()) {
        //retrieve the column headers
        var headers = parser.getColumnHeaders();
        var header1 = headers[0];
        var header2 = headers[1];
        var header3 = headers[2];

        //print headers
        gs.info(header1 + "\t||" + header2 + "\t||" + header3);

        // Iterate over each row in the worksheet
        while (parser.next()) {
            var row = parser.getRow();
            //print row value for both columns   
            gs.info(row[header1] + '\t|| ' + row[header2] + '\t||' + row[header3])
        }
    } else
        gs.info(parser.getErrorMessage());
}
```

Output:

```
*** Script:  Sheet Names Incident Table, sys_user Table, knowledge Table
*** Script: **************************************************************************************
*** Script: Sheet name:    Incident Table
*** Script: Number	||Opened	||Short description
*** Script: INC0010112	|| 2019-07-29 11:48:43	||Assessment :  ATF Assessor
*** Script: INC0010111	|| 2019-07-22 14:04:57	||ATF : Test1
*** Script: INC0009009	|| 2018-08-30 01:06:16	||Unable to access the shared folder.
*** Script: **************************************************************************************
*** Script: Sheet name:    sys_user Table
*** Script: User ID	||Name	||Email
*** Script: abel.tuter	|| Abel Tuter	||abel.tuter@example.com
*** Script: abraham.lincoln	|| Abraham Lincoln	||abraham.lincoln@example.com
*** Script: adela.cervantsz	|| Adela Cervantsz	||adela.cervantsz@example.com
*** Script: aileen.mottern	|| Aileen Mottern	||aileen.mottern@example.com
*** Script: alejandra.prenatt	|| Alejandra Prenatt	||alejandra.prenatt@example.com
*** Script: **************************************************************************************
*** Script: Sheet name:    knowledge Table
*** Script: Number	||Short description	||Author
*** Script: KB99999999	|| Microsoft Outlook Issues	||System Administrator
*** Script: KB0000033	|| Eclipse configuration for Android development	||System Administrator
*** Script: KB0000032	|| Getting Around in Windows	||System Administrator
*** Script: KB0000031	|| How can I find the MAC address of my Ethernet or
   wireless interface?	||Sam Sorokin
```

