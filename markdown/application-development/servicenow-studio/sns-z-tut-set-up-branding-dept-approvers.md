---
title: Set up the Branding department approvers
description: Set up the Branding department approvers on the platform.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tutorial part 1: Begin with an MVP, ServiceNow Studio tutorial, Explore, ServiceNow Studio, Developing your application, Building applications]
---

# Set up the Branding department approvers

Set up the Branding department approvers on the platform.

## Before you begin

Role required: admin or delegated\_developer

## Procedure

1.  Exit ServiceNow Studio and return to the platform.

2.  Select **All** in the Filter Navigator.

3.  Type `sys_user_group.list` in the Filter Navigator search and press the Enter key.

    The Groups List View loads, displaying the existing Groups.

4.  Select **New**.

5.  In the **Name** field, enter `Branding Dept`.

6.  Select and hold \(or right-click\) in the header bar of the form view and select **Save**.

7.  Select the **Group Members** tab.

8.  Add members by selecting **Edit**.

9.  Search for `Users` on the left side of the slush bucket.

10. Use the \[&gt;\] button to select add the following users to the group.

    -   Andrew Och
    -   Beth Anglin
    -   Luke Wilson
11. Select **Save**.

    Next, follow a similar process to add a role.

12. Select the **Roles** tab.

13. Select **Edit**.

14. Search for `*market`.

15. Add the user role from the **Marketing Services** app to the Branding Dept Group.

    Your role may have a slightly different prefix.

    ![Search for and select the marketing department user role.](../image/sns-z-tut-brand-dept.png)

16. Select **Save**.


**Parent Topic:**[ServiceNow Studio tutorial part 1: Begin with an MVP](../concept/sns-z-tutorial-begin-with-mvp.md)

