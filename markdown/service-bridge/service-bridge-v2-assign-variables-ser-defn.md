---
title: Create variables for remote record producers in Service Exchange for Providers
description: Create the variables for a remote record producer in Service Exchange for Providers application.
locale: en-US
release: xanadu
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Remote record producers in Service Exchange, Create remote catalogs in Service Exchange for providers, Installing and configuring Service Exchange for Providers, Service Exchange for Providers, Service Exchange]
---

# Create variables for remote record producers in Service Exchange for Providers

Create the variables for a remote record producer in Service Exchange for Providers application.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Administration** &gt; **Remote Catalog Items**.

2.  Click a record producer that you want to create variables for.

3.  Click the **Variables** tab in the Related List and then click **New**.

4.  On the form, fill in the fields.

<table id="table_brn_vgs_jmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Supported variable types are as follows: -   Attachment
-   Break
-   CheckBox
-   Container End
-   Container Split
-   Container Start
-   Date
-   Date/Time
-   Duration
-   Email
-   HTML
-   IP Address
-   Label
-   List Collector
-   Lookup Multiple Choice
-   Lookup Select Box
-   Masked
-   Multi line text
-   Multiple Choice
-   Numeric Scale
-   Reference
-   Requested For
-   Rich Text Label
-   Select Box
-   Single Line Text
-   URL
-   Wide Single LineText
-   Yes/No
If you use unsupported variables, Service Exchange might not integrate the data in the right format.

</td></tr><tr><td>

Catalog item

</td><td>

Catalog item that uses the variable.

</td></tr><tr><td>

Application

</td><td>

This is a read only field and is set by default based on the application scope.

</td></tr><tr><td>

Mandatory

</td><td>

Option for making the variable mandatory as part of the ordering process.**Note:** This behavior is applicable only on a page load. You can change it by using client APIs.

</td></tr><tr><td>

Active

</td><td>

This is a read only field and is enabled based on the **Publish**, **Retire**, or **Edit** actions.

</td></tr><tr><td>

Order

</td><td>

Placement order of the variable on the catalog item page. You organize the variables from top to bottom, and from the least to the greatest order value. For example, a variable with an order value of 1 is placed ahead of other variables with higher-order values.

</td></tr><tr><td>

Question

</td><td>

Question that you can ask users who are ordering the catalog item to obtain related information.

</td></tr><tr><td>

Name

</td><td>

Name to identify the question.**Note:** If this field is empty, its value is auto-populated based on the **Question** field for all variable types except Break, Container Split, and Container End.

</td></tr><tr><td>

Tooltip

</td><td>

Tooltip text to display when users point to the variable. Enter a brief note to describe the purpose of the question.

</td></tr><tr><td>

Example Text

</td><td>

Question field hint that appears before a user enters a value.You can use a hint for the following variables:

-   IP Address
-   Email
-   URL
-   Single Line Text
-   Wide Single Line Text
-   Multi Line Text
-   Date
-   Date/Time


</td></tr><tr><td>

Type Specification

</td><td>

Values specific to the type of variables.

</td></tr></tbody>
</table>5.  Click **Submit**.

    Repeat the above steps to create additional variables for the same remote record producer.


