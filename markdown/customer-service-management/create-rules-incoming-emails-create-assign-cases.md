---
title: Creating rules for incoming emails that create and assign cases
description: Create your email-related business processes using Inbound Email Flows. After you receive an email on a specified support email address, you can define rules to create cases and assign the cases to specific teams.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Email to case, Configuring the email channel, Configure communication channels, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Creating rules for incoming emails that create and assign cases

Create your email-related business processes using Inbound Email Flows. After you receive an email on a specified support email address, you can define rules to create cases and assign the cases to specific teams.

In previous releases, incoming emails were processed through inbound email actions. Admins created separate email actions to support different business flows using scripts.

**Inbound Email Flows** provide powerful configuration capabilities to manage emails along with your customer service processes through a visual Flow Designer interface. Business managers can define inbound email flows without having to depend on admins or developers to write complex scripts. Email flows use conditional logic to incorporate multiple business processes in one flow.

**Note:** The **Email conditions** under the **Inbound Email** trigger are case-sensitive. Review your flow designer conditions and consider lowercase and uppercase options depending on how the sender puts the email address in the headers.

The following example email flows are available by default after you activate the Customer Service Management plugin. Enable the email flows for activating the email processing rules to automatically create and update cases.

-   Create case from email
-   Update case using Reply

**Note:**

-   The execution order of the inbound email flows takes a higher precedence than inbound actions \(that is if an email flow executes, it avoids execution of inbound actions\).
-   The user who sends an email should have the necessary roles to perform operations specified in the flow, or else the operation stops while executing.

The following example email flows are installed with the platform. These flows aren’t required for any of the CSM email processing rules:

-   Handle email replies
-   Logging a problem

**Related topics**  


[Define rules to process incoming emails](../task/define-process-incoming-emails.md)

[Activate Customer Service Management](../task/t_ActivateCustomerService.md)

