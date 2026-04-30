---
title: Onboard Agile Development 2.0 to DevOps Change Velocity — Classic
description: Connect to Agile Development 2.0 and discover plans from it.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agile Development 2.0, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Agile Development 2.0 to DevOps Change Velocity — Classic

Connect to Agile Development 2.0 and discover plans from it.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Create a tool record in DevOps to automatically connect to Agile Development 2.0 and get the webhook URL.

    1.  Navigate to **DevOps** &gt; **Tools** &gt; **Create New \(legacy\)**.

    2.  On the form, fill in the fields.

<table id="table_hch_wnb_ymb"><tbody><tr><td>

Tool name

</td><td>

Name of your choice to identify the tool.

</td></tr><tr><td>

Tool Integration

</td><td>

Select **Agile Development 2.0**

</td></tr></tbody>
</table>    3.  Click **Submit**.

2.  On successful tool creation, you're taken to the tool record page.
3.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field on the **Access** tab.

    The tasks the users in the groups can perform depends on the roles assigned to them.

    -   DevOps Tool Owner role: Can view and edit the tool.
    -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
    -   DevOps Administrator role: Can edit all tools.
    -   Other DevOps roles: Can view the tool.
    **Note:** Only groups containing users with DevOps roles are available for selection in the **Maintained by** field.

    The **All App Owners can view and associate tool objects to applications** option becomes available for selection if you choose to restrict access to the tool. This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.

4.  Click **Discover** to discover Products from Agile Development 2.0.

    Discovered records are added to the Plans related list.

5.  Import data for the discovered plans by clicking the **Import** related link from a plan's record.

    Epics, stories, and release versions associated to this plan are listed in the respective related lists.

    -   Work items related list shows stories and defects.

        **Native State** and **Native Type** fields of the work item contain the original state and type values from the source tool.

    -   Plan Versions related list shows releases.
    -   Features related list shows epics.

**Parent Topic:**[Agile Development 2.0 integration with DevOps Change Velocity](../concept/agile-integration-dev-ops.md)

