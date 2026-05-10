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

-   
-   [Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-landing-cmdb.md)
-   [Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm.md)
-   [Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/now-assist-ea.md)
-   [Now Assist for Operational Sustainability \(formerly ESG\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/now-assist-for-esg.md)
-   [Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/now-assist-fsm.md)
-   [Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/now-assist-for-financial-services-operations.md)
-   [Now Assist for Hardware Asset Management \(HAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-hardware-asset-management/now-assist-ham.md)
-   [Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-health-and-safety/now-assist-hs-landing.md)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd.md)
-   [Now Assist for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom.md)
-   [Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm.md)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-legal-service-delivery/now-assist-lsd-landing.md)
-   [Now Assist for Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/now-assist-for-psds.md)
-   [Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/now-assist-for-irm.md)
-   [Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-security-incident-landing.md)
-   [Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/now-assist-sam.md)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo.md)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/now-assist-spm.md)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo.md)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spmc.md)
-   [Now Assist for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/now-assist-tprm.md)
-   [Now Assist for Workplace Service Delivery \(WSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-wsd/now-assist-wsd-landing.md)
-   [Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-now-assit-landing.md)
-   [Now Assist in Conversational Spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/conv-spokes-na.md)
-   [ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/servicenow-lens-landing-page.md)

**Note:** When you upgrade to the latest version of Now Assist in AI Search, the system reindexes content from the Catalog Item Table and Knowledge Table indexed sources. While these reindexing tasks are ongoing, searches may not return Catalog and Q&amp;A Genius Result answers. Once reindexing completes, Catalog and Q&amp;A Genius Result answers should appear normally.

## Procedure

1.  In Now Assist Admin, install one or more of the prerequisite feature plugins found in "About this task".

    For Now Assist feature plugin installation instructions, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

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

