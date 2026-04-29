---
title: File type data sources
description: Import a file from a local source, a remote network server, or another instance by providing a path and authentication information.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Data sources, Import sets, Imports, Workflow Data Fabric]
---

# File type data sources

Import a file from a local source, a remote network server, or another instance by providing a path and authentication information.

For file type import sets, you can select from a list of file retrieval methods: SFTP, FTP, FTPS, HTTP, HTTPS, and SCP.

**Note:** FTPS is not recommended because it is no longer supported by some firewall vendors. Consider using SFTP as an alternative.

## File retrieval methods

The following file retrieval methods are available to copy the file from where it resides to ServiceNow to be loaded into an import set.

After defining the files that are compatible for importing, define how the files can be imported.

**Note:** For the import to succeed, your FTP server and client must be set up for the same authentication mechanism that you select here.

<table id="table_xxs_lsj_dq"><thead><tr><th>

Method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attachment

</td><td>

[Add and manage attachments](https://www.servicenow.com/docs/access?context=t_AddingAnAttachment&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) a file to the record and import that file in an import set.

</td></tr><tr><td>

SFTP

</td><td>

Retrieve a file using SFTP. Fields are provided for the server name and login credentials.

</td></tr><tr><td>

FTP

</td><td>

Retrieve a file from an FTP server in your network. Fields are provided for the server name and login credentials.**Note:** FTP transfers are sent as clear text and cannot be encrypted. Use SCP or SFTP instead whenever possible.

</td></tr><tr><td>

FTPS \(Auth SSL\) \[not recommended\]

</td><td>

Not recommended because FTPS is no longer supported by some firewall vendors. Consider using SFTP as an alternative.An FTP Secure authentication command issued through the Secure Socket Layer \(SSL\) protocol. This method is also known as explicit FTP over SSL.

</td></tr><tr><td>

FTPS \(Auth TLS\) \[not recommended\]

</td><td>

Not recommended because FTPS is no longer supported by some firewall vendors. Consider using SFTP as an alternative.An FTP Secure authentication command issued through the Transport Layer Security \(TLS\) protocol. This method is also known as explicit FTP over TLS.

</td></tr><tr><td>

FTPS \(Implicit SSL\) \[not recommended\]

</td><td>

Not recommended because FTPS is no longer supported by some firewall vendors. Consider using SFTP as an alternative.In implicit security, the FTPS server defines a specific port for the client \(990\) to use for secure connections. Implicit security automatically begins with an SSL connection the moment an FTPS client connects to an FTPS server.

</td></tr><tr><td>

FTPS \(Implicit TLS\) \[not recommended\]

</td><td>

Not recommended because FTPS is no longer supported by some firewall vendors. Consider using SFTP as an alternative.In implicit security, the FTPS server defines a specific port for the client \(990\) to use for secure connections. Implicit security automatically begins with a TLS connection the moment an FTP client connects to an FTP server.

</td></tr><tr><td>

HTTP

</td><td>

Retrieve a file using HTTP. Fields are provided for the server name and login credentials.**Important:** For HTTP and HTTPS protocols, the file path is automatically URL encoded. Do not specify a URL-encoded file path when using either of these protocols.

</td></tr><tr><td>

HTTPS

</td><td>

Retrieve a file using HTTPS. Fields are provided for the server name and login credentials. Use this method to transfer data between ServiceNow instances.

</td></tr><tr><td>

SCP

</td><td>

The Secure Copy protocol \(SCP\) securely transfers files between a local and a remote host or between two remote hosts, using the Secure Shell \(SSH\) protocol.

</td></tr></tbody>
</table>## File data source examples

These examples describe how to import various file types as data sources.

## Excel data source file

You can import using both the XLSX format and the legacy XLS format. XLS is the default format for spreadsheets created in Excel for versions 2003 and older. XLSX is the default format for Excel 2007 or later. Use XLSX instead of legacy XLS whenever possible for optimal performance.

**Note:**

-   All .xls files must use the 1900 date system as opposed to the 1904 date system. The 1904 date system causes your dates to be imported with a year that is four years earlier than what appears in your spreadsheet. Refer to MS Support for additional information about date systems.
-   When importing a file from Excel that has upper case boolean values of \(TRUE/FALSE\), both values always transform to false. To prevent this behavior, set the **glide.transform.boolean.casesensitive** property to false.

![Microsoft Excel demo data](../image/Xls_shot.png "Microsoft Excel Demo Data")

## XML data source file

-   **XPath for each row**

    XML data source definitions have an extra field to specify the **XPath for each row**. This field is an [XPath](http://www.zvon.org/xxl/XPathTutorial/General/examples.html) expression to select the elements whose children are converted to rows in the import set table. Each selected element causes a row to be created in the import set table. The children of the selected element are converted into columns in the row. For example, to import the asset information from the sample XML file below, the XPath expression should be specified as `/export/asset`. This expression matches the three `<asset>` elements in the file, so three rows are created. Although you could also specify `//asset`, this expression is much less efficient for large files. Use the absolute location path form for XPath expressions when using the XML loader. In other words, avoid expressions containing `//` unless strictly necessary.

    Be careful not to specify an insufficiently restrictive XPath expression with a large XML file. For example, the expression `/export` would be wrong for the following sample file, since it matches the document \(root\) element. In general, you should never specify an XPath expression which matches the root element unless you want everything in the document to be made into a single row. Specifying an insufficiently restrictive XPath expression when attempting to load large XML files could result in lengthy processing times and incorrect output. For this reason, it is best to test and debug XML data source specifications with small XML files containing only a few rows worth of data. Once the specification has been tested, you can run it again with the full file.

-   **&lt;userInfo&gt; elements**

    Note that the `<userInfo>` elements contained within `<asset>` contain child elements. This type of nesting creates a column called **userInfo** that contains XML for the `<userInfo>` element. If **Expand child nodes** is checked, individual columns are also created for **userInfo/lastName** and **userInfo/firstName**. If **Expand child nodes** is not checked, only the **userInfo** XML column is created.

-   **Loading data from an XML file**

    When loading data from an XML file, ServiceNow samples the first 10 records to determine what fields are required to hold the data. If none of the first 10 records specify a value for a field, ServiceNow does not add that field to the table that holds the imported data. Ensure that at least one of the first 10 records specifies a value for any fields being imported.

    If the XML file used for an XML data source does not contain a field in the first 10 nodes, the field is ignored. To import the field and ensure it is not ignored, you can add the **glide.db.impex.XMLLoader.max.scan\_nodes** system property with a value greater than or equal to the position of the node where the field is first encountered. This property applies to all XML data sources. **glide.db.impex.XMLLoader.max.scan\_nodes** defaults to **10**, but you can enter a value from **1** to **2147483647** to specify how many nodes should be scanned to determine the values to be used for the import. You can specify **-1** to scan all nodes in the XML files.

    **Important:** If you specify **-1** or increase the value of **glide.db.impex.XMLLoader.max.scan\_nodes** beyond the default of **10**, all XML import processing may incur a significant increase in overall load time.


```
<?xml version= "1.0" encoding= "utf-8" ?><export><asset><assetTag>AT-01939</assetTag><type>Desktop</type><os>Windows 7 Professional</os><lastlogondate>12-07-2010 12:31:24</lastlogondate><userInfo><lastName>Loo</lastName><firstName>David</firstName></userInfo><isenabled>true</isenabled></asset><asset><assetTag>AT-53480</assetTag><type>Desktop</type><os>Windows 7 Professional</os><lastlogondate>09-07-2010 13:25:53</lastlogondate><userInfo><lastName>Merritt</lastName><firstName>Norris</firstName></userInfo><isenabled>true</isenabled></asset><asset><assetTag>AT-55782</assetTag><type>Desktop</type><os>Unknown</os><lastlogondate>01-01-1900 00:00:00</lastlogondate><userInfo><lastName>Currie</lastName><firstName>Mike</firstName></userInfo><isenabled>true</isenabled></asset></export>
```

## CSV data source file

CSV files are used as a cross-compatible file format for transferring files across platforms. A CSV file is a text file that defines a grid, where commas define columns and line breaks define rows. To define precise spacing for importing strings, you can optionally wrap text in quotes.

```
"user_name","name","email","sys_created_on","active"
"jared.laethem","Jared Laethem","jared.laethem@yourcompany.com","2008-02-24 22:21:32","true"
"jerrod.bennett","Jerrod Bennett","jerrod.bennett@yourcompany.com","2007-08-12 12:12:18","true"
"eric.schroeder","Eric Schroeder","eric.schroeder@yourcompany.com","2007-07-03 11:50:20","true"
"rob.woodbyrne","Rob Woodbyrne","rob.woodbyrne@yourcompany.com","2007-07-03 11:49:57","true"
"admin","System Administrator","admin@yourcompany.com","2007-07-03 11:48:47","true"
"christen.mitchell","Christen Mitchell","christen.mitchell@yourcompany.com","2007-05-16 15:26:42","true"
"rob.phillips","Rob Phillips","rob.phillips@yourcompany.com","2007-01-22 11:25:34","true"
"davin.czukowski","Davin Czukowski","davin.czukowski@yourcompany.com","2006-07-11 14:01:26","true"
"luke.wilson","Luke Wilson","luke.wilson@yourcompany.com","2006-02-07 15:29:48","true"
"bow.ruggeri","Bow Ruggeri","bow.ruggeri@yourcompany.com","2005-07-07 11:39:58","true"
"don.goodliffe","Don Goodliffe","don.goodliffe@yourcompany.com","2005-05-02 12:28:40","true"
"david.loo","David Loo","david.loo@yourcompany.com","2005-02-22 16:00:00","true"
"guest","Guest","guest@yourcompany.com","2004-05-01 17:00:00","true"
"fred.luddy","Fred Luddy","fred.luddy@yourcompany.com","2004-05-01 17:00:00","true"
```

When using CSV files, you can specify the encoding charset using the **Properties** field on the Data Source form. You may need to [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US) the Data Source form to see this field. For example, to use utf-8 encoding, enter **charset=utf-8**.

## Data in single column

For the JSON and XML formats, this feature lets you store a full record in a single column.

The column name used to store the full record is `data`.

If you create a JSON format data source to save data in a single column, selecting the **Data in single column** check box updates the following options:

-   **Discard Array** becomes unselected and is removed from the form.
-   **Expand node children** becomes selected and is removed from the form.

![JSON data in a single column](../image/json-data-in-single-column.png "JSON data in a single column")

If you create an XML format data source to save data in a single column and you select the **Data in single column** check box, **Expand node children** becomes selected and is removed from the form.

![XML data in a single column](../image/xml-data-in-single-column.png "XML data in a single column")

## Custom \(Parse by Script\) format

When you select a **Type** of **File** and a **Format** of **Custom \(Parse by Script\)**, a Javascript editor called **Parsing script** appears. You can use the parsing script to create customized Javascript to parse input lines into the list of maps.

The Javascript has three predefined parameters:

-   The **line** parameter is a string which contains line data from the source file.
-   The **lineNumber** is the line number from the source file for this line data.
-   The **result** parameter is used to pass back the parsed result from Javascript.

The **result** parameter is an instance of Java object ScopedScriptParseResult. When you type `result.`, four available methods appear as script auto-complete in the Javascript editor:

![Auto-complete menu](../image/auto-complete.png "Auto-complete menu")

-   `void setSkip(boolean skip);`
-   `boolean getSkip();`
-   `addRow(Map<String, String> map);`
-   `List<Map<String,String>> getRows()`

The `setSkip()` and `getSkip()` set and retrieve the skip flag. When the skip flag is set to true, the entire parsing result from Javascript is ignored.

The `addRow()` adds one map of the parsing row result, which is inserted into the staging table.

The `getRows()` retrieves all rows of the current parsing result, which are inserted into the staging table.

One line of source data can contain one row or multiple rows. It is up to the script writer to decide how to process the line data. For example, for line data `name=john,computer=windows;name=joe,computer=linux;name=linda,computer=windows`, if you use a semicolon \(;\) as a row break, then this line contains three rows of data. Each row is a map with two keys: `name` and `computer`. The `name` and `computer` become the column names for the staging table schema. You could use the following sample of Javascript to parse this line data:

```
(function(line, lineNumber, result) {
 var rowArr = line.split(";");
 var i;
 for(i in rowArr) {
 var map = {};
 var arr = rowArr[i].split(",");
 var x;
 for(x in arr) {
 var items = arr[x].split("=");
 map[items[0]]=items[1];
 }
 result.addRow(map);
 }
})(line, lineNumber, result);
```

The script writer must add the result so that the result is inserted in the staging table.

