---
title: Create an asset search in Security Posture Control
description: Set your conditions and search for assets by specific service graph connector products or for assets that have specific data reported by a connector.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use the workspace, Security Posture Control, Security Operations]
---

# Create an asset search in Security Posture Control

Set your conditions and search for assets by specific service graph connector products or for assets that have specific data reported by a connector.

## Before you begin

As an example search, say you want to identify your assets that have Windows servers and a specific version found in CrowdStrike metadata details.

Roles required: SPC Admin Group or SPC Analyst Group

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Posture Control** &gt; **Asset search**.

2.  Choose one.

    |Option|Description|
    |------|-----------|
    |**Hardware Asset**|Search for any device that includes personal computing devices, servers, network devices, cloud virtual machines, and other hardware.|
    |**Software**|Search for installed software on your assets reported by service graph connectors, your vulnerability scanner products, and the software reported by scanners that is already accounted for in Software Asset Management \(SAM\) and other ServiceNow products.|

    For this example, select **Hardware Asset** for Asset type.

3.  Select **Base policy** and **Exclusion policies** if you want to use an existing policy's conditions as a start and you want to exclude assets that match existing policies, respectively.

    The policies you select are displayed.

4.  Select **With connector data** for the Connection field.

5.  Select **CrowdStrike Device Details** for the Entity.

6.  For Property, Operator, and Value, select **\[Agent Version\]\[is\]** and enter the version, for example, **6.26.14003.0**.

7.  Select the and operator to the right of the Entity field with CrowdStrike Device Details as the value for another condition.

8.  Select **With CMDB metadata** for the Connection field.

    The Entity field is populated with CMDB Metadata.

9.  Select **Property** for the Criteria field.

10. For Property, Operator, and Value, select **\[OS\]\[contains\]** and enter **Windows server**.

11. Select **View assets**.

    After a few moments, results are displayed on the Matching assets tab. If you see no matches, you can refine your search. After you are satisfied you have set the conditions correctly, you can save the search as a policy and activate it. Like other policies, it searches your assets with a background job continuously after you activate it.


