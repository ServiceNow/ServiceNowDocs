---
title: Create a data source for LDAP
description: Each LDAP organizational unit \(OU\) definition has its own related list of data sources.
locale: en-US
release: zurich
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [LDAP integration setup, LDAP integration, Authentication, Access Management]
---

# Create a data source for LDAP

Each LDAP organizational unit \(OU\) definition has its own related list of data sources.

## Before you begin

Role required: admin

## About this task

**Note:** Both the **LDAP Server** and **LDAP OU Definition** must be active for the test load action to function properly. When the test load is activated for the first time, the system samples up to 20 records to determine the length of the import set fields. If the sampled records do not contain values for the **User ID** field, the system sets the field length for all subsequent imports to the default length of 40. The import truncates any imported data that exceeds the import set table field length. Additionally, the **User ID** field is truncated to a maximum of 40 characters. Be aware that the 20 loaded records cannot be transformed and are for testing purposes only. If the test records contain values for the **User ID** field, the field length is set based on the field length of the longest user ID in the test records.

To create a new data source:

## Procedure

1.  Navigate to **All** &gt; **System LDAP** &gt; **LDAP Servers**.

2.  Select the LDAP server to configure.

3.  In the **LDAP OU Definitions** related list, select an item, such as **Groups** or **Users**.

4.  In the **Data Sources** related list, click **New**.

5.  Complete the Data Source form \(see table\).

6.  Click **Submit**.

7.  Under **Related Links**, click **Test Load 20 Records** to test whether the data source can bring LDAP data into the import table.

    |Field|Description|
    |-----|-----------|
    |Name|Specify the name the integration uses when referencing this data source.|
    |Import set table name|Enter the name of the staging table where the system temporarily places the imported LDAP records and attributes. Review this table to view imported LDAP records. You can use the same import set table name for all LDAP data sources.|
    |Type|Select **LDAP** to indicate the imported data is LDAP data. After you select the type **LDAP**, the form displays the **LDAP target** field.|
    |LDAP target|Select the LDAP OU definition associated with this data source.|


