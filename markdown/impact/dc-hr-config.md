---
title: Configure Data Collection for HR
description: Configure Data Collection for HR.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Impact Value Management Data Collection Content Pack for HR, Impact Value Management data collection apps, Configuring Impact, Impact]
---

# Configure Data Collection for HR

Configure Data Collection for HR.

## Before you begin

**Note:** To get the data collection up and running this setup must be done only once.

You need to determine which of your assignment groups are leveraged within the Incident, Change, and Request workflows you consider to be Tier 1 and Tier 2:

-   Tier 1: First-line support, most commonly your helpdesk/service desk group\(s\)
-   Tier 2+: Second- and third-line support, these are your specialist teams as well as potential vendor teams

Role required: admin, pa\_power\_user, pa\_admin, or pa\_data\_collector

## Procedure

1.  Navigate to the **Groups** module in User Administration.

2.  Open the group records to use in the Incident process as the Assignment Group.

3.  Add one of the following types to the record:

    -   Tier 1
    -   Tier 2+
    The type might not show up by default on the group form. Request a system administrator to make the field visible on the form.

4.  Add the **human\_resources** type to the record to set it apart from other tiering groups in other product lines.

5.  Update the record.

6.  Repeat these steps for all potential assignment groups.

    ![Example with Type: Tier 1.](../image/dct_config_1.png)

7.  To validate, run a query against the HR Case table for assignment groups that are still unclassified to validate you have classified all groups.

    ![Query of Assignment.group.Type > does not contain > Tier 1 AND Assignment.group.Type > does not contain > Tier 2+.](../image/dct_config_2.png)

    If your assignment groups change, you will have to reclassify them.

8.  For issues where the Assignment Group field isn't showing Tier 1 or Tier 2 groups in incidents, changes, or requests, ensure that the ITIL type is also added to the group:

    1.  Navigate to **System Security &gt; Users and Groups &gt; Groups**.

    2.  In the Type field, add `itil`.

    3.  Save and update the form.

    4.  Refresh the incident, change, or request form and recheck the Assignment Group.

        The group should now appear.

9.  For the Manual Indicators, add a new data point every month.

    As an example, given the fixed nature of the Impact VM - Legacy HR Systems Annual Run-Rate indicator, you only need to enter this data point once.

    **Important:** If you do not have full access to Performance/Platform Analytics through a Pro or Enterprise subscription, you are required to enter this data point every month.

    1.  Navigate to **Performance/Platform Analytics** &gt; **Scoresheet**, and then select **Impact VM - Legacy HR Systems Annual Run-Rate**.

    2.  Enter the data point in the relevant month cell.

        ![Example with Mar 2024 cell selected with no Indicator score entered.](../image/dct_man_data_points_hr.png)


