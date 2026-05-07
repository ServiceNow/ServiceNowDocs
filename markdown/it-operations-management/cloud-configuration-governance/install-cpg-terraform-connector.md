---
title: Install Cloud Services Catalog Terraform Connector
description: You can install the Cloud Services Catalog Terraform Connector application \(com.sn\_cmp\_terraform\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Cloud Services Catalog Terraform Connector, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Install Cloud Services Catalog Terraform Connector

You can install the Cloud Services Catalog Terraform Connector application \(com.sn\_cmp\_terraform\) if you have the admin role.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Cloud Services Catalog: Terraform Connector](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9b04ffc20b1323002530a387b6673a1d/) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Ensure that Cloud Provisioning and Governance \(com.snc.cloud.mgmt\) application is installed and activated in the ServiceNow AI Platform. For more information, see [Request the Cloud Provisioning and Governance application](../../cloud-management-v2-setup/task/request-plugin-cloud-mgt.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Cloud Services Catalog Terraform Connector application \(com.sn\_cmp\_terraform\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select **Install**.


## What to do next

-   If you want to use Cloud Services Catalog Terraform Connector with Terraform Open Source, [Create a Terraform Open Source config provider](setup-cpg-terraform-connector-for-terraform-open-source.md).
-   If you want to use Cloud Services Catalog Terraform Connector with Terraform Enterprise, [Create a Terraform Enterprise or Terraform Cloud config provider](setup-cpg-terraform-connector-for-terraform-enterprise.md).

