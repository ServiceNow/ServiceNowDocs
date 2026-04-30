---
title: Create a Security Operations enrichment data map
description: Transform data from JSON, XML, or Properties file format to ServiceNow records using enrichment data maps.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Security Operations enrichment data mapping, Security Operations common functionality, Security Operations]
---

# Create a Security Operations enrichment data map

Transform data from JSON, XML, or Properties file format to ServiceNow records using enrichment data maps.

## Before you begin

Role required: sn\_sec\_cmn.write

## About this task

Existing enrichment data maps are used by workflows provided within Security Operations. You can view the list under **Enrichment Data Mapping**. To use a map, you need a trigger, either a business rule or workflow.

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Utilities** &gt; **Enrichment Data Mapping**.

2.  Click **New**.

3.  Fill in the fields, as appropriate.

<table id="table_qfl_nwk_cp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of this enrichment data map.

</td></tr><tr><td>

Input format

</td><td>

Choose a format from the list:-   JSON \(default\)
-   XML
-   Properties File format


</td></tr><tr><td>

Prefix key

</td><td>

Use to limit the input data set to a specified key. The root of the input data set is set to this key. In this example, if you entered file\_info, then the input values would be limited to those values within file\_info. ```
<?xml version="1.0" encoding="UTF-8"?>
<malware>
    <version>2.0</version>
    <file_info>
        <malware>yes</malware>
        <sha1>24c051142583e10451a53893fed3aa5d80bfb1f6</sha1>
        <filetype>PE</filetype>
        <sha256>be9bd96808173e2d967feef8c8c5b8c4d73b621584fb11eb68434da1e6a0a930</sha256>
        <md5>ee8c91751b3010e38c479cf9ab09827a</md5>
        <size>546304</size>
    </file_info>
</malware>
```

</td></tr><tr><td>

Application

</td><td>

Scope of the application.

</td></tr><tr><td>

Duplication rule

</td><td>

Rule defining when a record is considered a duplicate and what actions to take with duplicate records.

</td></tr><tr><td>

Destination table

</td><td>

Choose a table from the list.

</td></tr><tr><td>

Active

</td><td>

Select this check box to activate the map.

</td></tr><tr><td>

Description

</td><td>

Enter a description of the enrichment data map.

</td></tr></tbody>
</table>4.  Click **Submit.**

    The Enrichment Data Mapping Fields tab appears.

5.  Click **New**.

6.  Fill in the fields on the form, as appropriate.

<table id="table_tql_dvg_lw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field

</td><td>

Name of the enrichment data map.

</td></tr><tr><td>

Value type

</td><td>

Choose from the list: -   Lookup data using property key
-   Static value
-   Static value plus data from the property key
-   Field is an array or object \(raw data nesting\)
 Each choice has different entries. Field values and arrays or objects require a Property key.

</td></tr><tr><td>

Property key

</td><td>

Determines the key for the input data search and the value written to the target field.

</td></tr><tr><td>

Value transform

</td><td>

The field value transform that maps one value to another.

</td></tr><tr><td>

Application

</td><td>

Scope of the application.

</td></tr><tr><td>

Order

</td><td>

In what order to consider the mapping. The first match is used. Default is 100.

</td></tr><tr><td>

Mapping

</td><td>

Name of the enrichment data map.

</td></tr><tr><td>

Destination table

</td><td>

The table to which the fields to map are going.

</td></tr></tbody>
</table>7.  Click **Submit**.

    The following is an example of an enrichment data map.

    ![Enrichment Data Mapping example](../image/EnrichmentDataMapForm.png)


**Parent Topic:**[Security Operations enrichment data mapping](../concept/enrichment-data-mapping.md)

