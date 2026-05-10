---
title: Virtual Agent conversations for Vaccination Status
description: Vaccination Status provides a Virtual Agent conversation that enables users to report their vaccination status via SMS.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Vaccination Status, Safe Workplace, Health and Safety, Employee Service Management]
---

# Virtual Agent conversations for Vaccination Status

Vaccination Status provides a Virtual Agent conversation that enables users to report their vaccination status via SMS.

A ServiceNow® Virtual Agent conversation topic defines the dialog between the Virtual Agent \(chatbot\) and the user to accomplish a specific goal. The provided Vaccine conversation topic asks whether the user has been vaccinated, the date that they received the vaccine, and the type of vaccine that they received.

## Installation and setup requirements

To use Virtual Agent with SMS, your organization must have a Twilio account and phone number. You must also install the Virtual Agent plugin \(com.glide.cs.chatbot\) and set up the Conversational SMS Integration with Twilio application \(sn\_va\_sms\_twilio\). For more information, see [Set up the Conversational SMS Integration with Twilio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/configure-twilio-adapter.md).

On-premise customers who install the Safe Workplace applications in the Rome release for the first time require a scoped admin role to create an approved scope-to-scope Restricted Caller Access \(RCA\) record in Vaccination Status. This cross-scoped access is required for Conversational SMS Integration with Twilio to function in the Vaccination Status application.

The RCA record should have the following values set:

|Field|Value|
|-----|-----|
|Source Scope|Emergency Outreach|
|Source Type|Scope|
|Status|Vaccination Status|
|Application|Vaccination Status|
|Target Type|Scope|

For more information on creating caller access records, see [Set application scope, application resource, and event access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/scope-resource-access.md).

## Configuration

To receive SMS messages for Vaccination Status, users must have a mobile phone number listed on their user record \[sys\_user\]. Mobile numbers must be in E.164 format. For example, `+18585551212`.

Privacy consent for Vaccination Status must be configured before users can report their vaccination status via SMS. For instructions, see [Set up privacy consent for Vaccination Status](../task/set-up-vaccine-privacy.md).

**Note:** Users must agree to the privacy consent before they can submit their vaccination status. The Vaccine conversation topic prompts users to complete the privacy consent via SMS if they haven't already submitted their consent. Users must belong to an audience associated with a vaccine privacy consent outreach to be able to complete the privacy consent via SMS.

Vaccination Status uses an SMS outreach to let users know that they can report their vaccination status via SMS. The outreach provides users with the information that they need to begin interacting with the Vaccine Virtual Agent conversation. To configure the outreach, add users to the placeholder Vaccination status request audience. For detailed instructions about adding users to an audience, see [Add a Safe Workplace audience](../../employee-readiness-core/task/add-safe-workplace-audience.md). Then, add the audience to the placeholder Vaccination status request outreach and make any modifications to the outreach if needed, such as scheduling a time to send.

Once users receive the SMS outreach, they can report their vaccination status through the Vaccine Virtual Agent conversation. The Vaccine conversation topic is ready to use without modifications, but can be customized to meet your organization's requirements. To view or edit the Vaccine conversation topic, navigate to **Collaboration** &gt; **Virtual Agent** &gt; **Designer**. For more information about updating conversation topics, see [Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md).

The Vaccine conversation provides the user with options to select which type of vaccine they received. These options are pulled from the Vaccine response definition table \[sn\_imt\_vaccine\_vaccine\_response\_definition\]. To set the display name for a vaccine type, enter the name in the **SMS friendly name** field on the vaccine response definition record.

**Parent Topic:**[Vaccination Status](vaccination-status.md)

