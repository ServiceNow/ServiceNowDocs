---
title: Automatic creation of AI cases and inquiries from inbound email
description: The system automatically creates AI cases and inquiries from inbound emails using keywords in the subject line and body based on configured email intake settings.
locale: en-US
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Automatic creation of AI cases and inquiries from inbound email

The system automatically creates AI cases and inquiries from inbound emails using keywords in the subject line and body based on configured email intake settings.

## Overview of email-based intake

Email-based intake provides a simple and familiar way for users to submit AI-related cases or inquiries. Instead of navigating a portal or completing forms, users send an email to configured addresses. When an email is received, the system processes the message extracting key information such as the subject, body, and sender, and creates an AI Case or Inquiry. This automation helps capture submissions consistently and immediately, ready for review and action.

For step-by-step configuration instructions, see [Configure email-based intake for AI Risk and Compliance](../task/config-cases-inquiries-from-email.md).

## Benefits of email-based intake

This capability offers the following benefits:

-   Users can submit AI-related concerns or questions using a familiar communication method.
-   Reduces manual data entry and helps minimize reporting errors.
-   Helps confirm that each submission is captured as a trackable record.
-   Improves visibility by making new cases and inquiries immediately available for review.

## Email-to-ServiceNow field mapping

When an inbound email is processed, information from the email is used to populate fields on the resulting AI Case or AI Inquiry record.

-   The email sender is mapped to the **Requester** field for both record types.

    **Note:** This behavior depends on inbound email configuration and trusted domain settings. When automatic user creation is disabled, the **Requester** field displays **Guest**.

-   The email sent date populates the **Date of Discovery** field for AI cases and the **Created on** field for AI inquiries.
-   The TO recipient determines the **Assignment group** for both record types.
-   Any CC recipients are added to the **Watch list**.
-   Email importance determines the case or inquiry priority.
    -   High importance: Creates AI case or Inquiry with Priority 2 \(High\).
    -   Normal importance: Creates AI case or Inquiry with Priority 3 \(Moderate\).
    -   Low importance: Creates AI case or Inquiry with Priority 4 \(Low\).
-   The email subject is set to the record **Name**.
-   The email body populates the **Description** field.
-   Email attachments are included and linked to the record.
-   For AI cases, the **Source** field is set to **Email**.

