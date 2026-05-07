---
title: Transaction Manager: Fields
description: Understand the five major field type options: text, number, Boolean, picklist, and date/time. Learn how to create new fields using the Admin UI.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Transaction Manager, CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Fields

Understand the five major field type options: text, number, Boolean, picklist, and date/time. Learn how to create new fields using the Admin UI.

In Transaction Manager, administrators are able to create text, number, Boolean, picklist, and date/time fields. Admins also have the choice of creating fields at the transaction level or at the transaction line level.

Fields created at the transaction level sit outside the transaction line grid. These fields commonly contain information about the account, addresses, list price total, total discount, and net total for all line items.

Fields created at the transaction line level sit in the transaction line grid. These can appear as column fields or as fields in the Line Details, Model, and Slide Out UI effects.

The selected level will ultimately impact the field’s availability for rules, which also have a transaction and transaction line level.

In the buyside screenshot below, the sections marked 1 are transaction-level fields; the fields in the section marked 2 are transaction line-level fields.

![Transaction screen](../images/cpq-txn-mgr-fields.jpeg)

## Field types

Transaction Manager provides the following field types.

-   Text
-   Number
-   Boolean
-   Picklist
-   Date/Time

Options for these types are described in the sections that follow.

## System-provided fields

Transaction Manager provides the administrator with a set of system-provided fields that are often used in transaction processing. There are system-provided fields at both the transaction level and the transaction line level.

The system-provided fields provide fields in the following categories:

Transaction level:

-   Pricing information
-   Opportunity information
-   Transaction information
-   Account information

For a complete list of transaction-level fields, see [Transaction Manager: Transaction-level system fields](transaction-manager-transaction-header-level-system-fields.md).

Transaction line level:

-   Pricing information
-   Transaction line information
-   Configuration information
-   Product information
-   Order information

For a complete list of line-level fields, see [Transaction Manager: Line-level system fields](transaction-manager-line-level-system-fields.md).

You can also add custom fields to a blueprint in Transaction Manager. Custom fields added via the Transaction Manager Admin UI are automatically associated with the blueprint. However, custom fields uploaded by using the Matrix Loader must be associated with the blueprint by means of the blueprint.yaml file. To do so, add a list to the blueprint.yaml file that details the field variable names to be associated with the blueprint.

The following sample blueprint.yaml file shows the field associations in the relatedFields section:

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

## Creating a new field using the Admin UI

To add a new field to the Transaction Manager blueprint, follow these steps:

1.  Navigate to the Transaction Manager Admin UI.

2.  Click **Associated Fields**.

    ![Admin transaction](../images/cpq-txn-mgr-associated-fields.jpeg)

3.  Click **Create Field** to create a new field.

    ![Utilities screen](../images/cpq-txn-mgr-create-field.jpeg)

    The **New Field** dialog box opens.

4.  Enter a name in the **Name** field.

    As the name is entered, it is mirrored in the **Variable Name** field. By default, the variable name is the same as the entered name, but in camel case with all spaces and special characters removed. For example, if you enter the name Customer Billing Address, the automatically entered variable name is customerBillingAddress. To create a custom variable name, click the pencil icon to the right of the variable name field and enter your own value.

    ![New field screen](../images/cpq-txn-mgr-fields-select-level.jpeg)

5.  Select a level to choose whether the field is a transaction level field or a transaction line level field.
6.  Choose the type of field you are creating from the five available field types.

    ![Select data type screen](../images/cpq-txn-mgr-fields-select-type.jpeg)

7.  Click **Save**.

The field editor page opens. Select the desired options.

## Text field options

The name and variable name appear at the top left of the field editor page. You can change the name, but the variable name is locked and can be changed only by deleting the field and re-adding it to the blueprint. Optionally, you can add a description of the field here. If the field is to be required on the buyside layout, toggle the **Required** switch.

![Quote name](../images/cpq-txn-mgr-fields-quote-name.jpeg)

The **Default Access** field controls access to this field in the default view. **Editable** makes this field Read/Write accessible. If you select **No Access**, the field is hidden from view on the buyside layout and is not accessible via APIs.

![Relationship access screen](../images/cpq-txn-mgr-fields-default-access.jpeg)

You can enter a default value for the text field in the **Default Value** field.

![Field description](../images/cpq-txn-mgr-text-default-value.jpeg)

The **Minimum Field Length** and **Maximum Field Length** values let you set the minimum and maximum number of characters that can be entered.

![Rules](../images/cpq-txn-mgr-min-max-length.jpeg)

## Number field options

The name and variable name appear at the top left of the field editor page. You can change the name, but the variable name is locked and can be changed only by deleting the field and re-adding it to the blueprint. Optionally, you can add a description of the field here. If the field is to be required on the buyside layout, toggle the **Required** switch.

![Number field options](../images/cpq-txn-mgr-txn-number.jpeg)

The **Default Access** field controls access to this field in the default view. **Editable** makes this field Read/Write accessible. If you select **No Access**, the field is hidden from view on the buyside layout and is not accessible via APIs.

