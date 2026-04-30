---
title: Automatic creation of AI cases and inquiries from an inbound email
description: The system automatically creates AI cases and inquiries from emails, using keywords in the subject line and body.
locale: en-US
release: yokohama
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2025-12-01"
reading_time_minutes: 3
breadcrumb: [Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Automatic creation of AI cases and inquiries from an inbound email

The system automatically creates AI cases and inquiries from emails, using keywords in the subject line and body.

## Overview of the Email Reporting Feature

The email reporting feature provides a simple and familiar way for users to submit AI-related cases or inquiries directly into the system. Instead of navigating a dedicated portal or filling out forms, users can simply send an email to a designated email address and an instance email address. On receipt, the system automatically processes this inbound email, extracting key information such as the subject, body, and sender, and creates an AI Case or Inquiry. This automation confirms that every submission is captured consistently and immediately, ready for review and action.

## Benefits of the Email Reporting Feature

This feature offers the following advantages:

-   Using email to report issues or asking questions removes the need for users to learn new interfaces or processes.
-   Removing manual data entry saves time and lowers the chance of mistakes, enabling teams to focus on resolving issues instead of administrative work.
-   Converting each email into a trackable record provides clear details such as the sender, subject, and message body, making it easier to review what was reported.
-   Creating records automatically makes new cases and questions visible to the correct teams, helping them review, assign, and resolve them faster.

## Configure the Email Reporting Feature

You must follow the following steps to enable the email reporting feature:

1.  Admin must enable the Inbound Email Configuration from the Email Properties page. For more information, refer to [Inbound mail configuration](https://www.servicenow.com/docs/access?context=r_InboundMailConfiguration&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).![Inbound email configurations to enable.](../image/inbound-email-properties-airc.png)
2.  AI Case Admin \[sn\_ai\_case\_mgmt.ai\_case\_admin\] must update the group email field on the Case type record. Navigate to **AI Case Management** &gt; **Case type**.

    ![AI Case record type.](../image/ai-case-group-email.png)

3.  AI Case Admin \[sn\_ai\_case\_mgmt.ai\_case\_admin\] must update the group email field on the Inquiry type record. Navigate to **AI Case Management** &gt; **Inquiry Type**.

    ![AI inquiry record type.](../image/ai-inquiry-group-email.png)


**Note:** After you configure, if any email is sent to the defined group email address and the instance address, an AI Case or AI Inquiry record is created.

## Email to ServiceNow fields mapping

This feature automatically populates AI Case and AI Inquiry fields in ServiceNow using information from inbound emails, confirming consistent data capture and streamlining the reporting process.

When an email is received:

-   The sender of the email is mapped to the **Requester** field for both AI Cases and AI Inquiries.

    **Note:** This feature is only available when the **Automatically create users for incoming emails from trusted domains** property is enabled on the Inbound Email Configuration form. For more information, refer to [Configure the Email Reporting Feature](automatic-creation-cases-inquiries-from-email.md#section_pdz_gbm_mhc). When the property is disabled, the **Requester** field will display **Guest**.

-   The date the email is sent populates the **Date of Discovery** field for AI Cases and the **Created on** field for AI Inquiries.
-   The TO recipient of the email is used to determine the **Assignment group** for both record types.
-   Any CC recipients on the email are added to the **Watch list** for both AI Cases and AI Inquiries.
-   The priority of the Case or Inquiry is determined by the email’s Importance value.
    -   A High-importance email creates an AI Case or Inquiry with Priority 2 \(High\).
    -   A Normal-importance email creates an AI Case or Inquiry with Priority 3 \(Moderate\).
    -   A Low-importance email creates an AI Case or Inquiry with Priority 4 \(Low\).
-   The subject of the email becomes the **Name** of the new AI Case or AI Inquiry record.
-   The message body of the email populates the **Description** field for both record types.
-   Any attachments included in the email can also be transferred and linked to the new record.
-   The **Source** field is automatically set to **Email** for AI Cases.

