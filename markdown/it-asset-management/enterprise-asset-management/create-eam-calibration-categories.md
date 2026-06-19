---
title: Create a calibration category for your enterprise asset calibrations
description: Create a calibration category to indicate the type of calibration that you need to perform on your enterprise assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/create-eam-calibration-categories.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Asset Management, IT Asset Management]
---

# Create a calibration category for your enterprise asset calibrations

Create a calibration category to indicate the type of calibration that you need to perform on your enterprise assets.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## About this task

You can specify the calibrations that are required for your enterprise assets by using calibration attributes. When you create a calibration attribute, you must select a calibration category to indicate the type of calibration that you need to perform. The Enterprise Asset Management application includes default calibration categories such as Electrical, Flow, Humidity, and Pressure. You can create additional calibration categories for any calibrations that do not fall under the default categories.

For more details on calibration attributes, see [Add calibration attributes to an enterprise asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/add-calibration-attributes-enterprise-asset.md) or [Add calibration attributes to an enterprise model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/add-calibration-attributes-enterprise-model.md).

## Procedure

1.  From the Enterprise Asset Workspace, open the Admin center view.

2.  From the left navigation menu of the Admin center view, navigate to **Calibration configuration** &gt; **Category**.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the calibration category.|
    |Description|Detailed description of the calibration category.|

5.  Select **Save**.


## Result

The calibration category is available to use in your calibration attributes.

