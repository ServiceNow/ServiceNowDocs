---
title: Configure the product home page
description: Track delta changes, over-allocated subscriptions, customizations, and slow execution on the product home page by selecting a product family
locale: en-US
release: zurich
product: Admin Center
classification: admin-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Admin Center, Get started, Administer]
---

# Configure the product home page

Track delta changes, over-allocated subscriptions, customizations, and slow execution on the product home page by selecting a product family

## Before you begin

Role required: admin

## Procedure

1.  Access Configuration Hub in one of the following ways.

    |Option|Steps|
    |------|-----|
    |**Using left navigation**|Navigate to **All** &gt; **Admin Center** &gt; **Configuration Hub**.|
    |**Using Admin tab option**|Navigate to **Admin** &gt; **Configuration Hub**.|

2.  Select one of the product families as per your requirement.

    The product home page shows up.![App engine screen.](../image/ac-product-home-page-details.png)

3.  Track the following activities in the Overview tab.

    -   Change in total errors: Weekly delta change in errors
    -   Subscriptions that need review: Number of licenses that have been over-allocated
    -   Customizations: Total modified files related to the installed applications within the selected product family.

        **Note:** The number mentioned under the total customizations is the number of files that have been modified recently within last 7 days.

    -   Slow execution: The number of slow transactions, events and scripts on the instance.
    By default, the core applications are hidden. Core applications are installed by default as you upgrade your instance. You can’t uninstall the core applications. But you can use the toggle to show all the applications including the core apps.

    **Note:** It is recommended not to modify the core applications and its functionality so that during an upgrade you don't have too many skipped files.

    Select **See details** to read more about the store applications that have been installed. Select **Explore files** to list the records in the selected application of the product.

4.  Drill down to a particular application by selecting the **Explore** tab.

    **Note:** The first time the **Explore** option is loaded, it takes in all the applications displayed in the **Overview** section.

    ![Explore tab.](../image/ac-explore-files.png)You can do the following in the Explore tab:

    -   Search for table names, sys\_id, or relevant records in the Configuration tables search bar.

        **Note:** You can also display the files as per machine names.

    -   Select a particular table from the left navigation bar and all the records in that table show up.

        **Note:** The number mentioned next to the table name is the number of records in that table. The records also satisfy the Applications in filter. You can also save your table preference by pinning the required tables.

    -   You can make edits in the records directly within Configuration Hub. You don't have to open the records in a conventional way to make edits in them.

**Parent Topic:**[Configuration Hub](../concept/ac-configuration-hub.md)

