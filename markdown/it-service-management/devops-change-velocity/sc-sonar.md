---
title: Onboard SonarQube to DevOps Change Velocity — Service Catalog
description: Connect your Sonar instance using the ServiceNow Service Catalog.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SonarQube, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard SonarQube to DevOps Change Velocity — Service Catalog

Connect your Sonar instance using the ServiceNow Service Catalog.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items** and search for DevOps.

    **Note:** You can also access the service catalog from Employee Center or Service portal.

2.  From the DevOps catalog items, select and activate **DevOps App Onboarding** and **DevOps Tool Onboarding**.

3.  After activating, select **DevOps Tool Onboarding** and select **Try it**.

4.  In the DevOps Tool Onboarding form, enter the tool details:

<table id="table_ubw_p1p_gwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tool name

</td><td>

Name for your Sonar integration.

</td></tr><tr><td>

Tool integration

</td><td>

Select SonarQube.

</td></tr><tr><td>

Tool URL

</td><td>

SonarQube/SonarCloud instance URL.For example,https://sonarcloud.io.

</td></tr><tr><td>

Tool password/ Access token

</td><td>

SonarQube user token.

</td></tr><tr><td>

Use MidServer

</td><td>

Optional. Select MID Server for an on-premises tool that is attached to a  MID Server. Application is automatically set to  DevOps and capability is set to REST.

</td></tr></tbody>
</table>5.  Select **Order Now**.

    A request is created. When the request is approved, the tool is connected.


**Parent Topic:**[SonarQube integration with DevOps Change Velocity](../concept/sonarqube-devops-integration-devops.md)

