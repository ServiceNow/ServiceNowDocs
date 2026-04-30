---
title: Onboard Veracode to DevOps Change Velocity - Service Catalog
description: Connect your Veracode instance using the ServiceNow Service Catalog.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Veracode, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Veracode to DevOps Change Velocity - Service Catalog

Connect your Veracode instance using the ServiceNow Service Catalog.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items** and search for DevOps.

    **Note:** You can also access the service catalog from Employee Center or Service portal.

2.  From the DevOps catalog items, select and activate **DevOps Tool Onboarding**.

3.  After activating, select **DevOps Tool Onboarding** and select **Try it**.

4.  In the DevOps Tool Onboarding form, enter the tool details:

    |Field|Description|
    |-----|-----------|
    |Tool name|Name for your Veracode integration.|
    |Tool integration|Select Veracode.|
    |Tool username/ API ID|API ID of your Veracode instance.|
    |Tool password/ Access token / API Key|API key of your Veracode instance.|

    **Note:** You must have the Results and Upload and scan API roles for your Veracode credentials. For more information, see [https://docs.veracode.com/r/c\_API\_roles\_details](https://docs.veracode.com/r/c_API_roles_details)

5.  Select **Order Now**.

    A request is created. When the request is approved, the tool is connected.


## What to do next

[Configure Veracode scans on your pipeline](configure-veracode-scans-on-your-pipeline.md)

**Parent Topic:**[Veracode integration with DevOps Change Velocity](../concept/veracode-integration-with-devops-change-velocity.md)

