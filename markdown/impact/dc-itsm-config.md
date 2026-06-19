---
title: Configure Data Collection for ITSM
description: Configure Data Collection for ITSM.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/dc-itsm-config.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Impact Value Management Data Collection Content Pack for ITSM, Enable data collection for Value Management, Configuring Impact, Impact]
---

# Configure Data Collection for ITSM

Configure Data Collection for ITSM.

## Before you begin

**Note:** To get the data collection up and running, this setup must be done only once.

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

4.  Update the record.

5.  Repeat these steps for all assignment groups.

    \[Omitted image "dct\_config\_1.png"\] Alt text: Example with Type set to Tier 1.

6.  To validate, run a query against the incident table for assignment groups that are still unclassified to validate you have classified all groups.

    \[Omitted image "dct\_config\_2.png"\] Alt text: Query of Assignment.group.Type &gt; does not contain &gt; Tier 1 AND Assignment.group.Type &gt; does not contain &gt; Tier 2+.

    If your assignment groups change, you will have to reclassify them.

7.  For issues where the Assignment Group field isn't showing Tier 1 or Tier 2 groups in incidents, changes, or requests, ensure that the ITIL type is also added to the group:

    1.  Navigate to **System Security** &gt; **Users and Groups** &gt; **Groups**.

    2.  In the Type field, add `itil`.

    3.  Save and update the form.

    4.  Refresh the incident, change, or request form and recheck the Assignment Group.

        The group should now appear.

8.  For the Manual Indicators, add a new data point every month.

    As an example, given the fixed nature of the Impact VM - Legacy ITSM Systems Annual Run-Rate indicator, you only need to enter this data point once.

    **Note:** If you do not have full access to Performance/Platform Analytics through a Pro or Enterprise subscription, you are required to enter this data point every month.

    1.  Navigate to **Performance/Platform Analytics** &gt; **Scoresheet**, and then select **Impact VM - Legacy ITSM Systems Annual Run-Rate**.

    2.  Enter the data point in the relevant month cell.

        \[Omitted image "dct\_man\_data\_points\_itsm.png"\] Alt text: Example with Mar 2024 cell selected with no Indicator score value entered.


