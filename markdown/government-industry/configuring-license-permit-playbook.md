---
title: Install and configure the License and Permit Playbook application
description: Install the License and Permit Playbook application, which enables public sector end users to submit and track license and permit requests and provides government agents with a pre-defined process for handling and resolving these requests. You can then configure the features available for submitting requests and routing requests to agents.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Install and configure the License and Permit Playbook application

Install the License and Permit Playbook application, which enables public sector end users to submit and track license and permit requests and provides government agents with a pre-defined process for handling and resolving these requests. You can then configure the features available for submitting requests and routing requests to agents.

As a user with the admin role, complete the following configuration tasks to set up the License and Permit Playbook, after you install the [Public Sector Digital Services Core](../task/install-public-sector-digital-services-core.md) application.

|Task|Description|
|----|-----------|
|[Install License and Permit Playbook for Public Sector Digital Services](../task/install-psds-license-permit-request-playbook.md)|Install License and Permit Playbook \(com.sn\_public\_sector\_digital\_services\_core\) from the ServiceNow® Store.|
|[Configure service definition catalog items for License and Permit Playbook application](../task/psds-create-service-definition-catalog-item.md)|The Services Offered and Services Received tables have been migrated into the Service Definition table. All Services Offered data must be converted into individual Service Definitions. For more information, see [Services Offered and Services Received Migration Guidance](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1559449).|
|[Enable public sector end users to create a License or Permit request using Virtual Agent](psds-configuring-va.md)|Use Virtual Agent Designer to [publish](https://www.servicenow.com/docs/access?context=publish-virtual-agent-topic&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) the pre-built conversation topic, **Start a License/Permit Application**, which enables end users to submit a license or permit request using the Virtual Agent chatbot.|
|[Automatically route license and permit requests using Advanced Work Assignment](psds-configuring-awa-lpr.md)|Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign license and permit requests to designated agents.|
|[Configure E-sign in License and Permit Playbook](../task/configure-esign-lpr.md)|Configure E-sign to allow constituents the option of drawing their signature when they submit cases through the Government Service Portal.|
|[Configure Eligibility Checklist UI in License and Permit Playbook](../task/psds-configure-eligibility-checklist-ui-lpr.md)|Configure the eligibility checklist UI to allow agents to confirm whether an applicant is eligible for the specific license or permit requested.|
|[Configure decision tables for License and Permit Playbook](../task/psds-configure-decision-tables.md)|Use decisions tables to simplify the pricing configuration of a license or permit request that depends on multiple factors. Decision tables provide a single point where you can create, view, and modify pricing and dependent attributes.|
|[Append price to Pricing Attribute label​](../task/psds-append-price-to-pricing-attribute-label.md#)|Prices are appended to all Boolean Price Attributes by default. Client scripts must added for any price choice attributes​ or price control attributes.|
|[Create Document Templates for License and Permit Playbook](../task/psds-lpr-configure-doc-template.md)|Use the Document Templates application to generate templates for various types of Licenses and Permits issued through the License and Permit Playbook.|

