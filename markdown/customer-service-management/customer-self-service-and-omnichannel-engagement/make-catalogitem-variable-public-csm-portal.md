---
title: Enable public access for a catalog item variable and variable set
description: Configure input variables and variable sets to be displayed on the submit form. Enable guest users to access these items.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enable public access for a catalog item, Submit catalog item as a guest, Configure the Customer and Consumer Service Portals, Set up self-service, Configure, Customer Service Management]
---

# Enable public access for a catalog item variable and variable set

Configure input variables and variable sets to be displayed on the submit form. Enable guest users to access these items.

## Before you begin

Role required: catalog\_admin

## About this task

The following video demonstrates the process of enabling public access for a catalog item variable and variable set.Enable public access for a catalog item variable and variable set. 

## Procedure

1.  Find the catalog items.

    1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**.

    2.  Search and select the required item.

2.  Make all available catalog item variables public.

    1.  Select the **Variable** related list.

    2.  Open a variable.

    3.  Select **Permission**.

    4.  Select the pencil icon \(![edit user role icon](../image/edit-new.png)\) for **Create roles**.

        ![Showing the create role under permission tab](../image/variables-create-roles.png)

    5.  In the Create Roles pop-up window, search and move **public** from Available to Selected.

    6.  Select **Done**.

    7.  Select **Update**.

    A single catalog item variable is public. Repeat these steps to make other catalog item variables public.

3.  Make catalog item variable sets public.

    1.  Select the **Variable Sets** related list.

        For more information about variable sets, see [Service catalog variable sets](https://www.servicenow.com/docs/access?context=c_ServiceCatalogVariableSets&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

    2.  Open a variable set.

        The Variable Set page opens.

    3.  From the **Variables** tab, open a variable.

    4.  Select **Permissions**.

    5.  Select the pencil icon \(![edit user role icon](../image/edit-new.png)\) for **Create roles**.

    6.  In the Create Roles pop-up window, search and move **public** from Available to Selected.

    7.  Select **Done**.

    8.  Select **Update**.

    A single catalog item variable set is public. Repeat these steps to make other catalog item variable sets public.

4.  Select **Update**.


## Result

The variables and variable sets used to display catalog item fields are made public.

**Parent Topic:**[Enable public access for a catalog item](make-item-public-csm-portal.md)

