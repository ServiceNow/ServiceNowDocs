---
title: Configure catalog item script to display confirmation message and redirect the guest user
description: Configure the catalog item script to display a confirmation message and redirect the guest user to homepage or browse catalog page.
locale: en-US
release: zurich
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Enable public access for a catalog item, Submit catalog item as a guest, Configure the Customer and Consumer Service Portals, Set up self-service, Configure, Customer Service Management]
---

# Configure catalog item script to display confirmation message and redirect the guest user

Configure the catalog item script to display a confirmation message and redirect the guest user to homepage or browse catalog page.

## Before you begin

Role required: admin, catalog\_admin

## Procedure

1.  Find the catalog items.

    1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**.

    2.  Search and select the required item.

2.  Make changes to the script.

    1.  Select the **What it will contain** tab and scroll down to the Script section.

        ![showing Script section under what it will contain tab](../image/what-it-will-contain-script.png)

    2.  Paste the following code and update it as per your requirement

        ```
        gs.addInfoMessage("Your case has been submitted"); // Info message to be displayed  
        producer.portal_redirect = "csm?id=csm_sc_category&catalog_id=-1"; // portal page to redirect to
        ```

3.  Select **Update**.


## Result

The catalog item script is configured to display a confirmation message and redirect guest users.

**Parent Topic:**[Enable public access for a catalog item](make-item-public-csm-portal.md)

