---
title: Create a Space Recommender rule
description: Define a space recommender rule using which the qualifying spaces must be calculated when a user raises a space assistance request using Workplace Service Portal. You must have Workplace Central plugin.
locale: en-US
release: australia
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Create a Space Recommender rule

Define a space recommender rule using which the qualifying spaces must be calculated when a user raises a space assistance request using Workplace Service Portal. You must have Workplace Central plugin.

## Before you begin

Ensure the following:

-   Workplace Central plugin is installed.
-   Workplace Case Management is installed.
-   Workplace Core is installed.

Role required: sn\_wsd\_core.admin

## About this task

Create space recommender rules and specify the type of rule based on which space results must be calculated. Rule types such as Condition, Advanced script, Ignore blocked spaces and Proximity are available to set for a rule.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Administration** &gt; **Space Recommender Rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_qkt_vgg_cwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rule name

</td><td>

Name of the rule.

</td></tr><tr><td>

Rule type

</td><td>

Type of rule. Select any one of the following options:-   **Condition**: Option to set the rule with conditions. You can select the table on which you want to set the conditions and add conditions that must be met in the rule.
-   **Advanced script**:Option to configure a script to run on the Space table. Ensure that the script returns a query on the Space table.
-   **Ignore blocked spaces**: Option to set the rule to ignore blocked spaces while recommending spaces. By default, the option is set to **Ignore blocked spaces**.
-   **Proximity**: Option to set the rule that the space must be of exact proximity with the specified Cost center or Department. You can specify the location level where you want to implement the proximity.


</td></tr><tr><td>

Active

</td><td>

Option to activate the rule.

</td></tr><tr><td>

**Condition** **Note:** This tab appears only if you select **Condition** in the **Rule type** field.

</td><td>

 

</td></tr><tr><td>

Condition table

</td><td>

Table on which you want to run the conditions.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that you want to run on the table. Select **New criteria** to add multiple conditions.

</td></tr><tr><td>

**Script** **Note:** This tab appears only if you select **Advanced script** in the **Rule type** field.

</td><td>

 

</td></tr><tr><td>

Script

</td><td>

Script that you want to run on the Space table. The script will run on the table and return qualifying spaces. Ensure that the scripts returns a query on the Space table.

</td></tr><tr><td>

**Proximity**

</td><td>

 

</td></tr><tr><td>

Proximity at

</td><td>

Select the location level where the proximity must be implemented.

</td></tr></tbody>
</table>4.  Click **Submit**


## Result

The Space recommender rule is created.

## What to do next

[Add space recommender rules to a space recommender rule set](add-rules-to-space-recommender-rule-set.md)

-   **[Configure a Space Recommender Rule set](configure-space-recommender-rule-sets.md)**  
Create a space recommender rule set consisting multiple rules. The rule set calculates the qualifying spaces when a user submits a space assistance request using the Workplace Service Portal. You must have Workplace Central plugin.
-   **[Add space recommender rules to a space recommender rule set](add-rules-to-space-recommender-rule-set.md)**  
Add rules to a space recommender rule set based on which qualifying spaces must be calculated when a space assistance request is raised using the Workplace Service Portal. A rule set is a collection of rules.

**Parent Topic:**[Managing workplace locations](../concept/Creating-workplace-location-records-using-spce-mgmt.md)

**Related topics**  


[Add a campus](add-a-campus.md)

[Add a building using Workplace Space Management](add-new-building-1.md)

[Add a floor using Workplace Space Management](add-a-floor-1.md)

[Add an area using Workplace Space Management](add-an-area.md)

[Add a room using Workplace Space Management](add-a-room.md)

[Add a space using Workplace Space Management](add-a-space.md)

[Allocate a cost center, department, or workplace entity](add-cost-center-department-floor.md)

[Configure a workspace or desk as flexible or permanent](assign-a-flex-perm-space.md)

[Update the measurement details of a workplace location](update-measurement-details-of-workplace-location.md)

[Change the status of a workplace location](change-active-status-of-workplace-location.md)

[Configure a BOMA type](configure-a-boma-type.md)

[Map a space type with BOMA type](map-a-space-type-with-boma-type.md)

[Raise a space assistance request](raise-a-space-recommendation-request.md)

[Create a view-by configuration](create-view-by-config.md)

[Reviewing allocation changes](../concept/reviewing-allocation-changes.md)

