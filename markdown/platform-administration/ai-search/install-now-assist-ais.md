---
title: Install Now Assist in AI Search
description: As an administrator, you can install the Now Assist in AI Search application \(sn\_ais\_assist\) from the Now Assist Admin module.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Install Now Assist in AI Search

As an administrator, you can install the Now Assist in AI Search application \(sn\_ais\_assist\) from the Now Assist Admin module.

## Before you begin

Role required: admin

## About this task

The Now Assist in AI Search plugin is automatically installed when you install any of these feature plugins from Now Assist Admin:

-   Now Assist for Accounts Payable Operations \(APO\)
-   Now Assist for Configuration Management Database \(CMDB\)
-   Now Assist for Customer Service Management \(CSM\)
-   Now Assist for Enterprise Architecture \(EA\)
-   Now Assist for Operational Sustainability \(formerly ESG\)
-   Now Assist for Field Service Management \(FSM\)
-   Now Assist for Financial Services Operations \(FSO\)
-   Now Assist for Hardware Asset Management \(HAM\)
-   Now Assist for Health and Safety
-   Now Assist for HR Service Delivery \(HRSD\)
-   Now Assist for ITOM
-   Now Assist for IT Service Management \(ITSM\)
-   Now Assist for Legal Service Delivery \(LSD\)
-   Now Assist for Public Sector Digital Services \(PSDS\)
-   Now Assist for Integrated Risk Management \(IRM\)
-   Now Assist for Security Incident Response
-   Now Assist for Software Asset Management \(SAM\)
-   Now Assist for Sourcing and Procurement Operations \(SPO\)
-   Now Assist for Strategic Portfolio Management \(SPM\)
-   Now Assist for Supplier Lifecycle Operations \(SLO\)
-   Now Assist for Telecommunications, Media and Technology \(TMT\)
-   Now Assist for Third-party Risk Management \(TPRM\)
-   Now Assist for Workplace Service Delivery \(WSD\)
-   Now Assist in Contract Management
-   Now Assist in Conversational Spokes
-   ServiceNow AI Lens

**Note:** When you upgrade to the latest version of Now Assist in AI Search, the system reindexes content from the Catalog Item Table and Knowledge Table indexed sources. While these reindexing tasks are ongoing, searches may not return Catalog and Q&amp;A Genius Result answers. Once reindexing completes, Catalog and Q&amp;A Genius Result answers should appear normally.

## Procedure

1.  In Now Assist Admin, install one or more of the prerequisite feature plugins found in "About this task".

    For Now Assist feature plugin installation instructions, see Install Now Assist plugins.

2.  Verify that Now Assist in AI Search is installed:

    1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

    2.  In the workflow list, select **Platform**.

    3.  Verify that the **Conversational experience** feature card displays, and that the **Now Assist Q&amp;A Genius Results** and **Now Assist Actions** skills appear in the **All Conversational experience skills** listing.

        ![Conversational experience feature card showing Now Assist Q&A Genius Results and Now Assist Actions skills.](../image/now-assist-admin-cexp-card-2024-06.png)


## What to do next

With the plugin installed, search administrators can enable Now Assist Genius Results in the following contexts.

-   Enable all available Now Assist Genius Result configurations in individual AI Search portals. For details, see [Enable Now Assist Genius Results in AI Search portals and mobile applications](enable-now-assist-gr-ais-apps.md).
-   Enable Now Assist Q&amp;A Genius Results in search profiles for AI Search applications. For steps, see [Enabling Now Assist Q&amp;A Genius Results](../concept/enabling-now-assist-qa-grs.md#).
-   Enable Now Assist Q&amp;A Genius Results in global search using the AI Search for Next Experience application. For steps, see [Enabling Now Assist Q&amp;A Genius Results](../concept/enabling-now-assist-qa-grs.md#).

To learn more about configuration settings for the plugin, see [Configuring Now Assist in AI Search](../concept/configuring-now-assist-ais.md).

-   **[Review available versions of Now Assist in AI Search](review-available-versions-na-ais.md)**  
View all versions of the Now Assist in AI Search application on the ServiceNow Store. Use this information to find the latest version of the application that's compatible with your instance's current ServiceNow AI Platform® family release.

**Parent Topic:**[Now Assist in AI Search](../reference/now-assist-ais.md)

