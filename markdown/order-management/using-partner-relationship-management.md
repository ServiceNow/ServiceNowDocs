---
title: Using Partner Relationship Management
description: Install the Partner Relationship Management plugin \(com.snc.partner\_relationship\_management\) to enable administrators and channel partners to collaborate through the Partner portal and PRM workspace. As an Enterprise Partner Relationship Manager, you can manage partner relationships, approvals, and sales activity. As a channel partner, you can access the Partner portal to register deals, create quotes, and track opportunities—all from a single, branded experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/using-partner-relationship-management.html
release: australia
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 5
breadcrumb: [Use, Sales Customer Relationship Management]
---

# Using Partner Relationship Management

Install the Partner Relationship Management plugin \(com.snc.partner\_relationship\_management\) to enable administrators and channel partners to collaborate through the Partner portal and PRM workspace. As an Enterprise Partner Relationship Manager, you can manage partner relationships, approvals, and sales activity. As a channel partner, you can access the Partner portal to register deals, create quotes, and track opportunities—all from a single, branded experience.

## What you can do

**Enterprise Partner Relationship Managers**:

-   Set up partner hierarchies, tiers, and territories
-   Configure approval workflows for deal registrations and quotes
-   Define product catalogs and discount governance by partner tier
-   Monitor partner sales activity and deal pipeline
-   Manage partner staff and access controls
-   Track deal registrations through approval stages

**Channel Partners**:

-   Register deals through guided workflows
-   Create and submit quotes for enterprise approval
-   Track quote status and deal registrations in real-time
-   Manage staff members and team access
-   View opportunities and orders
-   Access knowledge articles and engage with the community

:

## Partner portal

Partner portal is the partner-facing workspace where partners manage sales activity, quotes, and deal registrations.

\[Omitted image "partner-portal-ui.png"\] Alt text: Interface of the partner portal

From the Partner Portal, you can use and access the following features.

<table id="table_s1t_hjx_1fc"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create

</td><td>

Allows channel partners to create deal registrations, cases, or quotes.To learn more about creating deal registrations, see [Register a deal on Partner portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/register-a-deal-partner-portal.md).

To learn more about creating quotes, see [Create a Quote via Self-Service for Channel Partners](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-a-self-service-quote.md).

</td></tr><tr><td>

Sales

</td><td>

Overview of deal registrations, opportunities, and quotes.View deal registrations in the **Draft**, **Submitted**, and **Approved** states.

View Self-service quotes

View a list of all active opportunities and their detailed analytics.

</td></tr><tr><td>

Services

</td><td>

Provides access to all cases and quick links to open cases that require action.

</td></tr><tr><td>

Catalog

</td><td>

List of all services that can be performed by a channel partner.

</td></tr><tr><td>

Partner Center

</td><td>

List of all the channel partners.

</td></tr><tr><td>

Knowledge

</td><td>

Select **Knowledge** on the header to view the kb\_home page.You can search the knowledge base or view a list of top-rated or most viewed knowledge base articles.

</td></tr><tr><td>

General Inquiry

</td><td>

Raise concerns or queries with the enterprise.To learn more about general inquiry, see [Raise an inquiry on Partner Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/raise-an-inquiry-on-partner-portal.md).

</td></tr><tr><td>

Browse catalog

</td><td>

List of all catalog forms.

</td></tr><tr><td>

Cases

</td><td>

Provides access to all cases and quick links to open cases that require action.

</td></tr><tr><td>

My Lists

</td><td>

Lists of deal registrations, opportunities, quotes, orders, and cases associated to the channel partner.Select **Opportunity** to view detailed information about the line items and activity associated with an oportunity.

</td></tr><tr><td>

Quick Links

</td><td>

Links to knowledge articles and other information.

</td></tr><tr><td>

Tours

</td><td>

View a tour for additional guidance on how the Partner Portal works.Your administrator determines whether tours appear on pages.

</td></tr><tr><td>

Profile menu

</td><td>

