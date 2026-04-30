---
title: Create a record producer to add additional details
description: Configure a record producer with additional details and add it to the reservable module. The fields configured for additional details will be displayed to the employee when they make a reservation.
locale: en-US
release: zurich
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure a reservable module, Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create a record producer to add additional details

Configure a record producer with additional details and add it to the reservable module. The fields configured for additional details will be displayed to the employee when they make a reservation.

## Before you begin

Before you configure the record producer, refer to [Additional details record producer - Mapping Variable types and limitations](../reference/custom-fields-record-producer-mapping-variable-type-conditions.md).

**Note:** The record producer is only used to retrieve data related to the additional fields.

If you want to add details that aren’t included in the Workplace Reservation \(sn\_wsd\_rsv\_reservation\) table, you must perform the following:

**Important:** In the Workplace Reservation \(sn\_wsd\_rsv\_reservation\) table, Columns related list, when you add fields \(columns\) that aren’t included, note the following:

-   On the Dictionary Entry form, the **Mandatory**, **Read only** and **Display** fields are not applicable.
-   The columns in the table are created to only store the data.
-   The **Max length** field is considered to save the data with **Max length**.

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.
2.  Open the Workplace Reservation \(sn\_wsd\_rsv\_reservation\) table.
3.  On Table form, scroll down to the Columns related list.
4.  Select **New**.
5.  On the Dictionary Entry form, fill in the fields.

    For more information on columns and fields, refer to [Exploring field administration](https://www.servicenow.com/docs/access?context=c_IntroductionToFields&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

6.  Select **Submit**.

    The table column is added.

7.  **Update** the Workplace Reservation \(sn\_wsd\_rsv\_reservation\) table

**Note:**

When you configure the record producer, note the following:

-   You can add **Catalog UI Policies** to the record producer.
-   Only the following **Catalog Client Scripts** types are supported:
    -   OnChange
    -   OnLoad
-   Code added in the **Script** isn’t supported.
-   The following record producer related lists aren’t supported:
    -   Variable Sets
    -   Not Available For
    -   Categories
    -   Catalogs
    -   Catalog Data Lookup Definitions
    -   Related Articles
    -   Related Catalog Items
    -   Assigned Topics

Role required: sn\_wsd\_rsv.admin

## About this task

Create a record producer with additional details and link it with the reservable module on which you want the details to be displayed to an employee. For example, if you add a record producer - Related Information and link it with the Meeting rooms reservable module, then the reservation form in the Reservation Portal displays an additional section - Related Information as follows:

Record producer form of 'Related Information':

![Record producer form of 'Related Information'.](../image/additionaldetails-recordproducer.png)

Reservation portal - Reservation form with the 'Related Information' section:

![Reservation portal - Reservation form with the 'Related Information' section.](../image/additionaldetails-rsvportal.png)

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Record producers**.

2.  Select **New**.

3.  Enter the **Name** of the record producer.

4.  In the **Table name** select Workplace Reservation \(sn\_wsd\_rsv\_reservation\) table.

5.  Select **Active** to activate the record producer.

    For further form field descriptions, refer to [Record Producer form](https://www.servicenow.com/docs/access?context=record-producer-form&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

6.  Select and hold \(or right-click\) on the form header and select **Save**.

    The record producer is created. After creation, a list of record producers created in the application is displayed.

7.  From the list, open the record producer that you created.

8.  In the **Variables** related list, add the additional details that you want to configure.

    Variables collect information from the user, and are used to ask questions and map answers to fields. You can add as many variables as you need to the reservation form. Commonly used variable types include:

    -   Checkbox
    -   Multiple Choice
    -   Reference
    -   Select Box
    -   Single Line Text
    To learn more about the different types of variables and how to configure them, see [Types of service catalog variables](https://www.servicenow.com/docs/access?context=r_VariableTypes&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) Types of service catalog variables.

    1.  Select **New**.

    2.  On the Variable form, select **Map to field**.

    3.  In the **Order** field, specify in what order should the field appear.

    4.  In the **Field** field, select the field that you want to add.

        You can select from a list of fields available with the Workplace Reservation \(sn\_wsd\_rsv\_reservation\) table.

    5.  Select **Active** to activate the field.

    6.  To set the field as required, select **Mandatory**.

    7.  To set the field as read only, select **Read only**.

    8.  To hide the field, select **Hidden**.

    9.  In the **Question** related list, enter the name of the field in the **Question** field.

        The name specified in the **Question** field is displayed on the form.

    10. Select and hold \(or right-click\) on the header and select **Save**.

        The field is added. Repeat the above steps if you want to add more fields.

    **Important:** The Permission and Availability related lists aren’t supported for the variable.

9.  Navigate back to the Record producer form.

    The added fields are displayed in the **Variables** related list.

10. You can add **Catalog UI Policies**.

    Refer to [Service catalog UI policy](https://www.servicenow.com/docs/access?context=c_ServiceCatalogUIPolicy&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

11. You can add **Catalog Client Scripts**.

    Refer to [Create a Service Catalog client script](https://www.servicenow.com/docs/access?context=t_CreateACatalogClientScript&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    **Note:** Only the following Client Scripts types are supported:

    -   OnChange
    -   OnLoad \(Note: The script part must be wrapped in setTimeout\)
12. Select **Update**.


## Result

The record producer is created with the additional details.

## What to do next

[Create a record producer to add additional details](create-a-record-producer-to-add-additional-fields.md)

**Parent Topic:**[Configure a reservable module](config-reservable-module.md)

