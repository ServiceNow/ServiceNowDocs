---
title: Update a Currency Instance record
description: Review and edit the details of a currency entry in an FX Currency field.
locale: en-US
release: australia
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Defaults required for FX Currency use, Configure, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Update a Currency Instance record

Review and edit the details of a currency entry in an FX Currency field.

## Before you begin

Role required: currency\_instance\_admin, with ACL access to the FX Currency field, or admin

## Procedure

1.  Access the Currency Instance record using one of the following methods.

<table id="choicetable_wfb_pcw_5jb"><thead><tr><th align="left" id="d67484e73">

Access method

</th><th align="left" id="d67484e76">

Description

</th></tr></thead><tbody><tr><td id="d67484e82">

**Direct access from an FX Currency field**

</td><td>

Select the edit icon \(![Edit icon](../images/currency-edit.png)\) that appears next to the FX Currency field in a transaction record.

</td></tr><tr><td id="d67484e101">

**From the navigator bar**

</td><td>

1.  Navigate to **System Localization** &gt; **FX Currency Instances**.
2.  Select the Currency Instance record to edit.
 **Note:** Only users with an assigned admin role can access this selection from the navigator.

</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_uyx_ygm_4jb"><thead><tr><th>

**Field**

</th><th>

**Description**

</th></tr></thead><tbody><tr><td>

Amount

</td><td>

Currency amount that you entered into the FX Currency field, formatted according to the currency code in your user locale. The amount stores internally as a currency code and a numerical value of up to 12 digits in length. For example, `USD; 1234.56`. **Note:** The currency value has two parts: the currency amount and a currency code. The amount stores as a decimal value, for example, `1234.56`.

</td></tr><tr><td>

Currency Code

</td><td>

Three-letter ISO code that identifies the currency that you select for the currency amount. For example, USD for the US Dollar, or EUR for the Euro.

</td></tr><tr><td>

Conversion Rate

</td><td>

Conversion rate used to calculate the reference currency value. It converts a session currency value, expressed in one currency, to another, and stores as a reference to a record in the Currency Conversion Rate \[fx\_conversion\_rate\] table. The conversation rate is based on the **Conversion Rate Table** and **Conversion Date Source** settings for the FX Currency field in the Rate tab of FX Currency Configuration. To learn more about these settings, see [Configuring FX Currency field behavior](../concept/configure-fx-currency-field-behavior.md).

 You change or select the conversion rate as needed.

</td></tr><tr><td>

Reference Amount

</td><td>

Calculated reference currency amount. The ServiceNow AI Platform converts the currency value entered into the **Amount** field into a common reference currency. It uses the settings in the **Reference Currency Source** and **Reference Currency** fields in **System Localization** &gt; **FX Currency Configuration** to do so. You can't change the calculated reference amount.

 **Note:** To learn more about reference currencies, see [Set the reference currency](fx-currency-set-reference.md).

</td></tr><tr><td>

Reference Currency Code

</td><td>

Three-letter ISO code that identifies the reference currency, for example, USD, to which the entered currency value converted. You can't change the reference currency code.

</td></tr></tbody>
</table>    **Note:** You can't edit the reference currency and value because they are calculated automatically.

3.  Select **Save**.


**Parent Topic:**[Setting up defaults required for FX Currency use](../concept/setting-up-defaults-fx-currency-use.md)

**Related topics**  


[Add conversion rates using a custom rate table](custom-rate-table.md)

[Configuring FX Currency global settings](fx-currency-configure.md)

[Add an FX Currency field to a table](add-fx-currency-field-table.md)

[Configuring FX Currency field behavior](../concept/configure-fx-currency-field-behavior.md)

