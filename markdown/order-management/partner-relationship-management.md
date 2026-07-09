---
title: Partner Relationship Management
description: Learn how Partner Relationship Management gives enterprises and channel partners a shared platform to manage the partner sales lifecycle, from deal registration through order fulfillment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/partner-relationship-management.html
release: australia
topic_type: concept
last_updated: "2026-07-07"
reading_time_minutes: 8
keywords: [explore]
breadcrumb: [Explore, Sales Customer Relationship Management]
---

# Partner Relationship Management

Learn how Partner Relationship Management gives enterprises and channel partners a shared platform to manage the partner sales lifecycle, from deal registration through order fulfillment.

## Partner Relationship Management overview

Use Partner Relationship Management to define and manage partner programs, onboard channel partners, and collaborate on deals, quotes, and orders — all within a single platform. Channel partners access their work through the Partner portal, while enterprise teams use the Partner Workspace. Both sides see a consistent, real-time view of the partner relationship.

Partner Relationship Management is built on three core entities: partner, partner program, and partner segment. These entities define who channel partners are, what programs they participate in, and at what tier they operate. A partner can belong to multiple programs but holds exactly one segment within each program.

## Use case

ABC Systems, a global technology reseller and implementation channel partner for XYZ Solutions \(enterprise\), operates across North America with hundreds of active customer engagements. ABC's consulting and delivery teams frequently encounter challenges requiring direct support from XYZ, such as clarification on licensing models or product configurations. With Partner Relationship Management, ABC no longer needs to rely on ad hoc emails, informal escalation channels, or multiple sessions leading to delays.

With Partner Relationship Management, the channel partner ABC can do the following:

-   Submit and manage support cases through the Partner portal designed for easy access and case tracking.
-   Benefit from a role-based experience where channel partner managers and associates can independently raise cases and monitor status without dependency on enterprise contacts.
-   Gain visibility into program participation and support activities through personalized dashboards.
-   Use the unified partner data model to confirm that entitlements and participation in XYZ's partner programs are accurately tracked and easily accessible.

With Partner Relationship Management, the enterprise XYZ can do the following:

-   View and fulfill cases raised by the channel partner ABC in a centralized workspace.
-   Route assignments to the appropriate support agents.
-   Track channel partner engagement levels within ABC via real-time dashboards.

By streamlining support and collaboration through Partner Relationship Management, ABC reduces its resolution time, improves internal efficiency, and strengthens its partnership with XYZ.

## Partner Relationship Management users

|User|Description|
|----|-----------|
|Enterprise admin|Sets up and maintains the Partner Relationship Management configuration. Creates and manages partner programs, segments, and criteria. Onboards new channel partners and owns partner primary data.|
|Enterprise relationship manager|Acts as the main point of contact between the enterprise and one or more channel partners. Tracks all partner activity — deals, quotes, orders, and cases — and reviews and approves deal registrations submitted by channel partners.|
|Channel partner manager|Accesses the Partner portal to manage their team, onboard new staff, register and track deals, and monitor the partner pipeline including opportunities, quotes, and orders.|
|Partner associate|A frontline sales agent who registers deals, creates quotes on behalf of customers, manages cases, and provides customer support. Can work with multiple channel partners simultaneously.|

## Partner Relationship Management workflow

The following illustration describes the tasks involved in configuring and using Partner Relationship Management, organized by platform and persona.\[Omitted image "prm-workflow.png"\] Alt text: Partner Relationship Management workflow

## CSM configurable workspace in Partner Relationship Management

The Partner Workspace is the enterprise-facing platform in Partner Relationship Management. Enterprise admins, enterprise relationship managers, and enterprise partner agents use it to configure, manage, and monitor the partner ecosystem.

**Enterprise admin**

1.  Configure Partner Relationship Management — set up programs, segments, and roles:
    -   Create partner programs \(for example, referral, reseller, authorized trainer\).
    -   Define partner segments and tier criteria \(for example, Silver, Gold, Platinum\).
    -   Set access policies and assign roles to enterprise and channel partner users.
2.  Onboard channel partner organizations, register partner members, and assign them to the relevant programs and tiers.
3.  Manage access policies to ensure cross-partner data isolation and role-appropriate visibility across the partner ecosystem.

**Enterprise relationship manager**

