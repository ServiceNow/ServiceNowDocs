---
title: Computer Telephony demo integration with the Case form
description: Activating the CTI Softphone plugin enables call-related features on the Case form.An incoming call from a customer contact or a consumer can be routed to an available customer service agent.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CTI demo implementation, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Computer Telephony demo integration with the Case form

Activating the CTI Softphone plugin enables call-related features on the Case form.

The customer service or consumer service agent can use the phone icon next to the **Contact** and **Consumer** fields on the Case form to make a phone call. The phone icon appears next to these fields if the entity record has at least one phone field \(ph\_number\) and at least one of those phone fields contains a phone number.

The phone icon is a reference contribution that can be added to any reference field by modifying the dictionary and adding the following attribute: **ref\_contributions=show\_phone\_customer\_service**.

**Note:** If you’re using a third-party provided CTI application, then you can integrate with the show\_phone UI macro to make calls.For more information on UI macros, refer to [UI macros installed with OpenFrame](../reference/r_InstalledWithOpenFrame.md#)

Select the phone icon to call a consumer or contact.

-   If only one phone field is populated, a call is placed to that number.
-   If more than one phone field is populated, a dialog box displays the available numbers. Select the desired number to call and close the dialog box.

![Dialog box displaying mobile and home phone numbers.](../image/SelectPhoneNumber.png "Select Phone Number dialog box")

Incoming and outgoing calls are logged in the Phone Log \[sn\_openframe\_phone\_log\] table. Call details are recorded in the **Activity** field on the Case form and in the **Phone** related list.

## CTI demo integration with case routing

An incoming call from a customer contact or a consumer can be routed to an available customer service agent.

Similar to the other communication channels, incoming calls from customer contacts and consumers can be routed to a specific agent by using matching rules. If an agent is not available, the call can be placed in a queue. After the agent is free, the matching call in the queue with the longest wait time is rerouted to the agent.

Case routing is enabled as an activity in a workflow. In the Call Center demo workflow \(available with the Customer Service CTI Demo Data plugin\), a call is forwarded to an agent after the caller either creates a new case or enters a valid number for an existing case.

If no agents are available, the call goes into a queue and remains there until an agent becomes available. If a call is in the queue for longer than 10 minutes, it is forwarded to voice mail and the caller is asked to leave a message.

**Related topics**  


[Routing and assigning customer service cases](c_CaseRouting.md)

