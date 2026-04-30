---
title: Transaction Manager: Fields
description: Understand the five major field type options: text, number, Boolean, picklist, and date/time. Learn how to create new fields using the Admin UI.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-10"
reading_time_minutes: 12
breadcrumb: [Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Fields

Understand the five major field type options: text, number, Boolean, picklist, and date/time. Learn how to create new fields using the Admin UI.

In the Transaction Manager, administrators are able to create text, number, boolean, picklist, and date/time fields. Admins also have the choice of creating fields at the Transaction level or at the Transaction Line level.

Fields created at the Transaction level sit outside the Transaction Line grid. These fields commonly contain information about the Account, Addresses, List Price Total, Total Discount, andNet Total for all line items.

Fields created at the Transaction Line level sit in the Transaction Line grid. These can appear as column fields or as fields in the UI Effects: Line Details, Model, and Slide Out.

The selected level will ultimately impact the field’s availability for rules, which also have a Transaction and Transaction Line level.

In the buyside screenshot below, the sections marked '1' are Transaction-level fields; the fields in the section marked '2' are Transaction Line-level.

![Transaction screen](../images/cpq-txn-mgr-fields.jpeg)

## Field types

Transaction Manager provides the following field types:

-   Text
-   Number
-   Boolean
-   Picklist
-   Date/Time

We will review the various Field Type Options for each field type later in this article.

One new field type that is not a carryover from the Configuration world is the Date/Time field. This new field type was necessary in Transaction Manager due to the auditing and term calculation requirements found in the Transaction world.

We will discuss the auditing and term calculation details when we discuss the Date/Time Field Type Options later in this article.

## System-provided fields

Out of the box, Transaction Manager provides the administrator with a set of system-provided fields. These system provided fields are often used in Transaction processing. There are system provided fields at both the Transaction level and the Transaction Line level.

The system provided fields provide fields in the following categories:

Transaction Level:

-   Pricing Information
-   Opportunity Information
-   Transaction information
-   Account Information

For a full list of transaction-level fields, see [Transaction Manager: Transaction-level system fields](transaction-manager-transaction-header-level-system-fields.md).

Transaction Line Level:

-   Pricing Information
-   Transaction Line Information
-   Configuration Information
-   Product Information
-   Order Information

For a full list of line-level fields, see [Transaction Manager: Line-level system fields](transaction-manager-line-level-system-fields.md).

Custom fields:

Custom fields are fields that are required by their implementation that the System Administrator adds to the Transaction Manager Blueprint. Custom fields added via the Transaction Manager Admin UI are automatically associated with the Blueprint, no additional action needs to be taken. If Custom fields are bulk uploaded to the Transaction Manager Blueprint via the Matrix Loader, these fields must be associated with the Blueprint via the blueprint.yaml file. To achieve this association, simply add a list to the blueprint.yaml file detailing the field variable names that you would like to be associated with the Blueprint.

Here is a sample blueprint.yaml file showing the field associations \(see ‘relatedFields’ section\):

```
---
blueprints:
- variableName: default
  relatedFields:
  - txn.custom.transactionNumber
  - txn.custom.quoteName
  - txn.custom.quoteValidUntil
  - txn.custom.paymentTerm
  - txn.custom.accountSpecificDiscount
  - txn.custom.agreementDiscount
  - txn.line.custom.agreementLineDiscount
  - txn.line.custom.customerLineDiscount
 lastModifiedBy: mark@logik.io.sfdcdev
  name: Transaction Manager Default
  stages: /blueprints/default/stages/stage.yaml
  description: Transaction Manager Default blueprint
  layouts: null
  events: /blueprints/default/events/events.csv
  views: /blueprints/default/views/views.yaml
fieldOptions: /fields/fieldOptions.csv
rules: null
fields: /fields/fields.csv
```

## Creating new fields via the Admin UI

To a new field to the Transaction Manager Blueprint, follow these steps:

1.  Navigate to the Transaction Manager Admin UI.

2.  Click "Associated Fields".

    ![Admin transaction](../images/cpq-txn-mgr-associated-fields.jpeg)

3.  Click "Create Field" to create a new field.

    ![Utilities screen](../images/cpq-txn-mgr-create-field.jpeg)

    The New Field dialog box opens.

4.  Enter a Name in the Name field.

    As the Name value is being entered in the Name field, the same value is being mirrored in the Variable Name field. By default, Transaction Manager makes the Variable Name the same as the Name value that the Admin enters. The Variable Name however in created using “camel case” and all spaces and special characters are removed from the name. For example, if you type “Customer Billing Address” for the Name field, the Variable Name field will contain “customerBillingAddress”. If you want to create your own custom Variable Names, simply click the pencil icon at the right end of the Variable Name field and you will be allowed to enter your own value for Variable Name.

    ![New field screen](../images/cpq-txn-mgr-fields-select-level.jpeg)

5.  Choose whether this field will be a Transaction level field or a Transaction Line level field. Click the appropriate Select a Level option based on your decision.
6.  Choose the type of field you are creating from the 5 available field types.

    ![Select data type screen](../images/cpq-txn-mgr-fields-select-type.jpeg)

7.  Click the "Save" button to save your field.

At this point, you will brought into the field editor page for the type of field that you chose to create. We will now review the various field type Options for each field type.

## Text field options

In the top left portion of the Field Editor page, you will see the Name and Variable Name you created in the New Field page. You can change the Name Value, but the Variable Name value is locked in and can only be changed if you delete the field and re-add it to the Blueprint. You can add a Description of the field and there is a Required toggle you can set if the field is to be a required field on the buyside Layout.

![Quote name](../images/cpq-txn-mgr-fields-quote-name.jpeg)

The Default Access field allows you to modify the access to this field in the Default View. You can make this field Read/Write accessible by choosing Editable as the access, you can set the field access to Read-Only, which means that the field will be visible on the buyside Layout but you will not be able to modify the field value directly, or you can set the field access to No Access which means that the field will be hidden from view on the buyside Layout and will not be accessible via APIs.

![Relationship access screen](../images/cpq-txn-mgr-fields-default-access.jpeg)

The Default Value field allows you set a default value for the Text field.

![Field description](../images/cpq-txn-mgr-text-default-value.jpeg)

The Minimum Field Length and Maximum Field Length allow you to set the minimum and maximum number of characters that can be entered into the Text field.

![Rules](../images/cpq-txn-mgr-min-max-length.jpeg)

## Number field options

In the top left portion of the Field Editor page you will see the Name and Variable Name you created in the New Field page. You can change the Name Value, but the Variable Name value is locked in and can only be changed if you delete the field and re-add it to the Bleuprint. You can add a Description of the field and there is a Required toggle you can set if the field is to be a required field on the buyside Layout.

![Number field options](../images/cpq-txn-mgr-txn-number.jpeg)

The Default Access field allows you to modify the access to this field in the Default View. You can make this field Read/Write accessible by choosing Editable as the access, you can set the field access to Read-Only, which means that the field will be visible on the buyside Layout but you will not be able to modify the field value directly, or you can set the field access to No Access which means that the field will be hidden from view on the buyside Layout and will not be accessible via APIs.

![Relationship access screen](../images/cpq-txn-mgr-fields-default-access.jpeg)

Number fields can take one of three forms, Number, Currency, or Percentage. Choose which form you want this Number field to take.

The Unit Label field allows you to determine what you would like the Unit Label to be for this numeric field. If the Number field is a Currency, then the Unit Label will be the default Currency symbol for your ServiceNow CPQ site. If the Number field is a Percentage then the Unit Label will be the Percent symbol \(%\).

The Minimum Value and Maximum Value fields allow you to set the minimum and maximum numeric value that will be allowed in this Number field.

![Number field options](../images/cpq-txn-mgr-number-field-options.jpeg)

The Default Value field allows you to set the default numeric value for this Number field.

## Boolean field options

In the top left portion of the Field Editor page you will see the Name and Variable Name you created in the New Field page. You can change the Name Value, but the Variable Name value is locked in and can only be changed if you delete the field and re-add it to the Bleuprint. You can add a Description of the field and there is a Required toggle you can set if the field is to be a required field on the buyside Layout.

![Boolean field options](../images/cpq-txn-mgr-boolean-field-options.jpeg)

The Default Access field allows you to modify the access to this field in the Default View. You can make this field Read/Write accessible by choosing Editable as the access, you can set the field access to Read-Only, which means that the field will be visible on the buyside Layout but you will not be able to modify the field value directly, or you can set the field access to No Access which means that the field will be hidden from view on the buyside Layout and will not be accessible via APIs.

![Relationship access screen](../images/cpq-txn-mgr-fields-default-access.jpeg)

The default value for a Boolean field is either True or False. The Default Checked toggle determines whether the Boolean field is set to True or False as its default value.

The True Label field allows you to set the text value of the field when the Boolean value is True \(for example, you might set the True Value to “Yes”\). The False Label allows you to set the text value of the Boolean field when the field value is False \(for example, you might set the False Value to “No”\).

![Boolean field options](../images/cpq-txn-mgr-boolean-true-label.jpeg)

![Field label](../images/cpq-txn-mgr-boolean-false-label.jpeg)

## Picklist field options

In the top left portion of the Field Editor page you will see the Name and Variable Name you created in the New Field page. You can change the Name Value, but the Variable Name value is locked in and can only be changed if you delete the field and re-add it to the Bleuprint. You can add a Description of the field and there is a Required toggle you can set if the field is to be a required field on the buyside Layout.

![Field summary](../images/cpq-txn-mgr-picklist-field-options.jpeg)

The Default Access field allows you to modify the access to this field in the Default View. You can make this field Read/Write accessible by choosing Editable as the access, you can set the field access to Read-Only, which means that the field will be visible on the buyside Layout but you will not be able to modify the field value directly, or you can set the field access to No Access which means that the field will be hidden from view on the buyside Layout and will not be accessible via APIs.

![Relationships editable screen](../images/cpq-txn-mgr-fields-default-access.jpeg)

The Selection Type option allows you to define the Picklist as either a Single Select menu or a Multi Select menu.

The Comparison Type option allows to determine how the value of the menu option will be treated when it is used in some form of comparison situation. Will the menu option be treated as a Text value or a Number value for comparison purposes.

The + Picklist Option link allows you to add the first menu option to this Picklist menu field.

![Selection type screen](../images/cpq-txn-mgr-picklist-selection-type.jpeg)

When adding a Picklist \(Menu\) Option, you need to consider the following field values:

![Selection type screen](../images/cpq-txn-mgr-picklist-selection-type-values.jpeg)

Order: This numeric field allows you to determine the order of the menu options in the menu. The lower the number the higher the place in the menu. It is recommended that you leave some room between the Order values to better facilitate menu maintenance down the road. Instead of numbering your menu options 1-5, number them 10, 20, 30, 40, 50. This leaves numerical room in the order sequence if you have to add new menu items into the menu later on.

Option Label: This is the display name of the menu option, the value that the buyside user will see displayed on the Transaction Manager Layout.

Option Value: This is the variable name of the menu option, this is the value that the ServiceNow CPQ software will use to identify this menu option in the menu.

Selected: This toggle allows you to determine if any of the menu options should be the default value for the menu.

Description: This field allows you to add a description of the menu option.

Image URL: This field allows you to enter the URL location of a graphic image that you would like to use in the menu to create an image menu instead of a text menu.

Once the necessary information is entered click **Save Option** to add this menu option to the list of options for this Picklist field. Use the +Add Option button that appears above the list of menu options to the right, to add additional menu options to the menu.

## Date/time field options

In the top left portion of the Field Editor page you will see the Name and Variable Name you created in the New Field page. You can change the Name Value, but the Variable Name value is locked in and can only be changed if you delete the field and re-add it to the Blueprint. You can add a Description of the field and there is a Required toggle you can set if the field is to be a required field on the buyside Layout.

![Field summary screen](../images/cpq-txn-mgr-date-time-options.jpeg)

The Default Access field allows you to modify the access to this field in the Default View. You can make this field Read/Write accessible by choosing Editable as the access, you can set the field access to Read-Only, which means that the field will be visible on the buyside Layout but you will not be able to modify the field value directly, or you can set the field access to No Access which means that the field will be hidden from view on the buyside Layout and will not be accessible via APIs.

![Relationship access screen](../images/cpq-txn-mgr-fields-default-access.jpeg)

The Default Value field allows you set the default date and time setting for the Date/Time field. The value will be converted to UTC timezone and Zulu format \( YYYY-MM-DDTHH:MM:SSZ\)

![Date time fieldoptions](../images/cpq-txn-mgr-date-time-default-value.jpeg)

The Not Before and Not After fields allow you to set the minimum and maximum date/time values for this Date/Time field.

![Userinterface](../images/cpq-txn-mgr-date-time-not-before-after.jpeg)

For additional information on the Date/Time field type, see [Transaction Manager: Date and Time Fields](transaction-manager-date-and-time-fields.md).

**Related topics**  


[Transaction Manager](transaction-manager.md)

[Transaction Manager: Transaction-level system fields](transaction-manager-transaction-header-level-system-fields.md)

[Transaction Manager: Line-level system fields](transaction-manager-line-level-system-fields.md)

[Transaction Manager: Date and Time Fields](transaction-manager-date-and-time-fields.md)

