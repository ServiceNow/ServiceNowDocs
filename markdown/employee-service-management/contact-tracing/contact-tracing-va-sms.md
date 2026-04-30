---
title: Virtual Agent conversations for Contact Tracing
description: Contact Tracing provides a Virtual Agent conversation to assess the health of potentially exposed contacts via SMS.As an administrator, you can configure Contact Tracing to enable Exposure Case Task Surveys to be automatically sent via SMS.
locale: en-US
release: xanadu
product: Contact Tracing
classification: contact-tracing
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Virtual Agent conversations for Contact Tracing

Contact Tracing provides a Virtual Agent conversation to assess the health of potentially exposed contacts via SMS.

## Contact Tracing Overview

A Virtual Agent conversation topic enables a dialog between the Virtual Agent \(chatbot\) and a user to accomplish a specific goal. The provided Exposure conversation topic for Contact Tracing asks potentially exposed contacts questions based on the Exposure Case Task Survey. Contact tracers use the responses to assess the health of a potentially exposed contact.

Contact Tracing uses an SMS outreach to initiate the Virtual Agent conversation and begin the survey. The Exposure Case Task Survey outreach can be sent automatically when users are added to case tasks as exposed contacts. Alternatively, contact tracers can send the survey manually while working on a case task by selecting the **Send SMS Survey** button. Users who receive the survey can reply back via SMS.

Organizations can use the Exposure conversation topic and Exposure Case Task Survey as provided or customize it. For example, you might want to add a "Prefer not to say" answer option to one or more questions.

**Note:** To complete the customization, you must apply any changes to both the Exposure conversation topic in **Virtual Agent** &gt; **Designer** and the Exposure Case Task Survey in **Survey** &gt; **View Surveys**. Applying changes to only the conversation topic or the survey will not update both the topic and survey.

-   For more information on updating conversation topics, see [Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).
-   For more information on updating surveys, see [Survey designer](https://www.servicenow.com/docs/access?context=c_SurveyDesigner&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Installation and setup requirements

Note the following requirements to use Virtual Agent with SMS:

-   A Twilio account and phone number.

-   The Emergency Outreach application.

    For details, see [Install Emergency Outreach](../../business-continuity/task/install-emergency-outreach.md#).

-   The Virtual Agent plugin \(com.glide.cs.chatbot\).

-   Conversational SMS Integration with Twilio application \(sn\_va\_sms\_twilio\).

    For more information, see [Set up the Conversational SMS Integration with Twilio](https://www.servicenow.com/docs/access?context=configure-twilio-adapter&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).


Note the following requirements for users to complete Exposure Case Task Surveys via SMS:

-   Your organization must install and set up Virtual Agent for use with SMS.
-   To receive SMS messages for Contact Tracing, users must have a mobile phone number listed on their user record \[sys\_user\]. Mobile numbers must be in E.164 format, for example, `+18585551212`.
-   Privacy consent for Contact Tracing must be configured before users can reply to SMS messages. For instructions and more information, see [Setting up data privacy consent settings for Contact Tracing](set-up-privacy-consent-settings.md).
-   Users must agree to the privacy consent before they can respond to the survey.

**Parent Topic:**[Setting up Contact Tracing](set-up-contact-tracing.md)

## Send Exposure Case Task Surveys automatically via SMS

As an administrator, you can configure Contact Tracing to enable Exposure Case Task Surveys to be automatically sent via SMS.

### Before you begin

Ensure that the installation and setup requirements to enable Virtual Agent conversations for Contact Tracing are met. For more information, see [Virtual Agent conversations for Contact Tracing](contact-tracing-va-sms.md#).

Role required: admin

### About this task

Enable the **sn\_imt\_tracing.enable\_sms\_exposure\_survey** property so that Exposure Case Task Surveys are sent automatically when users are added to Exposed Contacts. Potentially exposed contacts can respond to the surveys via SMS, providing contact tracers with an assessment of their health status.

### Procedure

1.  Configure the **sn\_imt\_tracing.enable\_sms\_exposure\_survey** property.

    1.  Navigate to **Contact Tracing** &gt; **Administration** &gt; **Properties**.

    2.  Set the **sn\_imt\_tracing.enable\_sms\_exposure\_survey** property to **Yes**.

    3.  Click **Save**.

2.  Modify the survey questions and answers sent to potentially exposed contacts.

    For example, add a "Prefer not to say" answer option to one or more questions.

    1.  Update the Exposure Virtual Agent conversation topic in **Virtual Agent** &gt; **Designer**.

        For more information on updating conversation topics, see [Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

    2.  Update the Exposure Case Task Survey in **Survey** &gt; **View Surveys**.

        For more information on updating surveys, see [Survey designer](https://www.servicenow.com/docs/access?context=c_SurveyDesigner&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    To complete the customization, you must apply any changes to both the Exposure conversation topic in **Virtual Agent** &gt; **Designer** and the Exposure Case Task Survey in **Survey** &gt; **View Surveys**. Applying changes to only the conversation topic or the survey will not update both the topic and survey.


### Result

When adding users to potentially exposed contacts in case tasks:

-   Potentially exposed contacts are automatically added to the Exposure case task survey audience.
-   The Exposure Case Task Survey outreach sends the SMS notification to the audience and the Virtual Agent processes the responses, executing the survey as an SMS conversation.
-   Survey answers are stored in the \[asmt\_metric\_result\] table.