![Relationship access screen](../images/cpq-txn-mgr-fields-default-access.jpeg)

Number fields can take one of three forms: number, currency, or percentage. Choose which form you want the field to take.

The **Unit Label** field lets you specify the unit label for the number field. If the field is for currency, the unit label is the default currency symbol for your CPQ site. If the field is a percentage, the unit label is the percent symbol \(%\).

The **Minimum Value** and **Maximum Value** fields let you set the minimum and maximum allowable values for the field.

![Number field options](../images/cpq-txn-mgr-number-field-options.jpeg)

You can enter a default value for the number field in the **Default Value** field.

## Boolean field options

The name and variable name appear at the top left of the field editor page. You can change the name, but the variable name is locked and can be changed only by deleting the field and re-adding it to the blueprint. Optionally, you can add a description of the field here. If the field is to be required on the buyside layout, toggle the **Required** switch.

![Boolean field options](../images/cpq-txn-mgr-boolean-field-options.jpeg)

The **Default Access** field controls access to this field in the default view. **Editable** makes this field Read/Write accessible. If you select **No Access**, the field is hidden from view on the buyside layout and is not accessible via APIs.

![Relationship access screen](../images/cpq-txn-mgr-fields-default-access.jpeg)

You can set whether the Boolean field defaults to True by setting the **Default Checked** toggle. If the toggle is not set, the field defaults to False.

In the **True Label** field, you can set the text value of the field when the Boolean value is True. For example, you can set the displayed value to “Yes” when the value is True. Similarly, the **False Label** field lets you set the text when the field value is False.

![Boolean field options](../images/cpq-txn-mgr-boolean-true-label.jpeg)

![Field label](../images/cpq-txn-mgr-boolean-false-label.jpeg)

## Picklist field options

The name and variable name appear at the top left of the field editor page. You can change the name, but the variable name is locked and can be changed only by deleting the field and re-adding it to the blueprint. Optionally, you can add a description of the field here. If the field is to be required on the buyside layout, toggle the **Required** switch.

![Field summary](../images/cpq-txn-mgr-picklist-field-options.jpeg)

The **Default Access** field controls access to this field in the default view. **Editable** makes this field Read/Write accessible. If you select **No Access**, the field is hidden from view on the buyside layout and is not accessible via APIs.

![Relationships editable screen](../images/cpq-txn-mgr-fields-default-access.jpeg)

**Selection Type** defines the picklist as either single-select menu or multi-select.

**Comparison Type** lets you determine how the value of the menu option is treated when it is used in a comparison: as a text value or as a number value.

The **+ Add Picklist Options** link allows you to add the first menu option to this picklist menu field.

![Selection type screen](../images/cpq-txn-mgr-picklist-selection-type.jpeg)

When adding a picklist option, consider the following field values:

![Selection type screen](../images/cpq-txn-mgr-picklist-selection-type-values.jpeg)

-   **Order**

    Use this field to determine the order of the menu options in the menu. The lower the number, the higher the place in the menu. As a general guideline, number your menu options 10, 20, 30, 40, and 50 instead of numbering them 1 to 5. This leaves room in the sequence if you new items must be inserted later.

-   **Option Label**

    The option name that the user sees in the Transaction Manager layout.

-   **Option Value**

    The value that CPQ uses to identify this menu option.

-   **Selected**

    Determines whether a menu option is the default menu value.

-   **Description**

    A description of the menu option.

-   **Image URL**

    The URL of a graphic image that can be displayed instead of text.


Click **Save Option** to add the option to the list of options for the picklist field. To add additional menu options, click **+Add Option**.

## Date/Time field options

The name and variable name appear at the top left of the field editor page. You can change the name, but the variable name is locked and can be changed only by deleting the field and re-adding it to the blueprint. Optionally, you can add a description of the field here. If the field is to be required on the buyside layout, toggle the **Required** switch.

![Field summary screen](../images/cpq-txn-mgr-date-time-options.jpeg)

The **Default Access** field controls access to this field in the default view. **Editable** makes this field Read/Write accessible. If you select **No Access**, the field is hidden from view on the buyside layout and is not accessible via APIs.

![Relationship access screen](../images/cpq-txn-mgr-fields-default-access.jpeg)

The **Default Value** field lets you set the default date and time setting for the field. The value is converted to UTC in YYYY-MM-DDTHH:MM:SSZ format.

![Date time fieldoptions](../images/cpq-txn-mgr-date-time-default-value.jpeg)

The **Not Before** and **Not After** fields let you to set the minimum and maximum date and time values for the field.

![Userinterface](../images/cpq-txn-mgr-date-time-not-before-after.jpeg)

For more information about the Date/Time field type, see [Transaction Manager: Date and time fields](transaction-manager-date-and-time-fields.md).

**Related topics**  


[Transaction Manager](transaction-manager.md)

[Transaction Manager: Transaction-level system fields](transaction-manager-transaction-header-level-system-fields.md)

[Transaction Manager: Line-level system fields](transaction-manager-line-level-system-fields.md)

[Transaction Manager: Date and time fields](transaction-manager-date-and-time-fields.md)

