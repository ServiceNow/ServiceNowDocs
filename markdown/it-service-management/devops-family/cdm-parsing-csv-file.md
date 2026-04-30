---
title: Parsing of CSV files in CDM
description: The CDM CSV parser enables parsing of data in CSV files, so when you upload config data from a Comma-Separated Values \(CSV\) file into CDM, you can easily identify the data format attributes and config data in the CDM editor or list view.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Uploading your config data, Configure, DevOps Config, IT Service Management]
---

# Parsing of CSV files in CDM

The CDM CSV parser enables parsing of data in CSV files, so when you upload config data from a Comma-Separated Values \(CSV\) file into CDM, you can easily identify the data format attributes and config data in the CDM editor or list view.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

The CDM CSV parser follows the CSV standard RFC 4180. This parsing of data from a CSV file to a JSON format in CDM helps you in the following ways:

-   Uploading existing config data from a CSV file with custom header and delimiter attributes to parse them as appropriate key-value pairs in JSON.
-   Differentiating data format attributes \(metadata\) from the config data items \(data\) in the CDM editor.
-   Validating imported CSV data in CDM for deployment.
-   Converting config data from JSON format to CSV format with attributes in the original format.

## Parsing of CSV to JSON during import

When you import a CSV file into CDM, the parser converts the data in CSV format to the JSON format as follows:

-   Adds each record from the CSV file as a CDI in separate indexed nodes under the **data** node in JSON format.
-   Adds the data format attributes used during CSV upload under the **metadata** node.

    The query parameter **dataFormatAttributes** includes attributes for determining the delimiter, headers, first row as header, and secured headers.

<table id="table_jkn_hbd_bzb"><thead><tr><th>

Attribute name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

delimiter

</td><td>

Character to separate out each header field as a key and the record field as a value of a CDI. You can specify a valid character as the delimiter.Default: `"delimiter": ","`.

</td></tr><tr><td>

containsHeader

</td><td>

Option to determine whether the first row in the CSV file is considered as the header row. This attribute is optional.-   true: The CSV file contains the first row as the header.
-   false: The CSV file doesn't have the first row as the header. In this case, you must provide the headers in the **headers** attribute.
Default: `"containsHeader": "true"`.

</td></tr><tr><td>

headers

</td><td>

List of header fields for record fields in the CSV file. These headers are converted to the key names of the CDIs in the JSON format.**Note:** This attribute is applicable only if the **containsHeader** attribute is set to **false**.

If your CSV file doesn't have the first row with headers, you can provide an array of headers. The number of headers must match the number of record fields. Example: `"headers": ["FirstName","LastName","Location","Salary"]`.

Default: An empty array: `"headers": []`.

</td></tr><tr><td>

securedHeaders

</td><td>

List of header fields for which the value for all records is displayed in the encrypted format in the JSON format. This attribute is optional.You can provide an array of headers that must be secured. The name of the secured headers must match the name of the headers in the **headers** attribute or CSV file. Example: `"securedHeaders": ["Salary"]`.

Default: An empty array: `"securedHeaders": []`.

</td></tr></tbody>
</table>
## Conversion of CSV to JSON format

This example shows the given data format attributes and the conversion of CSV content to the JSON format based on these attributes.

-   **Data format attributes**

    **Note:** This parameter is optional. If you don't provide values, the default values of the attributes are used.

    `{ "delimiter": ",", "containsHeader": "true", "headers": [], "securedHeaders": ["salary"] }`

-   **CSV format**

    ```
    //Sample CSV file content: no header in the first row; each line represents a record 
      FirstName,LastName,Location,Salary
      David,Ben,NYC,1000
      Jakes D,Ron,IRE,1220
      "George, R",Martin,US,12120
      "Antony, ""Ron",Mak,US,1210
    ```

-   **JSON format**

    ```json
    
    //data node for the records from CSV - each record row converted to individual nodes with fields separated by delimiter character converted to individual items of the node{
    	"data": {   
    		"0": {
    			"FirstName": "David",
    			"LastName": "Ben",
    			"Location": "NYC",
    			"Salary": "*****"
    		},
    		"1": {
    			"FirstName": "Jakes D",
    			"LastName": "Ron",
    			"Location": "IRE",
    			"Salary": "*****"
    		},
    		"2": {
    			"FirstName": "George, R",  //the name has a delimiter char so the full name is enclosed within " "
    			"LastName": "Martin",
    			"Location": "US",
    			"Salary": "******"
    		},
    		"3": {
    			"FirstName": "Antony, \"Ron", //the last name has "" so a \ is added to include " in the last name
    			"LastName": "Mak",
    			"Location": "US",
    			"Salary": "*****"
    		}
    	},
    //metadata added for the data format attributes
    	"metadata": {   
    		"containsHeader": "true",
    		"delimiter": ",",
    		"headers": "FirstName�LastName�Location�salary",
    		"securedHeaders": "Salary"
    	}
    }
    ```


## Parsing of JSON to CSV during export

To keep the CSV config data in its original format when exporting the config data to a CSV file format, ensure that you have the **data** and **metadata** nodes in your data.

-   Config data items within the **data** node are converted to individual record rows in the CSV file.
-   Data format attributes within the **metadata** node are used to define the delimiter, header, and secret header information in the CSV file.

**Related topics**  


[Uploading your config data](cdm-upload-process.md)

[Add the nodes that will contain config data to a new CDM application](../task/cdm-data-structure-add-for-upload.md)

[Parsing of XML files in CDM](cdm-parsing-xml-file.md)

