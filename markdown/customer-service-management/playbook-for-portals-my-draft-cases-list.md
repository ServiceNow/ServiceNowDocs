---
title: View cases in Draft state on the portal
description: Customers can view a list of cases in the Draft state from the Customer and Consumer Service Portals.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up predefined Playbooks for Portals, Playbooks for Portals, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# View cases in Draft state on the portal

Customers can view a list of cases in the Draft state from the Customer and Consumer Service Portals.

When using playbooks on the Customer Service Portal or Consumer Service Portal, customers can view a list of cases in the Draft state by navigating to **Home** &gt; **My Lists** &gt; **My Draft Cases**. Selecting a case in the Draft state returns the user to the playbook intake stage and activities.

## Enabling the Draft state

The Draft state for the base case is shipped as inactive by default. Customers can manually activate the Draft state in the Choice \[sys\_choice\] table.

1.  Navigate to sys\_choice.list.
2.  Select the following record:
    -   **Table** = sn\_customerservice\_case
    -   **Element** = state
    -   **Label** = Draft
3.  Select **Edit**.
4.  Clear the **Inactive** check box.
5.  Select **Update**.

For more information, see [Choice list field type](https://www.servicenow.com/docs/access?context=c_ChoiceLists&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Case draft state values system property

The **sn\_customerservice.case\_draft\_state\_values** system property stores a comma-separated list of values for the Draft state choice list values for the cutomer service base case and case types. The default value for this property is 0.

