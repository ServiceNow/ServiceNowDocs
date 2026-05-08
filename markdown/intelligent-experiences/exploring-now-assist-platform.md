---
title: Exploring Now Assist Admin
description: Learn how Now Assist Admin brings generative AI capabilities to the ServiceNow AI Platform. With Now Assist Admin, you can improve the productivity and efficiency in your organization, deliver better self-service, recommend actions and provide answers, and empower your users to search more effectively.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
keywords: [Exploring, Now Assist, ServiceNow AI Platform, Generative AI, GenAI, framework]
breadcrumb: [Now Assist, Enable AI experiences]
---

# Exploring Now Assist Admin

Learn how Now Assist Admin brings generative AI capabilities to the ServiceNow AI Platform. With Now Assist Admin, you can improve the productivity and efficiency in your organization, deliver better self-service, recommend actions and provide answers, and empower your users to search more effectively.

## Now Assist Admin overview

Now Assist is a growing cross-platform family of generative AI features, which are tasks that a large language model \(LLM\) can perform. Generative AI features are based on the initial training and architecture.

A skill delivers a feature plus the use case to the user. An example of a skill is chat summarization within a customer workspace. Now Assist products provide features and skills that are tailored to meet the needs of users in different workflows.

## Now Assist framework

The Now Assist framework is supported across the ServiceNow AI Platform. To use Now Assist skills, activate one or more of the following Now Assist products.

<table id="table_bdm_bpk_rcc" class="custom-rows"><thead><tr><th class="filter">

Workflow

</th><th>

Business areas

</th><th>

Available products

</th></tr></thead><tbody><tr><td>

Technology

</td><td>

The Technology workflow includes IT applications, such as IT services and operations, managing your strategy to deliver products and services, and platform security.

</td><td>

-   Now Assist for Collaborative Work Management \(CWM\)
-   Now Assist for Configuration Management Database \(CMDB\)
-   Now Assist for Enterprise Architecture \(EA\)
-   Now Assist for Operational Sustainability \(formerly ESG\)
-   Now Assist for Hardware Asset Management \(HAM\)
-   Now Assist for Integrated Risk Management \(IRM\)
-   Now Assist for ITOM
-   Now Assist for IT Service Management \(ITSM\)
-   Operational Technology \(OT\) Manager Foundation
-   Now Assist for Operational Technology Service Management \(OTSM\)
-   Now Assist for Security Incident Response
-   Now Assist for Software Asset Management \(SAM\)
-   Now Assist for Strategic Portfolio Management \(SPM\)
-   Now Assist for Third-party Risk Management \(TPRM\)
-   Now Assist for Vulnerability Response

</td></tr><tr><td>

Customer

</td><td>

The Customer workflow includes applications that support customer service, including field service, financial services, telecommunications and media, and the public service sector.

</td><td>

-   Now Assist for Customer Service Management \(CSM\)
-   Now Assist for Field Service Management \(FSM\)
-   Now Assist for Financial Services Operations \(FSO\)
-   Now Assist for Order Management
-   Now Assist for Public Sector Digital Services \(PSDS\)
-   Now Assist for Sales Force Automation \(SFA\)
-   Now Assist for Telecommunications, Media and Technology \(TMT\)

</td></tr><tr><td>

Employee

</td><td>

The Employee workflow supports HR Service Delivery and Employee Experience features.

</td><td>

-   Now Assist for Employee Experience
-   Now Assist for Health and Safety
-   Now Assist for HR Service Delivery \(HRSD\)
-   Now Assist for Legal Service Delivery \(LSD\)
-   Now Assist for Workplace Service Delivery \(WSD\)

</td></tr><tr><td>

Creator

</td><td>

The Creator workflow supports a variety of Platform tools and builders, including the following:-   App Engine Studio
-   ServiceNow AI Platform scripting
-   Platform Analytics
-   Service Catalog
-   Workflow Studio
-   RPA Hub
-   Process Mining

</td><td>



</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

The Finance &amp; Supply Chain workflow supports purchase requisitions, sourcing requests, and request for products or services.

</td><td>

-   Now Assist for Accounts Payable Operations \(APO\)
-   Now Assist for Supplier Lifecycle Operations \(SLO\)
-   Now Assist for Sourcing and Procurement Operations \(SPO\)

</td></tr><tr><td>

App Engine

</td><td>

The App Engine workflow supports App Engine products and offerings so that you can enhance your custom applications with AI.

</td><td>

Now Assist for App Engine

</td></tr><tr><td>

Vault

</td><td>

The Vault workflow supports generating custom data patterns from text descriptions to streamline your workload, checking role access for an encrypted column to monitor your instance’s encryption access posture, and scheduling Data Discovery jobs to detect sensitive data.

</td><td>

Now Assist for Vault

</td></tr><tr><td>

Other

</td><td>

The Other workflow accommodates additional plugins and skills that don't fit into any other workflow.

</td><td>

Now Assist for Zero Copy Connector

</td></tr></tbody>
</table>Now Assist products include some or all of the following foundational platform tools for Now Assist. For more information, see [Now Assist skills in the Platform workflow](../../now-assist-skills/concept/now-assist-on-now-platform.md).

-   Administrators install plugins, manage skills, and analyze usage and performance with the [Overview tab in Now Assist Admin](configuring-now-assist.md).
-   Users can take advantage of Now Assist skills by using the [Now Assist panel](now-assist-panel-overview.md) on the instance.
-   Use Now Assist in AI Search to generate answers for AI Search.
-   Use Now Assist for Mobile to run generative AI skills in a mobile environment.
-   Use Now Assist in Virtual Agent to create conversational catalog experiences and author topics that use LLM topic discovery.
-   Developers can use the [Generative AI Controller](../../generative-ai-controller/concept/generative-ai-controller.md) to integrate generative AI features in custom flows and conversations by using your own third-party large language model \(LLM\) licenses.

The following diagram shows what's available in the Now Assist framework.

![The Now Assist framework includes Now Assist Admin, Now Assist panel, and Generative AI Controller. Framework components become available once you install a product such as Now Assist for IT Service Management (ITSM).](../images/now-assist-framework-overview.png "Now Assist framework")

## Now Assist benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Leverage the power of search with the Now LLM generative AI model to answer questions in user searches with actionable AI-generated summaries of relevant knowledge articles.|Now Assist in AI Search|Everyone|
|Install and configure Now Assist applications and the skills they provide.|[Now Assist Admin console](../../now-assist-admin/task/install-now-assist-feature-plugins.md)|Administrators|
|Choose which skills to turn on, and which users can access them.|[Now Assist Admin console](../../now-assist-admin/task/configure-a-now-assist-skill.md)|Administrators|
|Monitor the usage and performance of generative AI features and capabilities offered under Now Assist.|[Now Assist Analytics](../../now-assist-analytics/concept/now-assist-analytics.md)|Administrators|
|Access generative AI skills in context through a user-friendly interface.|[Now Assist panel](now-assist-panel-overview.md)|Everyone|
|Use Now Assist skills on mobile devices.|Now Assist for Mobile|Everyone|
|Customize your workflows and use your own third-party LLM license.|[Generative AI Controller](../../generative-ai-controller/concept/generative-ai-controller.md)|Administrators or developers|
|Use Now Assist in other platform features.|[Now Assist skills in the Platform workflow](../../now-assist-skills/concept/now-assist-on-now-platform.md)|Administrators or developers|
|Monitor Now Assist consumption on your instance.|Monitoring Now Assist usage in Subscription Management|Administrators|

