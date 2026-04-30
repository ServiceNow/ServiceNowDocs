---
title: Tech Product Support Case table
description: The Technology Product Support Case application adds the Tech Product Support Case \(sn\_tech\_product\_support\_case\) table.
locale: en-US
release: yokohama
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Technology Product Support Case application, Proactive Service Experience Workflows]
---

# Tech Product Support Case table

The Technology Product Support Case application adds the Tech Product Support Case \(sn\_tech\_product\_support\_case\) table.

<table id="table_kbz_1nf_n1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account

</td><td>

The name of the contact's company. This field is filled in automatically if the information is available in the contact record.

</td></tr><tr><td>

Action status

</td><td>

Identifies cases that need attention or that are blocked.

</td></tr><tr><td>

Additional comments

</td><td>

Customer-viewable comments. Each comment is inserted into the **Activity** field when the user selects the Post button.

</td></tr><tr><td>

Assigned to

</td><td>

The assigned agent. If a group is selected in the **Assignment group** field, the assigned agent must belong to this group.

</td></tr><tr><td>

Assignment group

</td><td>

The assigned customer service agent group.

</td></tr><tr><td>

Channel

</td><td>

The method by which the customer initiated contact and the case was opened. For example, chat or email.

</td></tr><tr><td>

Closed

</td><td>

The date and time that the case was closed.

</td></tr><tr><td>

Closed by

</td><td>

The name of the user who closed the case.

</td></tr><tr><td>

Close notes

</td><td>

Additional notes made by the user who closes the case.

</td></tr><tr><td>

Company

</td><td>

The name of the company for this case.

</td></tr><tr><td>

Contact

</td><td>

The name of the customer contact for this case.

</td></tr><tr><td>

Contract

</td><td>

The contract number associated with this case.

</td></tr><tr><td>

Created

</td><td>

The date and time that the case was created.

</td></tr><tr><td>

Created by

</td><td>

The name of the user who created the case.

</td></tr><tr><td>

Entitlement

</td><td>

The entitlement associated with this case.The available entitlements are filtered by the settings in the **Account**, **Contract**, **Product**, **Asset** fields.

</td></tr><tr><td>

Follow the sun

</td><td>

A check box to indicate that a case should be handed-off at the end of the work day for global follow-up.

</td></tr><tr><td>

Initial response

</td><td>

The first response sent by the agent to the customer.

</td></tr><tr><td>

Install base

</td><td>

The Install base field helps you track which products and services have been purchased by a customer, how they have been installed or provisioned, along with the detailed configuration for each installed item.

</td></tr><tr><td>

Issue summary

</td><td>

A summary of the case based on the agent's understanding of the reported issue.

</td></tr><tr><td>

Knowledge

</td><td>

If checked, the system automatically creates a draft knowledge article when the case is closed.

</td></tr><tr><td>

Last action plan updated

</td><td>

Indicates when the technical action plan was last updated.

</td></tr><tr><td>

Last action plan updated by

</td><td>

The user who last updated the technical action plan.

</td></tr><tr><td>

Needs attention

</td><td>

If enabled, the case record needs attention. For example, cases that have been updated by customers or internal users and are waiting for input or review.

</td></tr><tr><td>

Next steps

</td><td>

Stores the next steps to be taken toward case resolution.

</td></tr><tr><td>

Number

</td><td>

The auto generated case number.

</td></tr><tr><td>

Opened

</td><td>

The date and time that the case was opened.

</td></tr><tr><td>

Opened by

</td><td>

The name of the user who created the case.

</td></tr><tr><td>

Parent

</td><td>

The parent record for the case.

</td></tr><tr><td>

Partner

</td><td>

The name of the partner company.

</td></tr><tr><td>

Partner Contact

</td><td>

The name of the partner contact for this case.

</td></tr><tr><td>

Priority

</td><td>

The assigned priority for the case:-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low

</td></tr><tr><td>

Product

</td><td>

The product model of the asset. A model is a specific version or configuration of an asset.The product can be one of the following types: Application model or Service Product model.

Application models and Service Product models can have multiple components. They can also have multiple application, software, and software license combinations.

</td></tr><tr><td>

Product component

</td><td>

Displays a list of the child components for the product selected in the **Product** field.Users with the admin role can configure product components using the following related lists:

-   Service Model form &gt; Model Components related list
-   Application Model form &gt; Model Components related list

</td></tr><tr><td>

Resolution code

</td><td>

Choice list indicating the resolution states for the case.This field is mandatory when an agent proposes a solution for a case.

</td></tr><tr><td>

Resolution notes

</td><td>

Details about how the case was closed. This field is mandatory if a customer service agent or agent manager closes a case. If a customer closes a case, it is not mandatory.

</td></tr><tr><td>

Resolved

</td><td>

The date and time that the case was resolved.

</td></tr><tr><td>

Resolved by

</td><td>

The agent to whom the case is assigned when the case is resolved.

</td></tr><tr><td>

Root cause code

</td><td>

The reason that the case was created.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the issue or problem.

</td></tr><tr><td>

Sold Product

</td><td>

The product that the case is being created for.

</td></tr><tr><td>

Steps to reproduce

</td><td>

Includes details of the steps to follow to reproduce the issue.

</td></tr><tr><td>

Updated

</td><td>

The date and time that the case was updated.

</td></tr><tr><td>

Updated by

</td><td>

The name of the user who last updated the case.

</td></tr><tr><td>

Watch list

</td><td>

Users who receive notifications about this case when additional comments are added or if the state of a case is changed to Resolved or Closed.

</td></tr><tr><td>

Work notes

</td><td>

Information about how to resolve the case, or steps taken to resolve it, if applicable.Internal users who have been added to the Work notes list receive the Case work notes added notification containing the work notes when added.

</td></tr><tr><td>

Work notes list

</td><td>

Users who receive notifications about this case when work notes are added.

</td></tr></tbody>
</table>