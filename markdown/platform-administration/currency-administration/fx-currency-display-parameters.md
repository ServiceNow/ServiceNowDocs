---
title: Identify the FX Currency field and its display parameters
description: Specify the table, and the field within the table \(for example, cost\), that the FX Currency configuration applies to. Then, select the decimal precision and currency display parameters for the field.
locale: en-US
release: xanadu
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configuring FX Currency field behavior, Setting up defaults required for FX Currency use, Configuring currency fields, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Identify the FX Currency field and its display parameters

Specify the table, and the field within the table \(for example, cost\), that the FX Currency configuration applies to. Then, select the decimal precision and currency display parameters for the field.

## Before you begin

Role required: admin, currency\_admin

## Procedure

1.  Navigate to **All** &gt; **System Localization** &gt; **FX Currency Configuration**.

2.  Click **New**.

3.  In the **Table** field, select the table that contains the FX Currency dictionary attribute.

    For example, if you created a custom table that stores transactional information and contains an FX Currency field, select it from the table listing. To learn more about creating tables in an instance, see [Create a table](../../table-administration/task/t_CreateATable.md).

4.  In the **Field** field, select the column with the FX Currency field type.

    For example, if you created a custom table column for entry of the transaction cost, select it from the listing of fields for the table.

5.  Click **Save**.

6.  Click the Display tab.

7.  In the **Display Digits** field, select the number of digits that should appear after the decimal point in lists and reports.

<table id="choicetable_display_digits"><tbody><tr><td id="d178886e131">

**Currency Default**

</td><td>

Number of digits that appear on lists and forms, based on what is appropriate and customary for the specified currency itself. For example:-   USD: Two digits appear after the decimal, for example, 12.33.
-   Dinar: Three digits appear after the decimal, for example, 69.535.
-   Yen: No digits appear after the decimal, because the Yen uses no cents and numbers round to the next latest value. For example, a calculated currency value of 69.535 rounds up to, and appears as, 67 Yen.


</td></tr><tr><td id="d178886e152">

**0–12**

</td><td>

Specific number of digits that should appear after the decimal, with selectable values from 0 through 12. If you select more than 1, it pads the values with zeroes. -   For example, if you select `3`, and the calculated value is 1.1, the currency value appears as 1.100.
-   If you select `5`, this value appears as 1.10000.


</td></tr></tbody>
</table>    **Note:** In a form, FX Currency fields display the number of digits as entered by the user, up to 12 digits in length.

8.  In the **Display Value Currency** field, select what currency value appears in the designated FX Currency field on forms and lists.

<table id="choicetable_display_value_currency"><tbody><tr><td id="d178886e194">

**Use Global Default**

</td><td>

Use the global default you established in the **glide.currency2.display\_value** system property in **System Localization** &gt; **All Properties.**

</td></tr><tr><td id="d178886e215">

**Display As Entered**

</td><td>

Currency value, as entered into the designated FX Currency field. For example, if the user locale is US Dollars, the value appears in Euros if they select the Euro as the currency during an entry session.

</td></tr><tr><td id="d178886e224">

**Display in Session Currency**

</td><td>

Currency value entered into the designated FX Currency field, converted to the session currency. -   For example, if the user locale is the United States, the session currency appears in US Dollars.
-   If the user locale is Japan, the session currency appears in the Yen.
 To learn more about the user locale, see [Locale settings](../concept/locales.md).

</td></tr><tr><td id="d178886e252">

**Display in Reference Currency**

</td><td>

Currency value entered into the designated FX Currency field, converted to the reference currency designated in the **Reference Currency** field in the Reference tab. For example, if you enter the currency amount in Euros, it converts to and appears in US Dollars if that is the designated reference currency. To learn more the reference currency, see [Set the reference currency](fx-currency-set-reference.md).

</td></tr></tbody>
</table>9.  In the **Aggregation Source** field, select the currency type to use when aggregating currency amounts for the designated field on reports.

<table id="choicetable_aggregation_source"><tbody><tr><td id="d178886e289">

**Use Global Default**

</td><td>

Use the global default you established in the **glide.currency2.default\_reference\_currency** property in **System Localization** &gt; **All Properties.**

</td></tr><tr><td id="d178886e310">

**As Entered Values**

</td><td>

Currency values, as entered into the designated FX Currency field. **Note:** If you select this option, you may experience situations where amounts entered in dissimilar currencies can't be aggregated on reports. For example, if you enter currency amounts in US Dollars, Yen, and Euros, the amounts can't be properly aggregated, or may result in erroneous totals.

</td></tr><tr><td id="d178886e322">

**Reference values**

</td><td>

Currency values, as entered into the designated FX Currency field, converted to the reference currency you designate in the **Reference Currency** field in the Reference tab. For example, if you designate USD as the reference currency, values entered into this field convert to the reference currency, regardless of the currency you entered them in. The currency values that appear on reports are the aggregated converted reference values.

</td></tr></tbody>
</table>10. Click **Save**.


**Parent Topic:**[Configuring FX Currency field behavior](../concept/configure-fx-currency-field-behavior.md)

