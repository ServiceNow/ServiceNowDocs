---
title: Reduce PPE stock
description: Reduce stock for a Personal Protective Equipment \(PPE\) model to reflect accurate inventory at different locations.
locale: en-US
release: xanadu
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up Workplace PPE Inventory Management, Workplace PPE Inventory Management, Safe Workplace, Health and Safety, Employee Service Management]
---

# Reduce PPE stock

Reduce stock for a Personal Protective Equipment \(PPE\) model to reflect accurate inventory at different locations.

## Before you begin

Role required: sn\_imt\_ppe.ppe\_admin

## Procedure

1.  Navigate to **All** &gt; **PPE Inventory Management** &gt; **Inventory** and select **Reduce consumable stock** or **Reduce hardware stock**.

    **Note:** To reduce PPE stock in the Now Mobile app, navigate to **More** &gt; **PPE Stock** and select **Reduce Consumable Stock** or **Reduce Hardware Stock**.

2.  On the form, fill in the fields.

<table id="table_s1r_1cf_cnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model

</td><td>

The model to remove stock for.

</td></tr><tr><td>

Stockroom

</td><td>

The stockroom where the PPE is located.

</td></tr><tr><td>

Quantity

</td><td>

The number of items to be reduced from stock.**Note:** This field is not available for hardware items. The quantity must be `1` so that each item is tracked with a unique asset tag and serial number.

</td></tr><tr><td>

Asset tag

</td><td>

The asset tag for the item. This field is only visible for hardware models.**Note:** If you enter an asset tag, only the stockrooms that contain the asset appear.

</td></tr><tr><td>

Serial number

</td><td>

The serial number for the item. This field is only available for hardware models.**Note:** If you enter a serial number, only the stockrooms that contain the serial number appear.

</td></tr><tr><td>

Comments

</td><td>

The reason that you're reducing stock.

</td></tr></tbody>
</table>    -   **Hardware stock**

        When reducing hardware models, if the asset tag and model number are not entered, the stock is removed from the stockroom listed first and the amount is set to zero \(0\).

        When a model and asset tag are entered, or if the model and serial number are entered, hardware stock is matched and the amount is set to zero \(0\).

    -   **Consumable stock**

        If you try to enter a quantity larger than the quantity that is in stock, the system does not allow you to proceed.

3.  Click **Submit**.

    The stock log is updated with the PPE stock that you removed. To view the stock log, navigate to **PPE Inventory Management** &gt; **Inventory** &gt; **Stock Log**.


**Parent Topic:**[Set up Workplace PPE Inventory Management](set-up-ppe.md)

**Previous topic:**[Add PPE stock](add-ppe-stock.md)

**Next topic:**[Create stock rules for PPE](create-ppe-stock-rule.md)

