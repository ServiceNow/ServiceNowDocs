---
title: Configuring Public Sector Digital Services
description: Set up Public Sector Digital Services to enable government agents and service managers to provide government services to constituents, businesses, and other agencies.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-02-10"
reading_time_minutes: 5
breadcrumb: [Public Sector Digital Services \(PSDS\)]
---

# Configuring Public Sector Digital Services

Set up Public Sector Digital Services to enable government agents and service managers to provide government services to constituents, businesses, and other agencies.

## Installing and Setting up Public Sector Digital Services

Configuring Public Sector Digital Services involves several main tasks:

-   Installing and setting up the Public Sector Digital Services Core application and the Performance Analytics content pack.
-   Setting up one or more playbooks in the CSM Configurable Workspace for use with Public Sector Digital Services.
-   Configuring additional features for public sector use, such as Virtual Agent, Engagement Messenger, and custom service definitions.

As a user with the admin role, complete the following main configuration tasks to set up Public Sector Digital Services.

|Configuration task|Description|
|------------------|-----------|
|[Install and configure the Public Sector Digital Services Core application](configure-psds-core.md)|Install and configure the Public Sector Digital Services Core application \(sn\_gsm\) plugin from the ServiceNow Store. It provides the public sector features used by constituents, businesses, agency agents, government agents, and government service managers.|
|[Install the Performance Analytics Content Pack for Public Sector Digital Services](../../../use/dashboards/application-content-packs/psds-install.md)|Install the Performance Analytics Content Pack for Public Sector Digital Services \(com.sn\_public\_sector\_digital\_services\_pa\) plugin from the ServiceNow Store. This application provides dashboards that government agents and service managers can use to track government cases and monitor government services offered to and received by constituents.|
|[Install and configure Now Assist for Public Sector Digital Services \(PSDS\)](now-assist-psds-configuring.md)|Install and configure the Now Assist for Public Sector Digital Services \(PSDS\) application so that your agents can use the generative AI skills in CSM Configurable Workspace and in Core UI.|
|[Install and configure the Service Request Playbook application](configuring-service-request-playbook.md)|Install and configure the Service Request Playbook application \(sn\_gsm\_srvc\_req\) plugin from the ServiceNow Store. It provides an end-to-end workflow for handling non-emergency service requests submitted by public sector end users.|
|[Install and configure the Information Request Playbook application](configuring-information-request-playbook.md)|Install and configure the Information Request Playbook application \(sn\_gsm\_info\_req\) plugin from the ServiceNow Store. It provides an end-to-end workflow for handling public record information requests submitted by public sector end users.|
|[Install and configure the License and Permit Playbook application](configuring-license-permit-playbook.md)|Install and configure the License and Permit Playbook application \(sn\_gsm\_license\_permit\) plugin from the ServiceNow Store. It provides government agents with a pre-defined process for handling and resolving license and permit requests submitted by public sector end users.|
|[Install and configure the Social Benefits Playbook application](configuring-social-benefit-playbook.md)|Install and configure the License and Permit Playbook application \(sn\_gsm\_license\_permit\) plugin from the ServiceNow Store. It provides government agents with a pre-defined workflow for reviewing applications for the social benefit programs offered by your agency.|

## Other configuration tasks

In addition to installing the public sector application and playbooks, you can configure other features for public sector use:

-   **ServiceNow® Virtual Agent**

    Virtual Agent, which is included with a public sector subscription, provides end-user assistance through automated conversations in chat channels.

    The Public Sector Digital Services Core application offers several prebuilt public sector components \(topic blocks\) that conversation designers can use to create Virtual Agent conversations.

    The Service Request Playbook application provides a prebuilt Virtual Agent conversation topic, Create a service request, to help constituents submit non-emergency service requests.

    For details on configuring Virtual Agent for public sector use, see [Configure Virtual Agent for Public Sector Digital Services](psds-configuring-va.md).

-   **Service definitions**

    A service definition enables you to map a public service, information service, or license and permit request service to the list of services your agency offers for resolving that request.

    As an admin, you can create service definitions that connect the services your agency offers to the services being requested by a constituent or business. When you create a service definition, you can configure the case management processes, such as the case types, for executing those services.

    For more information, see [Service definitions for Public Sector Digital Services](psds-service-definitions.md).

-   **Relabel menu items in CSM Configurable Workspace after upgrade**

    After you upgrade your instance to a new release, certain menus and menu items in the CSM Configurable Workspace might not be labeled appropriately for public sector use. You can relabel the following items for public sector use by changing them in the UX list categories for Customer and Service Organizations.

    For details, see [Relabel items for public sector use after upgrade](../task/psds-relabel-after-upgrading.md).


