---
title: Create a catalog request for onboarding multiple assets
description: Create a catalog request for onboarding multiple assets on a single model.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use Service Catalog for requests and flows, Enterprise Asset Management, IT Asset Management]
---

# Create a catalog request for onboarding multiple assets

Create a catalog request for onboarding multiple assets on a single model.

## Before you begin

Role required: enterprise\_asset\_technician

## About this task

A minimum of one asset is required to submit a catalog request. Each catalog request may include a maximum of 50 assets.

## Procedure

1.  Navigate to **Service Portal** &gt; **Request Something** &gt; **Enterprise Asset Lifecycle**.

    You can also navigate to the **Enterprise Asset Lifecycle** via the Service Catalog.

2.  Select **Assets Onboarding**.

    The Asset Onboarding page opens.

3.  On the form, fill in the fields.

<table id="choicetable_isk_ybf_gzb"><thead><tr><th align="left" id="d324600e92">

Field

</th><th align="left" id="d324600e95">

Description

</th></tr></thead><tbody><tr><td id="d324600e101">

**Due by**

</td><td>

Date by when the asset onboarding must be complete.This field is optional.

</td></tr><tr><td id="d324600e112">

**Requested for**

</td><td>

Person for whom the asset is requested.This field is optional.

</td></tr><tr><td id="d324600e123">

**Stockroom**

</td><td>

Select a stockroom for the assets.

</td></tr><tr><td id="d324600e132">

**Is new model?**

</td><td>

Select this check box for a new model you want to create. Once selected, enter the following information.-   Manufacturer
-   Model name
-   Model number
-   Short description
**Note:** The above information is collected for creating a model record. The model record gets created in the Enterprise Asset Workspace.

</td></tr><tr><td id="d324600e161">

**Model**

</td><td>

Select an existing model record for the assets.

</td></tr><tr><td id="d324600e170">

**Add**

</td><td>

Select to enter information for creating new assets. In the Add Row dialog box, enter the following information and then select **Add**:

-   Serial number
-   Asset tag
-   MAC address
-   RFID tag
-   Comments
 To enter another asset, select **Add** again.

 **Note:** The above information is collected for creating an asset. The asset record gets created Enterprise Asset Workspace by the enterprise asset manager.

</td></tr></tbody>
</table>4.  Select **Submit**.

    After the catalog request is submitted, a requested item is created. An asset onboarding task is also created associated to the requested item which triggers the multi-asset playbook.


## What to do next

The enterprise\_asset\_manager role can launch the multi-asset playbook from the Enterprise Asset Workspace.

