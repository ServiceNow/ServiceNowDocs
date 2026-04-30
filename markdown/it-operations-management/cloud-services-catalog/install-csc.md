---
title: Install Cloud Services Catalog
description: You can install the Cloud Services Catalog application purchased from the ServiceNow Store, to make it available on your instance.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application also includes demo data and installs related to ServiceNow applications and plugins, if you don’t have them installed already.
locale: en-US
release: xanadu
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Install Cloud Services Catalog

You can install the Cloud Services Catalog application purchased from the ServiceNow® Store, to make it available on your instance.The application also includes demo data and installs related to ServiceNow applications and plugins, if you don’t have them installed already.

## Before you begin

-   Cloud Services Catalog application from the ServiceNow® Store.
-   Ensure that the application and all of its associated ServiceNow® Store applications have valid ServiceNow entitlements. See [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do?_ga=2.11647988.1191940289.1684662746-560845984.1665559200).

Role required: admin, sn\_appclient.app\_client\_company\_installer \(can only install applications that match the instance company\), or sn\_appclient.app\_client\_user

## About this task

The following items are installed with Cloud Services Catalog:

-   Plugins
-   Out Of Box Catalog
-   Roles

**Tip:**

If you’re an existing user of Cloud Services Catalog or CSC Innovation Labs:

-   An upgrade from the previous version isn’t currently supported. To upgrade an existing instance with Cloud Services Catalog or CSC apps, do the following actions:
-   -   Uninstall the previously installed CSC apps with table clean-ups \(CSC content pack and CSC in order\).
-   Install new CSC apps \(CSC and CSC content pack in the same order\).
-   As you can run Guided Setup only once in an instance, manually place new Terraform templates in the Terraform box and update the Out Of Box Terraform config provider accordingly and run [Discovery](../../discovery/reference/r-discovery.md).

For more information, see the components links.

## Procedure

1.  Navigate to **All** &gt; **System Application** &gt; **All Available Applications** &gt; **All**.

2.  Search for the application by its name or ID.

    If you can't find the application, you might have to request it from the ServiceNow® Store. CSC is available as a separate subscription and requires the Cloud Provisioning and Governance plugin \(com.snc.cloud.mgmt\).

3.  Select a version from the list and select **Install**.

    In the Install dialog box that is displayed, any dependencies that are installed with your application are listed.

4.  If you’re prompted, follow the links to the ServiceNow® Store to get any additional entitlements for dependencies.

5.  Select **Install**.


**Parent Topic:**[Configuring Cloud Services Catalog](configuring-csc.md)