Select your profile picture to view your profile or log out of the Partner portal.

</td></tr><tr><td>

Search

</td><td>

Search for support articles and other requests.Enter a search word or term and select **Search** to view the results.

</td></tr></tbody>
</table>## Deal Registration

Channel partners register deals through a structured workflow in the Partner Portal. To register a deal:

1.  Select Create &gt; Register a Deal.
2.  Enter deal details: account name, amount, close date, and product category.
3.  The deal is saved in Draft status.
4.  Submit for enterprise approval when ready.
5.  Track approval progress in the Sales section.

Enterprise managers configure approval workflows by territory, partner tier, and deal amount. Partners receive real-time notifications when their deal is approved or needs revision.

## Quote Management

Channel partners create and submit quotes directly from the Partner Portal. To create a quote:

1.  Select Create &gt; Create Quote.
2.  Select a customer and add products from the approved catalog.
3.  Configure quantities and optionsApply pre-approved discounts \(within limits\).
4.  Add attachments or internal notes.
5.  Submit for approval.

To track quotes:

-   View all quotes in the Sales section.
-   Filter by status: Draft, Submitted, or Approved.
-   Track approval progress in real-time.
-   Download approved quotes as PDF.
-   View full version history and activity.

Enterprise managers define approval rules by quote amount, partner tier, and product category. Approved quotes can automatically convert to opportunities for downstream order processing.

## CSM configurable workspace for PRM \(For Administrators\)

The PRM workspace is where enterprise administrators configure partner programs, approvals, and governance.

Key configuration areas:

-   Partner setup: Define partner hierarchies, tiers, programs, and territory assignments.
-   Approval workflows: Configure multi-stage approval rules for deal registrations and quotes by territory, tier, and amount.
-   Product catalog management: Manage which products each partner tier can access. Set discount limits and approval thresholds.
-   User roles and permissions: Assign roles to Partner Managers, Admins, and Agents. Control what each user sees and can approve.
-   Reporting and analytics: Track partner deal pipeline, quote activity, and approval metrics. Monitor channel revenue.
-   Integration settings: Configure automatic opportunity conversion from approved deals. Map custom fields for downstream workflows.

-   **[Create Channel Partner record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-channel-partner-record.md)**  
Create and track channel partner records on the partner workspace to manage and store all information related to the channel partners.
-   **[Create cases for channel partners](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-cases-for-channel-partners.md)**  
Create customer service cases for channel partners to manage customer queries and offer resolution.
-   **[Update deal registration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/update-deal-registration-record.md)**  
Create a deal registration record or perform actions on an existing record on the CSM Configurable Workspace.
-   **[Raise an inquiry on Partner Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/raise-an-inquiry-on-partner-portal.md)**  
Raise a query or concern with the enterprise on the Partner Portal.
-   **[Register a member on Partner portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/register-a-member-on-partner-portal.md)**  
Register a new partner member or transfer existing staff within a partner organization.
-   **[Register a deal on Partner portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/register-a-deal-partner-portal.md)**  
Register a deal on the Partner portal to update its state and trigger the end-to-end life cycle of the deal.
-   **[Create a Quote via Self-Service for Channel Partners](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-a-self-service-quote.md)**  
Use the Quote Self-Service plugin \(com.sn\_quote\_self\_service\) to create and submit a configured quote directly from the Partner portal.
-   **[View opportunity analytics on Partner portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-opportunity-analytics-on-partner-portal.md)**  
View detailed analytics related to the opportunities accessible to you on the Partner portal.
-   **[View quote analytics on Partner portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-quote-analytics-on-partner-portal.md)**  
View detailed analytics related to all the quotes associated to a channel partner on the Partner portal.

**Parent Topic:**[Using Sales Customer Relationship Management applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-using.md)

**Related topics**  


[Raise an inquiry on Partner Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/raise-an-inquiry-on-partner-portal.md)

[Register a member on Partner portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/register-a-member-on-partner-portal.md)

