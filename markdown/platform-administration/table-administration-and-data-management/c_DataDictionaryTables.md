---
title: Data dictionary tables
description: Access details related to tables, columns, and field labels in your instance.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Explore, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Data dictionary tables

Access details related to tables, columns, and field labels in your instance.

## Tables

All of the information on an instance is stored in tables, which consist of a series of records. The record in turn holds a series of fields that hold the individual bits of data and can be viewed either as a list or a form.

The Tables \[sys\_db\_object\] table contains a record for each table in the database.

Access the Tables \[sys\_db\_object\] table by navigating to **System Definition** &gt; **Tables**. From the Tables list, an administrator can create a custom table, or select an existing table to view table details. In the table form, an administrator can access table administration options.

-   View, add, or modify columns with a searchable and sortable embedded list, define the auto-number format, make the table extendable by other tables, and create modules for the table.
-   Launch a schema map for a table by clicking the **Show Schema Map** related link.
-   Open the dictionary entries for the table by right-clicking the form header and selecting **Show Dictionary Record**.
-   Navigate directly to the default list or form view for the table by clicking the **Show List** or **Show Form** related link.
-   Delete all records from a table by clicking the **Delete All Records**.

The following image shows a list of the tables that extend the Application File table.

![A list of tables that extend the Application File table.](../image/Tables2.png "Tables")

## Dictionary Entries

The Dictionary Entries \[sys\_dictionary\] table, also called the **System Dictionary**, defines every table and field in the system. It contains information about data type, character limit, default value, dependency, and other attributes of a field.

Access the system dictionary in one of these ways:

-   To see the system dictionary list view, navigate to **System Definition** &gt; **Dictionary**.
-   To view particular dictionary definition, right-click the list header, form header, or field label, and select **Configure Dictionary**.

The following image shows a filtered list of dictionary entries for the Incident table and the Task table, which it extends.

![A filtered list of dictionary entries for the Incident table and the Task table.](../image/DictionaryIncTask2.png "Dictionary Inc Task")

## Field Labels

The Field Labels \[sys\_documentation\] table, also called the **Language File**, contains information about the labels and hints for each table and column in the system.

Access the language file in one of these ways:

-   To see the list view, navigate to **System Definition** &gt; **Language File**.
-   To see the field label for a particular field, right-click the field label on the form.

The following image shows the language file filtered to display only labels on the Incident table.

![A list showing field labels on the Incident table.](../image/Fieldlabels2.png "Field Labels")

**Parent Topic:**[Exploring ServiceNow AI Platform tables](../../table-administration/concept/exploring-table-administration.md)

