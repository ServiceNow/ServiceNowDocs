---
title: Install and configure the License and Permit Playbook application
description: Install the License and Permit Playbook application, which enables public sector end users to submit and track license and permit requests and provides government agents with a pre-defined process for handling and resolving these requests. You can then configure the features available for submitting requests and routing requests to agents.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Install and configure the License and Permit Playbook application

Install the License and Permit Playbook application, which enables public sector end users to submit and track license and permit requests and provides government agents with a pre-defined process for handling and resolving these requests. You can then configure the features available for submitting requests and routing requests to agents.

As a user with the admin role, complete the following configuration tasks to set up the License and Permit Playbook, after you install the [Public Sector Digital Services Core](../task/install-public-sector-digital-services-core.md) application.

|Task|Description|
|----|-----------|
|[Install License and Permit Playbook for Public Sector Digital Services](../task/install-psds-license-permit-request-playbook.md)|Install License and Permit Playbook \(com.sn\_public\_sector\_digital\_services\_core\) from the ServiceNow® Store.|
|[Configure service definition catalog items for License and Permit Playbook application](../task/psds-create-service-definition-catalog-item.md)|The Services Offered and Services Received tables have been migrated into the Service Definition table. All Services Offered data must be converted into individual Service Definitions. For more information, see [Services Offered and Services Received Migration Guidance](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1559449).|
|[Enable public sector end users to create a License or Permit request using Virtual Agent](psds-configuring-va.md)|Use Virtual Agent Designer to [publish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/publish-virtual-agent-topic.md) the pre-built conversation topic, **Start a License/Permit Application**, which enables end users to submit a license or permit request using the Virtual Agent chatbot. For more information, see [Configure Virtual Agent for License and Permit Playbook](psds-lpr-configure-va.md).|
|[Automatically route license and permit requests using Advanced Work Assignment](awa-psds-overview.md#)|Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign license and permit requests to designated agents.|
|[Configure License and Permit Eligibility Framework in License and Permit Playbook](psds-configure-eligibility-lpr.md)|Configure the pre-eligibility criteria to allow agents to confirm whether an applicant is eligible for the specific license or permit requested.|
|[Configure decision tables for License and Permit Playbook](psds-configure-decision-tables.md)|Use decisions tables to simplify the pricing configuration of a license or permit request that depends on multiple factors. Decision tables provide a single point where you can create, view, and modify pricing and dependent attributes.|
|[Create Document Templates for License and Permit Playbook](../task/psds-lpr-configure-doc-template.md)|Use the Document Templates application to generate templates for various types of Licenses and Permits issued through the License and Permit Playbook.|