1.  View and track all partner activity — deals, quotes, orders, and cases — from the Partner Workspace pipeline dashboard.
2.  Approve a deal registration submitted by the channel partner:
    -   Confirm no duplicate deal exists for the same customer and product.
    -   Approve the deal, locking it exclusively for that partner.
3.  Approve the quote submitted by the channel partner:
    -   Verify pricing reflects the rates defined for the partner's program and segment tier.
    -   Finalize pricing. The system automatically converts the approved quote into a sales order.

**Enterprise partner agent**

Fulfill cases raised by channel partners from the Partner Workspace:

-   Assign cases to the appropriate support team.
-   Update case status and post resolution notes.
-   Case resolution status is updated in the Partner portal for the channel partner to track.

## Partner portal in Partner Relationship Management

The Partner portal is the channel partner-facing platform in Partner Relationship Management. Channel partner managers and partner associates use it to manage deals, quotes, orders, cases, and team members. Channel partners have no access to the Partner Workspace.

**Channel partner manager**

1.  Onboard team members and register new staff on the Partner portal.
2.  Register a deal on the Partner portal:
    -   Capture the customer name, product area, and estimated deal value.
    -   Submit for enterprise review. The deal is approved and locked for that partner.
3.  View the pipeline to monitor deal progress, approval status, and associated opportunities.

**Partner associate**

1.  Create a quote from the Partner portal once the customer is ready for pricing. The enterprise relationship manager reviews and approves the quote before it is finalized.
2.  Track the order after the approved quote converts to a sales order:
    -   View order details and fulfillment progress.
    -   Manage attachments and download completed order documentation.
    -   Communicate with the enterprise team through comments and notes.
3.  Raise a support case from the Partner portal:
    -   Submit the case for enterprise review.
    -   Track case status and receive resolution updates from the enterprise partner agent.

## Partner Relationship Management benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Lock approved deals exclusively for the registering partner, preventing channel conflict and protecting partner commissions.|[Deal Registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/deal-registration-management.md)|Enterprise relationship manager, channel partner manager, partner associate|
|Automatically convert approved deals into enterprise pipeline opportunities. Partners can view pipeline stages and qualification status directly from the Partner portal.|[Install Opportunity Management for Channel Partners](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-opportunity-management-for-channel-partners.md)|Enterprise relationship manager, channel partner manager, partner associate|
|Create and submit quotes from the Partner portal with tier-based pricing applied automatically. Quotes go through enterprise review and approval before finalization.|[Install Quote Management for Channel Partners](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-quote-management-for-channel-partners.md)|Enterprise relationship manager, partner associate|
|Track order status, manage attachments, and communicate with enterprise teams directly from the Partner portal, without switching to internal systems or email.|[Quote creation via Self-Service for Channel Partners](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/self-service-quote.md)|Partner associate|
|Raise, submit, and track support cases through the Partner portal. Enterprise agents fulfill cases from a centralized workspace and route them to the appropriate teams.|[Create cases for channel partners](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-cases-for-channel-partners.md)|Enterprise partner agent, channel partner manager, partner associate|
|View all partner activity — deals, opportunities, quotes, orders, and cases — in one workspace. Monitor partner engagement and pipeline health via real-time dashboards.|[Partner Relationship Management in CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/partner-workspace.md)|Enterprise admin, enterprise relationship manager, enterprise partner agent|
|Onboard channel partners and manage their full lifecycle from a single configuration layer, reducing onboarding time and improving partner satisfaction.|Partner onboarding and lifecycle management|Enterprise admin, enterprise relationship manager|
|Assign partners to programs and tiers to automatically apply accurate pricing, discounts, and enablement resources. A partner can belong to multiple programs, each with a single segment.|[Create Partner Programs on the CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-partner-programs-on-workspace.md), [Configure Segment Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-segment-management.md)|Enterprise admin, channel partner manager|
|Restrict data access by role and enforce cross-partner isolation so partners can only view their own data. Admins set granular access policies per entity.|[Roles and components of Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/roles-and-components-of-partner-relationship-management.md)|Enterprise admin|

## What to explore next

To learn more about configuring and using Partner Relationship Management, see:

-   [Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-partner-relationship-management.md)
-   [Using Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-partner-relationship-management.md)
-   [Data model for Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/data-model-for-partner-relationship-management.md)

