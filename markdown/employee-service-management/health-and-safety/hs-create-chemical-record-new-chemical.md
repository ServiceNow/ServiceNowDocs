---
title: Create a chemical record for a chemical
description: The chemical manager can create a chemical record for the new chemical request that has been approved.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/health-and-safety/hs-create-chemical-record-new-chemical.html
release: australia
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2025-11-27"
reading_time_minutes: 1
breadcrumb: [Chemical management, Use, Health and Safety Environmental Management, Health and Safety, Employee Service Management]
---

# Create a chemical record for a chemical

The chemical manager can create a chemical record for the new chemical request that has been approved.

## Before you begin

Role required: sn\_hs\_chm.manager

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select **Environmental Management** \(\[Omitted image "icon-hs-envt-mgmt.png"\] Alt text: environmental management icon\) icon.

3.  In the **Chemical Requests** list, select the **Approved** tab and select a chemical request record.

4.  In the **Details** related list of the chemical request, select the **Create chemical** button.

5.  In the **Create chemical** form under the **Automatically** tab, the fields **Chemical name**, **Manufacturer**, and **Language** are automatically filled.

    -   The fields are populated automatically because of the integration with the 3E database. If this configuration isn’t done, the **Create chemical** form must be filled manually.
    -   To create chemical manually, use the **Manually** tab, enter the **Chemical name** and then select **Submit**. On the **Create chemical** form, fill in the fields. For more information, see [Chemical form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety/hs-chemical-form.md).
6.  In the **Country** field, select the name of the country.

    Enter the **Part number** that aligns with the 3E service providers if its available.

7.  Select **Submit**.


## Result

When the **Create chemical** form is,

-   Submitted through the **Automatically** tab, the chemical record and its related lists are automatically populated with information from the 3E database. Some fields may not be populated by the service provider and may be empty. Empty fields must be manually updated.
-   Submitted through the **Manually** tab, the chemical record is created with the fields to be filled manually.

The **Chemical hazard identification**, **Chemical ingredients**, **Chemical ingredients**, **Chemical items**, **Risk assessments**, **Documents**, and **Service provider requests** tabs appear for this chemical record.

The new chemical record is added to the **Chemicals** list in the **Environmental Management** list view.

**Parent Topic:**[Chemical management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety/hs-using-chemical-management.md)

