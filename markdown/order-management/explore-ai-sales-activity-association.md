---
title: AI sales activity association
description: AI sales activity association automatically connects incoming and outgoing emails to the correct CRM records using semantic search and agentic AI. Learn how the application works, its benefits, and common use cases for automating email association in your Sales CRM instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/explore-ai-sales-activity-association.html
release: australia
topic_type: concept
last_updated: "2026-06-24"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Activity Management, Sales automation, Explore, Sales Customer Relationship Management]
---

# AI sales activity association

AI sales activity association automatically connects incoming and outgoing emails to the correct CRM records using semantic search and agentic AI. Learn how the application works, its benefits, and common use cases for automating email association in your Sales CRM instance.

## AI sales activity association overview

Using semantic search and AI-powered matching, the AI sales activity association application helps identify relationships between email content and existing accounts, leads, opportunities, and contacts. It automatically captures important communication history without requiring manual association. This automation helps ensure that all relevant customer communications are tracked and visible in your CRM records, even when those conversations begin outside of your organization and later connect to known entities in your system.

The following workflow illustration shows how the system processes and associates an inbound inquiry using the AI sales activity association app.

\[Omitted image "ai-sales-activity-association-landing.svg"\] Alt text: Infographic showing how an admin installs and configures the AI sales activity association app and how the system automatically processes the emails. For details, refer to the following description.

1.  As an admin, install the AI sales activity association application.
2.  Install the User Mailbox Integration plugin.
3.  Configure email promotion so that emails that arrive in sales representatives' personal mailboxes are forwarded to the Staged Email \[sys\_email\_staging\] table.
4.  A prospect submits an inquiry through the company website or sends an email directly to a sales representative.
5.  The email enters the Staged Email \[sys\_email\_staging\] table where it waits for analysis.
6.  An agentic AI workflow activates to determine if the intent of the email is related to sales.
7.  If the sales intent is confirmed, the system uses semantic search to analyze the email content, looking for clues about which CRM entity \(account, lead, opportunity, or contact\) it might relate to, which includes:
    -   Email sender and recipient information
    -   Keywords and context from the message
    -   Mentioned product details or business context
8.  If the system identifies a matching entity with sufficient confidence, it auto-associates the email to that CRM entity and the sales representative is notified. Otherwise, the email is ignored.
9.  If an email was ignored but the sales representative expected it to have been associated with a record, they can use the ServiceNow CRM for Outlook add-in to manually associate the email. For more information, see [CRM Outlook Add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-crm-outlook-add-in.md).

## AI sales activity association benefits

-   **Accuracy**

    Emails are matched based on semantic understanding of content, not just keyword matching. The system recognizes context and intent, reducing false associations.

-   **Efficiency**

    No more manual searching through emails or digging for related communications. The system handles association in the background, freeing your team to focus on selling and customer engagement.

-   **Completeness**

    Captures communications that would otherwise be lost outside your CRM system. Ensures that every relevant customer interaction is visible and accessible in your records.

-   **Data quality**

    Reduces duplicate records and orphaned communications. Keeps your CRM data cleaner and more reliable for reporting and analysis.

-   **Informed decision-making**

    Sales teams have a complete communication history at their fingertips, enabling better judgment on customer needs, engagement level, and deal momentum.


## AI sales activity association use cases

-   **Multi-threaded customer engagement**

    A customer sends an email about a new inquiry while simultaneously having an active opportunity in the system. The AI auto-association feature automatically connects both communications to the opportunity record, creating a complete view of all interactions for that deal.

-   **Prospect journey from outreach to qualification**

    Your sales team has been nurturing a lead record in the CRM for a prospect who showed early interest in your product. When the prospect replies to a follow-up email or sends a new inquiry, that email lands in the staging table and triggers AI sales activity association. The AI agent evaluates the email and automatically links it to the correct lead record. As the prospect moves through qualification, every new inbound and outbound email is associated with the lead record as it arrives, building a comprehensive engagement timeline. Your sales team gets a complete, real-time view of prospect interactions without the overhead of manually logging each touchpoint.


## What to explore next

To learn more about configuring AI sales activity association, see:

-   [Configuring Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-activity-management.md)
-   [Install AI sales activity association](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-ai-sales-activity-association.md)

