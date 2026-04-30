---
title: Create and activate custom policies for Security Posture Control
description: Create your own custom policies to monitor assets for tool coverage and other high-risk combinations.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use the workspace, Security Posture Control, Security Operations]
---

# Create and activate custom policies for Security Posture Control

Create your own custom policies to monitor assets for tool coverage and other high-risk combinations.

## Before you begin

To help you understand the steps required to create a policy with more details, refer to [Examples of base, child, and cloned policies for Security Posture Control](../concept/spc-policy-examples.md). The examples walk you through the steps required to create a base policy, use the base policy to create a child policy, and clone a policy.

For example policies, see [Examples of base, child, and cloned policies for Security Posture Control](../concept/spc-policy-examples.md).

Roles required: SPC Admin Group or SPC Analyst Group

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Posture Control** &gt; **List** &gt; **Policies** &gt; **All**.

2.  Select **New policy**.

3.  Select the pencil icon next to the name at the top to modify the metadata.

    Fill out the fields.

<table id="table_yhl_pc1_3yb"><tbody><tr><td>

Field 

</td><td>

Description 

</td></tr><tr><td>

Name 

</td><td>

A unique name for your policy. 

</td></tr><tr><td>

Criticality 

</td><td>

Select one from the list. 

</td></tr><tr><td>

Short description 

</td><td>

A unique description for your policy. 

</td></tr></tbody>
</table>4.  Select **Save metadata**.

5.  For Asset type select on from the list.

    |Entity option|Entity description|
    |-------------|------------------|
    |**Hardware**|Locate IP devices that include personal computing devices, cloud virtual machines, servers, network devices, and other hardware.|
    |**Software**|Locate installed software on devices reported by from SGCs and your vulnerability scanners.|

6.  Choose none, one or both.

    |Option|Description|
    |------|-----------|
    |**Base policy**|The conditions of your base policy choice are inherited in the new policy.|
    |**Exclusion policies**|Select any policies you want to exclude from the asset findings for this policy. Any findings from these policies are ignored.|

    The Connection and Entity fields are displayed.

7.  Select one from the list for the Connection field.

    The target Entity field is auto populated based on your choice. A new Criteria field is displayed along with Property, Operator, and Value fields. For more information about asset types and the schema for relationships, see [Policies for Security Posture Control](../concept/spc-policies-overview.md).

8.  Select one from the list for Property.

9.  Select **Category** or **Source**.

10. Select an operator and enter a connector category, for example, Endpoint management, or a category product name \(source\).

11. Use the condition builder and add more conditions or condition sets.

    You navigate from the top-level asset types for hardware and software to their secondary entities by using the condition builder. Depending on your choices, fields are displayed for you and you modify or add criteria.

    The AND, OR decorators in the condition builder permit you to set up the logic for the returned data you want returned for the policy. Refer to the following table and image for more information.

    |Decorator|Description|Number referenced in the image|
    |---------|-----------|------------------------------|
    |Select **AND** next to the top-most Connection and Entity fields for new set of conditions.|Adds a logical AND between the current Connection-Entity criteria, and new criteria from another Connection-Entity.|1|
    |Select **AND** to the right of a Criteria or Property field for new set of Criteria and Property conditions.|Adds a logical AND between the current Connection-Entity criteria, and a new criteria under the same Connection-Entity.|2|
    |Select **OR/AND** to the right of a Property field for new set of Property conditions.|Adds a logical OR/AND between current Property, and a new Property from the same Connection-Entity-Criteria.|3|
    |Select **+ New condition set** for a new set of conditions.|Adds a logical OR between the Condition Set of all current Criteria, and a new Condition Set.|4|

    ![Decorators in the security posture control policy builder](../image/spc-decorators.png)

12. Select **Save policy** after you are done editing.

    Your policy is saved. You can choose to activate it now or return later to activate it.

13. From the more options menu next to **Save policy**, select configure findings.

14. Fill in the fields.

<table id="table_awh_fkm_dcc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Generate findings for this policy?

</td><td>

Choose **Yes** to generate findings for matching assets. After data is imported, select View finds is displayed on the policy record.

 Choose **No** if you don't want to generate findings.

</td></tr><tr><td>

Configure assignment rules

</td><td>

Select the link to set up assignment rules to assign findings for remediation in the Configuration Compliance application. There is a default assignment rule in the \[sn\_vulc\_assignment\_rule\_list\] table you can use in Configuration Compliance.

</td></tr></tbody>
</table>15. Select **Save configuration**.

    After you save and activate a policy, it evaluates the imported data from the service graph connector scheduled in the next run. If you want to display the data on the Configured insights dashboard in the workspace, you must create a New insight in the Custom insight builder module. After you activate the configured insight, its data is displayed on the Configured insights dashboard in the workspace.


