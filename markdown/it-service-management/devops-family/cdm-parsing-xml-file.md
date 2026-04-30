---
title: Parsing of XML files in CDM
description: The CDM XML parser enables the parsing of attribute key-value pairs in XML files, so when you upload config data from an XML file into CDM, you can easily identify the attributes of each element in the CDM editor or list view.
locale: en-US
release: xanadu
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Uploading your config data, Configure, DevOps Config, IT Service Management]
---

# Parsing of XML files in CDM

The CDM XML parser enables the parsing of attribute key-value pairs in XML files, so when you upload config data from an XML file into CDM, you can easily identify the attributes of each element in the CDM editor or list view.

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

This parsing of attribute key-value pairs from an XML file to a JSON format in CDM helps you in the following ways:

-   Uploading existing config data from an XML file, including the attributes of XML elements as appropriate key-value pairs in JSON.
-   Differentiating attributes from the config data items easily in the CDM editor.
-   Validating imported CSV data with attributes in CDM for deployment.
-   Converting attribute key-value pairs in JSON format as XML element attributes in XML file.

## Parsing of XML to JSON during import

When you import an XML file to upload your config data into CDM, the parser converts attributes and enclosing text in XML elements to the JSON format as follows:

-   Adds the **@** prefix to all key names corresponding to attributes of XML elements.
-   Adds a **\#text** key for the enclosing text value of XML elements that have both attributes and enclosing text.

These options help in identifying attributes and enclosing text in the Editor panel and List view while reviewing the config data.

The following example shows how the conversion looks between XML and JSON formats:

-   **XML format**

    ```xml
    <app>
         <components>
               <paymentService type="B2C">
                         <provider region="EMEA">ABCPay</provider>
                         <service>XYZPay</service>
               </paymentService>
         </components>
    <app>
    ```

-   **JSON format**

    ```json
    {
       "app" : {
             "components" : {
                     "paymentService" : { //key-value pair for XML elements with attributes
                              "@type" : "B2C", // @ prefix for attribute
                              "provider" : {
                                    "@region" : "EMEA", // @ prefix to key name for attribute 
                                    "#text" : "ABCPay"  // #text key name for enclosing text
                                },
                      "service" : "XYZPay" //key-value pair for XML elements without attributes
                      }
               }
       }
    }
    ```


## Parsing of JSON to XML during export

To keep the XML attributes and enclosing text in their original format when exporting the config data to an XML file format, you must update the config data as follows:

-   Add the **@** prefix to all key names to make them parse as attributes of XML elements.
-   Add keys named **\#text** to CDIs that should be parsed as the enclosing text value of XML elements, when both attributes and enclosing text are present.

**Related topics**  


[Uploading your config data](cdm-upload-process.md)

[Add the nodes that will contain config data to a new CDM application](../task/cdm-data-structure-add-for-upload.md)

[Parsing of CSV files in CDM](cdm-parsing-csv-file.md)

