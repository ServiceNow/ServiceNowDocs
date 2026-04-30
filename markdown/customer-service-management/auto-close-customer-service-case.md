---
title: Automatically close customer service cases
description: Customer service cases in the Resolved state can be closed automatically if customers don’t act.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer, Customer Service Management]
---

# Automatically close customer service cases

Customer service cases in the **Resolved** state can be closed automatically if customers don’t act.

This feature uses the **Auto Close Resolved Cases** Flow Designer flow.

**Note:** This flow isn’t active by default.

The **Auto Close Resolved Cases** Flow Designer Flow identifies cases in the **Resolved** state that are waiting for a customer response and takes the following actions:

-   Sends a reminder notification to the customer after five days with no response that the case is pending solution acceptance.
-   Closes the case and sends a reminder notification to the customer after 10 days that the case has been auto-closed.

The notifications are added to the **Additional comments** field on the Case form.

The administrator can enable the **Auto Close Resolved Cases** flow and configure the timing of the reminder notifications. The default settings include two notifications that are sent at 5 days and 10 days after a case has been resolved. The administrator can also create additional notifications to the flow.

The administrator can also create a configuration that enables both the system and agents to exclude cases from auto-closure.

## Using the Auto Close field on the Case form

Customer service agents can use the **Auto Close** field on the Case form to exclude cases from auto-closure. This field is hidden by default. To use this field, configure the Case form to display the **Auto Close** field.

## Configuring business rules for auto closure

The administrator can configure business rules to enable or disable the **Auto Close** field on the Case form.

<table id="table_rm5_g5p_zhb"><thead><tr><th>

Business rule

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mark for Auto Close

</td><td>

Use this business rule to configure when the system sets the **Auto Close** field to true. The default configuration is as follows:-   The case status is Resolved.
-   The **Needs attention** field on the Case form is false.
-   The case isn’t escalated.
-   The account isn’t escalated.

</td></tr><tr><td>

Clear Auto Close

</td><td>

Use this business rule to configure when the system automatically sets the **Auto Close** field to false. By default, the case status returns to **Open** if the solution is rejected.

</td></tr></tbody>
</table>**Related topics**  


[Workflow Studio](https://www.servicenow.com/docs/access?context=flow-designer&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

