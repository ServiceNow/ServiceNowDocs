---
title: References for Inbound email
description: Email object variables, user impersonations and inbound actions and examples for processing inbound email actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-platform-administration/references-inbound-email.html
release: zurich
product: AI Platform Administration
classification: ai-platform-administration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Inbound email, Notifications, Configure core features, Administer]
---

# References for Inbound email

Email object variables, user impersonations and inbound actions and examples for processing inbound email actions.

-   **[Accessing email object variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/r_AccessingEmailObjsWithVars.md)**  
An inbound email action script contains the email object to access various pieces of an inbound email through variables. You can use the global variable *sys\_email* with inbound email actions.
-   **[Email user matching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/r_MatchingEmailToExistingUsers.md)**  
When the instance receives an email message, the system searches for an existing user record with the same email address as the sender.
-   **[User impersonations and inbound actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/r_ImpUserRunInboundActions.md)**  
When the instance receives an email, it can take a variety of actions by impersonating the sender.
-   **[Allowing locked out users to process inbound email actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/r_AllowLockedUsersInbdEmailAct.md)**  
A property is available to allow locked out users to trigger inbound actions. For example, enabling the property can allow locked out users to reset their password and send email to the instance asking for assistance.
-   **[Redirecting email to the instance POP3 account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/r_RedirEmailDifferentAssignGrp.md)**  
Configure other mailboxes to forward email to the instance's POP3 account.
-   **[Inbound email action examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/r_InboundEmailActionExamples.md)**  
Various examples of inbound email actions are available to help you build your own inbound email actions. These examples show how to set up inbound email actions to handle email replies, create \(log\) a problem record, request a change, and update an incident.
-   **[Integrate inbound events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/t_IntegratingInboundEvents.md)**  
This example illustrates how to create a notification from an inbound JSON request.

**Parent Topic:**[Inbound email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/inbound-email-landing.md)

