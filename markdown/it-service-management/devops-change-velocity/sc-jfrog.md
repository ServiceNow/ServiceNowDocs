---
title: Onboard JFrog to DevOps Change Velocity — Service Catalog
description: Connect your JFrog instance using the ServiceNow Service Catalog.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [JFrog, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard JFrog to DevOps Change Velocity — Service Catalog

Connect your JFrog instance using the ServiceNow Service Catalog.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items** and search for DevOps.

    **Note:** You can also access the service catalog from Employee Center or Service portal.

2.  From the DevOps catalog items, select and activate **DevOps App Onboarding** and **DevOps Tool Onboarding**.

3.  After activating, select **DevOps Tool Onboarding** and select **Try it**.

4.  In the DevOps Tool Onboarding form, enter the tool details:

    |Field|Description|
    |-----|-----------|
    |Tool name|Name for your JFrog integration.|
    |Tool integration|Select JFrog.|
    |Tool URL|URL of your JFrog instance.|
    |Tool username, password or access token|Login credentials of the global admin for the existing JFrog instance.|
    |Use MidServer|Optional. Select MID Server for an on-premises tool that is attached to a MID Server. Application is automatically set to DevOps  and capability is set to REST.|

    For a list of all the permissions required on the credentials for connecting to JFrog, see JFrog permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

5.  Select **Order Now**.

    A request is created. When the request is approved, the tool is connected.


**Parent Topic:**[JFrog integration with DevOps Change Velocity](../concept/devops-jfrog-integration.md)

