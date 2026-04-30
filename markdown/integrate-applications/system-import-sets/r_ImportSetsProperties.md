---
title: Import sets properties
description: Multiple properties control import set behavior.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Import sets, Imports, Data and Automation]
---

# Import sets properties

Multiple properties control import set behavior.

## Import sets properties

-   **glide.import\_set.preserve.leading.spaces**

    Specifies whether the import process preserves leading spaces in Excel data cells. When false, the import process removes non-breaking leading spaces from Excel data cells. When true, the import process preserves non-breaking leading spaces.

    **Note:** The import process always removes trailing spaces from Excel data cells.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.import\_set\_row.dynamically\_add\_fields**

    Specifies whether an import set can add new columns to the staging table \(true\) or not \(false\). Instances that contain large numbers of import sets can sometimes become unresponsive when an import adds a column because the instance must alter every row in the staging table. In some cases, the database alter table action causes an outage. Setting this property to false prevents an import set from adding columns to the staging table and produces a log message. As a workaround, administrators can manually add a column to the staging table by creating a new dictionary entry and then reimporting the import set.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **com.glide.loader.verify\_target\_field\_size**

    Enables dynamic resizing of import set fields. With the default setting of **false**, up to 20 records of the source data are sampled to determine the import set field length. If the field is empty in all the sampled records, the default length of 40 is used. Any data loaded that exceeds the import set table field length is truncated. Set this property to **true** to allow any import set field to increase the column size by 100 to match the length of the data. For example, if the incoming source data has a length of 60, the system sets the length of the column to 160. This is relevant to data source only.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.ds.file.http.variable\_replacement**

    Enables system property expansion for File-type data sources that are retrieved using HTTP or HTTPS.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
    -   More information: [Data source fields](r_DataSourceFileTypeFields.md)
-   **glide.scheduled\_import.stop\_on\_error**

    Set to true to stop the import process when the parent scheduled import generates an error. This behavior can be useful when one import set depends on the results of another import set.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.impex.transformer.empty\_value\_nil**

    Controls how empty string values are handled during transformation from an import set staging table. Set this property to true to preserve empty strings. Set this property to false to convert empty strings to the string `NULL`.

    **Note:** An empty string is always stored as a null value in the database, regardless of this property value.

    You can use this property when you run an onBefore script during transformation. Setting this property to true allows you to check for null values using hasValue\(\) or nil\(\) functions.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **com.glide.loader.max\_scan\_rows**

    Controls how many rows of source data are sampled to automatically generate staging table fields when you import data. This property applies to JDBC, XLS, CSV, and XML imports but not to JSON and XSLX imports.

    -   Type: integer
    -   Default value: 20
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

## Concurrent import sets properties

-   **glide.scheduled\_import.max.concurrent.import\_sets**

    Maximum number of import sets for one concurrent import.

    -   Type: Integer
    -   Default value: 10
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **com.glide.concurrent\_import\_set\_insert\_mutex\_spin\_wait**

    Wait time mutex spends if the lock is acquired \(in milliseconds\).

    -   Type: Integer
    -   Default value: 1000
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **com.glide.concurrent\_import\_set\_insert\_mutex\_expiration**

    Mutex expiration time \(in milliseconds\).

    -   Type: Integer
    -   Default value: 300000
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **com.glide.concurrent\_import\_set\_mutex\_fast\_lock**

    Specifies whether to use fast lock \(true\) or SQL-based slow lock \(false\).

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

## Web service import sets properties

-   **com.glide.ws\_import\_set.column\_resize**

    When true, enables dynamic column resizing on import staging tables for web service import sets.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **com.glide.ws\_import\_set.column\_resize.max\_row\_count**

    The maximum number of rows an import staging table can have for dynamic column resizing with web service import sets.

    Import staging tables with more than this number of rows will not use dynamic resizing with web service import sets, even if **com.glide.ws\_import\_set.column\_resize** is true.

    This property has a maximum value of 500,000.

    -   Type: Integer
    -   Default value: 100,000
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

## CSV properties

-   **com.glide.csv.loader.ignore\_non\_parseable\_lines**

    Allows an instance to ignore one or more lines \(rows\) that contain bad data in a CSV import, such as a row that is missing a column of data. By default, imports cannot ignore bad data in CSV files and fail on the first error.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **com.glide.csv.loader.max\_errors\_allowed**

    Specifies the maximum number of lines \(rows\) that an import can ignore before failing. If the import succeeds, the import lists the number of rows the import ignored due to errors.

    -   Type: integer
    -   Default value: 100
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.import.csv.charset**

    The charset of the CSV file to import. Valid values are UTF-8 and WINDOWS-1252. You may need to use UTF-8 formatting when importing special characters.

    -   Type: String
    -   Default value: WINDOWS-1252
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

