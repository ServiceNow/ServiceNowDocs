---
title: Configure picklist extensions
description: Learn how to create and configure picklist extensions \(Picklist extensions\) in ServiceNow CPQ. Add extended option details, apply filters, and map products and quantities to display enriched picklist data in layouts for more dynamic and efficient configurations.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-09-17"
reading_time_minutes: 4
breadcrumb: [ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure picklist extensions

Learn how to create and configure picklist extensions \(Picklist extensions\) in ServiceNow CPQ. Add extended option details, apply filters, and map products and quantities to display enriched picklist data in layouts for more dynamic and efficient configurations.

## Before you begin

1.  Create a single-select or multi-select picklist field for your picklist extension \(example: dogBreed\).
2.  Create a single-select picklist field that you want to use to filter your picklist extension \(example: dogBarking\).

    **Tip:** For prerequisite steps 1 and 2, use Matrix Loader to upload the following two CSV files:

    [dogBreed Fields CSV](https://drive.google.com/file/d/1KtM5z-x50p5r0J8Fl0lLzQKNRzqRVE15/view?usp=sharing)

    [dogBreed FieldOptions CSV](https://drive.google.com/file/d/12NfNlewI7ENs_y4zy1c1VqIz9bGRX1K5/view?usp=sharing)

3.  Create an SFDC Product2 record, such as “Configured Canine”. Make a note of the ID \(the format is a 15-20 character token, similar to 01t5f0000004GBwAAM\) or Product Code, depending on your environment's ProductIdField setting. Define a standard pricebook price to the product record.

In steps 1 through 7 of the procedure, we set up the extension data. In the remaining steps, we map the data.

Role required: Admin

## Procedure

1.  In dogBreed picklist administration, click the Picklist Extension tab, and then click **Guided Setup**.

2.  Click the **Additional option info**, **Filter options**, and **Product Info** tiles, and then click **Next**.![Picklist extensions](../images/cpq-picklist-extensions-ples-2.png)

3.  For each option in the picklist, enter labels for the extended information to show.

    Examples: size, shedding, exerciseReq, biddability, drive, activities.

4.  Filter Options: choose the fields with which you will filter picklist extension.

    Example: Barking/Voice

5.  Product Info: check **Product ID** and **Product Quantity**.

6.  Click **Next**.![Picklist extensions](../images/cpq-picklist-extensions-ples-3.png)

7.  Review the format, and then click `Download CSV Template`.![Picklist extensions](../images/cpq-picklist-extensions-ples-4.png)

8.  Complete the CSV file on your local machine.

    \(If you’re implementing the dogBreed example: leverage the spreadsheet dogBreed picklist extension data; replace ProductId with token or Product Code from prerequisite step 3; and export to CSV format.\)

9.  In the picklist field you are editing, drag the CSV file to Import Extension Data, and then click **Import**.

10. Map the ‘value’ column to ‘Option Reference’.

    This instructs the picklist extension to display defined values of the picklist in the leftmost column. The column that is mapped as the option reference must be named 'value'.

11. Map ‘size’ to ‘Extended Info: “size” as API Payload Key’.

    The corresponding **Available In Layout** checkbox should be automatically checked.

12. Perform the same mapping for the ‘shedding’, ‘exerciseReq’, ‘biddability’, ‘drive’, ‘activities’, and ‘dogBarking’ fields.

    That is, for the ‘shedding’ imported column, map to ‘Extended Info: “shedding” as API Payload Key’, and so on.

13. Map ‘size\_filter’ to the Size \[dogSize\] field.

    This will filter the picklist according to the user’s selection in dogSize.

14. Map ‘shedding\_filter’ to the Shedding \[dogShedding\] field.

15. Map ‘dogBarking\_filter’ to the Barking/Voice \[dogBarking\] field.

16. Map ‘ProductId’ to the Product ID entry with the shopping cart icon, under ‘Set product info’.

    This tells the app to reference the ProductId or Product Code in the picklist extension data to add the corresponding product to the Shopping Cart.

17. Map ‘ProductQuantity’ to the Product Quantity entry with the shopping cart icon, under ‘Set product info’.

    This tells the app to set the quantity of the line item in the cart with this value from the picklist extension upload data.

18. Click **Save Mapping**, and then in the upper right corner, click **Save**.

19. Add the picklist extension field to the layout via the Logik Admin UI or by CSV upload, and deploy.

    For more information, see [Displaying a picklist extension on a layout](../concept/csv_layouts_how_do_i_display_a_picklist_extension.md).![Picklist extensions](../images/cpq-picklist-extensions-ples-5.png)


**Related topics**  


[Adding a field with an extended picklist to the layout](../concept/adding-field-with-extended-picklist-to-layout.md)

[Displaying a picklist extension on a layout](../concept/csv_layouts_how_do_i_display_a_picklist_extension.md)

[Picklists and picklist extensions in rules](../concept/cpq-picklists-and-picklist-extensions-in-rules.md)

