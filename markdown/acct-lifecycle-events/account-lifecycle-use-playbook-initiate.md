---
title: Initial setup
description: This phase is meant to gather the initial information required onboard a customer. For example, gathering core information like onboarding manager name, key customer contact, internal and external stakeholders, their responsibilities, and so on.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Set up playbook, Account onboarding, Customer Success Management, Customer Success Management]
---

# Initial setup

This phase is meant to gather the initial information required onboard a customer. For example, gathering core information like onboarding manager name, key customer contact, internal and external stakeholders, their responsibilities, and so on.

<table id="table_ghf_3n4_1yb"><thead><tr><th>

Activity

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Select account

</td><td>

When you select the customer account, a new account onboarding case is generated.**Note:** If the account onboarding case was generated from a case, this field is auto-populated.

Select **Continue** to go to the next activity.

</td></tr><tr><td>

Enter onboarding related info

</td><td>

The next activity in the playbook involves gathering onboarding related information. The required fields to be entered are:-   Assigned to: Select the provider agent who is working on this case.
-   Service Exchange integration: Select one of the following options:
    -   Not required: No Service Exchange integration is required.
    -   Remote catalog: A Service Exchange integration for the remote catalog feature is required.
    -   Remote task: A Service Exchange integration for the remote task feature is required.
    -   Foundation data sync: A Service Exchange integration for the foundation data sync feature is required.
-   Type: Select one of the following:
    -   Phased: A specific part of the onboarding process for this customer is managed through this Customer Success Management onboarding case.
    -   Full: The entire onboarding process for this customer is by this Customer Success Management onboarding case.
-   Specify the Go live date and select **Mark complete** to proceed with the next activity.

**Note:** The State field is set to **New** for a new record. If this field is updated, the Stage field is automatically updated based on the predefined mapping. This mapping is also available for account onboarding case tasks between the Progress and State fields. See [Field mapping for account onboarding cases and case tasks](#section_sm3_qlk_1cc) for details.

</td></tr><tr><td>

Add customer team

</td><td>

Add the customer contacts working on the account onboarding case.

 -   Enter the First name, Last name, Email address and select **Add** to create a customer contact.
-   Select **Mark complete** to move to the next step.

</td></tr><tr><td>

Add customer team responsibilities

</td><td>

Assign responsibilities to each of the customer contacts that have been added.-   Select the Contact that you’ve added in the previous step.
-   In the Responsibility field, select one of the predefined user roles and select **Add** to assign responsibility for the customer contact.
-   Select **Mark complete** to move to the next step.

When this step is completed, two emails are automatically generated. The first email identifies the primary point of contact for the account onboarding case. The second email identifies the key team members participating in the onboarding process.

</td></tr><tr><td>

Add account team

</td><td>

Add and assign responsibilities to the internal team members \(service providers\) working on the account onboarding case. This includes the ServiceNow administrator handling the case. After the account is added, an email is sent to all the team members.-   Select a predefined user role in the **Responsibility** field.
-   Select a user who is assigned this role and select **Add** to assign responsibility to the team member.
-   Select **Mark complete** to move to the next activity.

**Note:** By default, all tasks in the playbook are assigned to the provider's ServiceNow administrator.

</td></tr><tr><td>

Add squad

</td><td>

Add the squad members who will be involved in completing the onboarding case and other activities. This is an optional activity. Select **Mark complete** to move to the next stage.

</td></tr></tbody>
</table>After the Initial Setup stage has been completed, the case information, account, customer, and squad team member information you have added is displayed in the left panel.

## Field mapping for account onboarding cases and case tasks

For account onboarding cases, when the Stage field is updated, the State field is automatically updated based on the mapping shown after this:

|State|Stage|
|-----|-----|
|New|Not started, At risk|
|Unassigned|Not started, At risk|
|Active|On track, At risk|
|Blocked|Paused, At risk|
|Closed|Finished|
|Canceled|Finished|

For account onboarding case tasks, when the State field is updated, the Progress field is automatically updated based on the mapping shown after this:

|State|Progress|
|-----|--------|
|Open|Not started|
|Awaiting customer|Paused, At risk|
|Awaiting internal|Paused, At risk|
|In Progress|On track, At risk|
|Review|On track, At risk|
|Closed|Finished|
|Canceled|Finished|

If you’re using an earlier version of the Customer Success Management application, follow the instructions in [KB1651427](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=87a1689247a34e1077748d01426d4308) to correct the mapping between these fields.

**Parent Topic:**[Set up the account onboarding playbook](account-lifecycle-use-playbook.md)

