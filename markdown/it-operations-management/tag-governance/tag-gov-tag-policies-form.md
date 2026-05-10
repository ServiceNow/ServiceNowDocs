---
title: Tag Policies form
description: You use the Tag Policy form to configure tag compliance and health policies that are used in tag audits runs on discovered cloud resources or CIs.
locale: en-US
release: australia
product: Tag Governance
classification: tag-governance
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Tag Governance reference, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Tag Policies form

You use the Tag Policy form to configure tag compliance and health policies that are used in tag audits runs on discovered cloud resources or CIs.

<table id="table_nwh_ghs_21c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and descriptive name for the policy.

</td></tr><tr><td>

Short Description

</td><td>

A short summary that describes the policy.

</td></tr><tr><td>

Policy Type

</td><td>

Policy type selection for the tag compliance and health audit.-   Tag Count Policy: Check for a specific count of tags for CIs.
-   Tag Key Policy: Check for tags with specific values \(string expressions\).
-   Tag Key &amp; Value Policy: Check for key-value pair and value strings.
-   Tag Category Policy: Check for tags with a specific category.

**Important:** You must work in a leaf domain to use the Tag Category Policy.


Based on your selection, you will specify additional values.

</td></tr><tr><td>

Expected Tag Count

</td><td>

This field appears only when the **Tag Count Policy** policy type is selected.

CIs with fewer tags than the specified number are considered as failed or non-compliant. CIs that meet the value are considered certified against this policy.For example, if you specify `4`, the policy checks whether the CIs have at least four tags specified.

</td></tr><tr><td>

Expected Tag Keys

</td><td>

This field appears only when the **Tag Key Policy** policy type is selected.

Policy that checks discovered CIs for the tags specified in the **Expected Tag Keys** field. Specify multiple tags or string expressions in a comma-separated list.

For example, if you specify `prod,finance,cost center` the policy checks whether the CIs have all the specified tags. CIs that have all the specified tags as certified or fully compliant. If CIs are missing any of the listed tags, they’re considered failed or non-compliant.

</td></tr><tr><td>

Tag Key &amp; Value Checks

</td><td>

Execute this policy to check discovered CIs for the tag key and values specified in the **Tag Keys &amp; Value Checks** field.You can specify multiple tag key &amp; value pairs or specify a script to check for a collection of values.

For example, you can specify `user` in the **Key** field, and `admin` in the **Value** field.**Note:**

The **Script** field appears only when **Tag Key &amp; Value Policy** is selected in the **Policy Type** field. Use the **Script** field to specify multiple values to return a string set.

Example code

```
// The script should
        return a string set to tagValues variable.

         // the code sets the
        tagValues array with name of the CI

        // by this the check will
        be done for the tag to match the CI’s name
  
        tagValues =  [ci.name.toString()];

```

</td></tr><tr><td>

Active

</td><td>

Option to activate or deactivate the run schedule.

</td></tr><tr><td>

Run on cloud events

</td><td>

Option to enable real-time audit runs when cloud events occur. **Note:** Ensure that you have configured auto-updating the CMDB with cloud events for the relevant cloud provider.

</td></tr><tr><td>

Save cert audit result

</td><td>

Option to save the certification audit findings and incorporate tag audit outcomes in a CI's health calculations.**Note:** This option can be activated if there is a business need to incorporate tag audit outcomes in CI health calculations.

</td></tr><tr><td>

Run

</td><td>

Frequency at which the tag audit runs.-   **Daily**
-   **Monthly**
-   **Weekly**
-   **Periodically**
-   **Once**
-   **On Demand**

**Note:**

To run an audit immediately after configuring the policy, select the **On Demand** option.

-   **Business Calendar: Entry Start**
-   **Business Calendar: Entry End**

</td></tr><tr><td>

Next scheduled run date

</td><td>

Date and time on which the tag audit is next scheduled to run.This field appears only for scheduled runs and not for on-demand runs.

</td></tr><tr><td>

Filters

</td><td>

Condition statements with a series of contextually generated fields. Use lookup lists to build conditions and filter the CIs eligible for audit.Dynamic conditions and filters you specify to fetch the desired tags based on service accounts and associated datacenters.

</td></tr><tr><td>

Table

</td><td>

Displays the **Configuration Item \[cmdb\_ci\]** table to which filters are applied.

</td></tr><tr><td>

Policy Criteria

</td><td>

Other policy criteria that you can configure using dynamically populated reference lookup lists. The Configuration Item \[cmdb\_ci\] table populates the data for this lookup list. For more information, see the [Reference lookup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ReferenceLookup.md).

</td></tr><tr><td>

Tag Filter

</td><td>

Filter CIs further based on **Key**, **Keywords**, and **Value** that you specify. Use the condition builder to customize a filter.

</td></tr><tr><td>

Task Assignment

</td><td>

Option to assign follow-on tasks to users or user groups.

</td></tr><tr><td>

Create Tasks

</td><td>

Option to create follow-on tasks.**Note:** If there is an existing task mapped to a CI and tag policy, the **sn\_itom\_tag.allow\_new\_cert\_follow\_on\_task** system property determines whether to create a new task or update an existing one when there is a compliance failure:

-   To update the existing task with the compliance failure details but not create a new task, set the property to false \(default\)
-   To create a new task, set the property to true.

</td></tr><tr><td>

Group

</td><td>

This field appears only when you select the **Create Tasks** check box.

Assignment group to which to assign the task. Use lookup lists to select a group.

</td></tr><tr><td>

User

</td><td>

Specific user from the assignment group to whom you want to assign the task. Use lookup lists to select a user.This field appears only when you select the **Create Tasks** check box.

</td></tr></tbody>
</table>**Parent Topic:**[Tag Governance reference](../../it-operations-management/concept/reference-tag-governance.md)

