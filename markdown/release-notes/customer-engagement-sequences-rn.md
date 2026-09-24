---
title: Customer Engagement Sequences release notes
description: The ServiceNow Customer Engagement Sequences application enables customer-focused teams to execute structured, personalized outreach and follow-up activities that engage customers throughout their relationship with your business. See the following sections for release notes by version.Accelerate lead nurturing with a new email-based sequence available with the application that automates outreach, follow-up, and escalation to phone calls.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/customer-engagement-sequences-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Sales Customer Relationship Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Customer Engagement Sequences release notes

The ServiceNow® Customer Engagement Sequences application enables customer-focused teams to execute structured, personalized outreach and follow-up activities that engage customers throughout their relationship with your business. See the following sections for release notes by version.

## About Customer Engagement Sequences

-   Increase sales team productivity by automating repetitive outreach tasks so representatives can focus on high-value selling activities.
-   Deliver consistent, effective outreach at every stage of the customer relationship with structured, multi-channel engagement plans such as calls and emails.
-   Reduce missed follow-ups and speed up new-representative ramp-up by giving every representative a proven, predefined outreach playbook.
-   Build and adapt outreach sequences without developer effort using a no-code interface your sales operations team can maintain.
-   Give sales leaders visibility into what's working so they can scale high-performing sequences across territories.

See [Customer Engagement Sequences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/explore-customer-engagement-sequences.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Customer Engagement Sequences \(com.sn\_crm\_sequence\) from the ServiceNow Store. Assign delegated developer roles to designated users so they can create and manage sequences without needing the system admin role.

-   **Additional requirements**

    Email-based sequences requires the User Mailbox Integration plugin \(com.glide.email.user\_mailbox.integration\) to be active on your instance so that the sequence can detect email replies from prospects.


## Accessibility and localization

-   **Localization information**

    Customer Engagement Sequences is available in Arabic, Brazilian Portuguese, Chinese, Czech, Dutch, Finnish, French, French Canadian, German, Hebrew, Hungarian, Italian, Japanese, Korean, Norwegian, Polish, Portuguese, Russian, Spanish, Swedish, Thai, Traditional Chinese, and Turkish. Language packs are installed automatically when the corresponding ServiceNow AI Platform base system language plugin is active.


**Parent Topic:**[Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/sales-order-management-rn-landing.md)

## Version 2.3.1

Accelerate lead nurturing with a new email-based sequence available with the application that automates outreach, follow-up, and escalation to phone calls.

### What's new

-   **[Lead nurturing email sequence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/customize-lead-nurturing-email-sequence.md)**

    Accelerate lead nurturing by creating an email-based sequence that automates outreach and follow-up. A sample sequence is available with the application. When a lead with an email address is created, the sequence assigns a sequence task to the lead's owner, sends an initial outreach email, and automatically sends a follow-up email if there's no reply. If the prospect still hasn't responded, the sequence escalates to two call attempts, then updates the lead's work notes if no response is received on any channel. The sequence exits as soon as the prospect replies to an email or a call is resolved.


