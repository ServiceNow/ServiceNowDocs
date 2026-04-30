---
title: Activate Customer Service Problem Management
description: Activate the Customer Service Problem Management plugin \(sn\_sprb\_mgmt\) for Customer Service Problem Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and activate related ServiceNow Store applications and plugins if they aren't already installed.
locale: en-US
release: zurich
product: Customer Service Problem Management
classification: customer-service-problem-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Customer Service Problem Management]
---

# Activate Customer Service Problem Management

Activate the Customer Service Problem Management plugin \(sn\_sprb\_mgmt\) for Customer Service Problem Management if you have the admin role. The application includes demo data and activate related ServiceNow® Store applications and plugins if they aren't already installed.

## Before you begin

Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

-   Role required: admin
-   Plugins required: The following plugins must have been installed:
    -   Service Test Management \(sn\_st\_mgmt\)
    -   Customer Service \(com.sn\_customerservice\)
    -   Customer Service Case Types \(com.snc.csm\_case\_types\)
    -   Playbook Experience Core \(com.glide.playbook\_experience.config\)
    -   ServiceNow Integration Hub Starter Pack Installer \(com.glide.hub.integrations\)
    -   playbook for Customer Service Problem Management \(sn\_csm\_playbook\)
    -   Application spoke selector \(sn\_appss\)
    -   Telecommunications, Media, and Technology Core \(sn\_tmt\_core\)
    -   Product Inventory Advanced \(sn\_prd\_invt\)
    -   Telecommunication Open APIs \(com.sn\_tmf\_api\)

## About this task

The following items are installed with Customer Service Problem Management:

-   Roles
-   Tables
-   Properties

For more information, see [Components installed with Customer Service Problem Management](../reference/spm-components.md) and [Customer Service Problem Management properties](../reference/cspm-properties.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Customer Service Problem Management application \(sn\_sprb\_mgmt\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    All dependent plugins and applications that are included, or must be installed are listed in the dialog box.

4.  If demo data is available and you want to install it, select **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

5.  Select **Install**.