## Excel import properties

-   **glide.excel.multiplier**

    The maximum amount of instance memory to allocate to an Excel import. This property applies when importing .XLS files only.

    The value of this property is multiplied by the file size of the Excel file to determine the total memory allocation. The memory used cannot exceed the limit specified by the **glide.excel.max\_memory\_percent** property.

    For example, with the default value 8 and a 10MB Excel file, the instance will use up to 80MB of memory for the import.

    -   Type: integer
    -   Default value: 8
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.xlsx.multiplier**

    The maximum amount of instance memory to allocate to an Excel import. This property applies when importing .XLSX files only.

    The value of this property is multiplied by the file size of the Excel file to determine the total memory allocation. The memory used cannot exceed the limit specified by the **glide.excel.max\_memory\_percent** property.

    For example, with the default value 10 and a 10MB Excel file, the instance will use up to 100MB of memory for the import.

    **Note:** Do not modify the value of this property. The default value was selected for optimal performance.

    -   Type: integer
    -   Default value: 10
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.excel.max\_memory\_percent**

    The maximum amount of memory allowed for Excel imports, as a percentage of the total instance memory.

    -   Type: integer
    -   Default value: 10
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.excel.use\_disk\_backed\_strings\_table**

    Controls whether the instance uses disk storage to maintain large file data during XLSX import. Set this property to false to store XLSX file data only in memory. Setting this property to false increases the memory used during XLSX import.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.excel.in\_memory\_strings\_table\_size\_mb**

    The maximum amount of memory, in megabytes, available to store XLSX file data before writing to disk storage when glide.excel.use\_disk\_backed\_strings\_table is true. Setting a lower value for this property will use less memory during XLSX import but may result in slower imports.

    -   Type: integer
    -   Default value: 5
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.xlsx.import.debug**

    Enables debug logging for XLSX imports.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.import.excel.enhanced\_number\_conversions**

    When true, numeric values greater than 10 million are preserved in import staging tables. When false, imported values greater than 10 million are converted to scientific notation that may not match the original imported value. This property should be set to true for importing most kinds of data.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.transform.boolean.casesensitive**

    When true, upper case boolean values of \(TRUE/FALSE\) always transform to false. When false, upper case boolean values \(TRUE/FALSE\) are transformed correctly.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

## JDBC connection properties

-   **glide.jdbcprobeloader.retry**

    The number of times a JDBC probe loader attempts to process data returning from a JDBC data source. Sleeps on the value defined in **glide.jdbcprobeloader.retry\_millis** between retries.

    -   Type: integer
    -   Default value: 60
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.jdbcprobeloader.retry\_millis**

    How many milliseconds a JDBC probe loader waits in between retry attempts to process data from a JDBC data source.

    -   Type: integer
    -   Default value: 5000
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

## Logging and debug properties

-   **com.glide.import\_set.importlog\_level**

    Specifies how much information import sets add to the log. Possible values are INFO, WARNING, and ERROR. You can set this to INFO in the dev environment and change it to WARNING or ERROR in production to reduce amount of logging noise traffic to the database.

    **Note:** This property does not impact logging related to the cleanup of staging tables.

    -   Type: string
    -   Default value: INFO
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.import.debug**

    Enables debug logging for all import processes.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)Add to the System Property \[sys\_properties\] table
-   **glide.importlog.log\_to\_table**

    Specifies whether to write information-level log messages into the import\_log table. When true, the information-level log messages are written.

    **Note:** The information-level logs for [IntegrationHub ETL](https://www.servicenow.com/docs/access?context=integrationhub-etl&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) are written to the importlog.log table regardless of this property setting. To have additional exceptions added, contact Now Support.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.import.sftp.debug**

    Enables additional debug logging for SFTP imports. Enabling this property will cause the instance to log all outgoing and incoming messages during the SSH session.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   **glide.import.scp.debug**

    Enables additional debug logging for SCP imports. Enabling this property will cause the instance to log all outgoing and incoming messages during the SSH session.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

**Parent Topic:**[Import sets](import-sets-landing-page.md)

