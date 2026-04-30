---
title: Onboard Checkmarx to DevOps Change Velocity - Service Catalog
description: Connect your Checkmarx instance using the ServiceNow Service Catalog.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Checkmarx, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Checkmarx to DevOps Change Velocity - Service Catalog

Connect your Checkmarx instance using the ServiceNow Service Catalog.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items** and search for DevOps.

    **Note:** You can also access the service catalog from Employee Center or Service portal.

2.  From the DevOps catalog items, select and activate **DevOps Tool Onboarding**.

3.  After activating, select **DevOps Tool Onboarding** and select **Try it**.

4.  In the DevOps Tool Onboarding form, enter the tool details based on whether you are onboarding Checkmarx SAST or Checkmarx One.

    |Field|Description|
    |-----|-----------|
    |Tool name|Name for your Checkmarx integration.|
    |Tool integration|Checkmarx SAST.|
    |Server URL|Base URL of your Checkmarx One intance.|
    |Tool username/ API ID|API ID of your Checkmarx instance.|
    |Tool password/ Access token / API Key|API key of your Checkmarx instance.|
    |MID server|MID server associated with the Checkmarx One instance.|

    |Field|Description|
    |-----|-----------|
    |Tool name|Name for your Checkmarx integration.|
    |Tool integration|Checkmarx One.|
    |CheckmarxOne Access Control Base URL|Access Control Base URL of your Checkmarx One instance.|
    |CheckmarxOne API Base URL.|API Base URL of your Checkmarx One instance.|
    |Tenant|Name of your Checkmarx One tenant account.|
    |Client Id|Name you used to store your Checkmarx Client ID in your repository.|
    |Client Secret|Name you used to store your Checkmarx Secret in your repository.|

    Ensure that your Checkmarx SAST user has a role that has permissions to read **Project** and **Scan Results** to get summary details. For more information, see [Checkmarx documentation](https://checkmarx.atlassian.net/wiki/spaces/KC/pages/1178009601/CxSAST+CxOSA+Roles+and+Permissions+v9.0.0+and+up). Ensure that your Checkmarx One user has the **create-scan** and **manage-project** roles to access Scan summary details. For more information, see [Checkmarx documentation](https://checkmarx.com/resource/documents/en/34965-68603-managing-roles.html).

5.  Select **Order Now**.

    A request is created. When the request is approved, the tool is connected.


## What to do next

[Configure Checkmarx scans on your pipeline](../concept/configure-checkmarx-scans-on-your-pipeline.md)

**Parent Topic:**[Checkmarx integration with DevOps Change Velocity](../concept/checkmarx-integration-with-devops-change-velocity.md)

