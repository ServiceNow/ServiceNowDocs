---
title: Close an email interaction
description: Close the email interaction after the customer accepts the resolution. The email interaction also automatically closes due to customer inactivity.Close an email interaction after receiving the customer’s confirmation of the resolution.An email interaction gets closed automatically when there’s no response from the customer within a certain period. By default, the period of inactivity is set to a value of five days.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Email Interaction for CSM, Email Interaction for CSM, Email Interaction for CSM]
breadcrumb: [Engaging with the customer using email interaction, Using Email Interaction for Customer Service Management, Customer communication, Using Customer Service Management, Customer Service Management]
---

# Close an email interaction

Close the email interaction after the customer accepts the resolution. The email interaction also automatically closes due to customer inactivity.

## Close an email interaction after the customer accepts a resolution

Close an email interaction after receiving the customer’s confirmation of the resolution.

### Before you begin

Role required: sn\_customerservice\_agent, or sn\_customerservice\_manager

### Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon \(![List icon](../image/List_icon.jpg)\).

3.  In the Interactions section, select **My Interactions**.

4.  Open an email interaction.

5.  Select **Close**.


### Result

The email interaction is closed and marked as Closed Complete.

## Closing an email interaction due to customer inactivity

An email interaction gets closed automatically when there’s no response from the customer within a certain period. By default, the period of inactivity is set to a value of five days.

If a consumer, contact, or guest user doesn’t respond within five days, the email interaction automatically closes. Any subsequent email from the customer creates an email interaction. For more information on configuring the inactivity period property, see [System properties for configuring Email Interaction](../reference/system-properties-for-configuring-email-as-an-interaction.md).

When a customer replies on top of a closed email interaction, a new email interaction is created and linked to the closed interaction.

