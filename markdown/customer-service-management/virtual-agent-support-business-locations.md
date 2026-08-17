---
title: Virtual Agent support for business organizations
description: Customer service agents receive chat requests from your business organization \(formerly business location\) staff members on the CSM Agent Workspace. These agents can assist your staff members to resolve issues and manage the cases more efficiently if your staff members fill out a pre-chat survey first.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/virtual-agent-support-business-locations.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a business organization, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Virtual Agent support for business organizations

Customer service agents receive chat requests from your business organization \(formerly business location\) staff members on the CSM Agent Workspace. These agents can assist your staff members to resolve issues and manage the cases more efficiently if your staff members fill out a pre-chat survey first.

**Important:** Some table and field labels have been changed across recent releases. For a mapping of former labels to current labels, see [Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/renamed-entities.md).

## Overview of pre-chat survey

Before your staff members can use a pre-chat survey to initiate a chat, your administrator must activate the pre-chat configuration for the Business Organization Support Portal. The preconfigured surveys are activated by default in the base system. If your business organization has upgraded the system to manually activate the pre-chat configuration, then staff members can fill in the pre-survey before the chat. To learn more about the pre-chat survey, see [Pre-chat surveys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-pre-chat-overview.md).

You must also assign the service organization contributor \(sn\_customerservice.service\_organization\_contributor\) and location manager \(sn\_customerservice.svc\_location\_manager\_core\) roles to the staff members using the pre-survey chat feature.

Let's say that a staff member with the correct role fills out a pre-chat survey on the Business Organization Support Portal. The chat is then assigned to a customer service agent or Virtual Agent via the advanced work assignment \(AWA\) routing. To learn more about AWA, see [Exploring Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-overview.md).

Before entering into a chat conversation with the staff member, the assigned agent reviews the context of the case so that agents know how to handle the case.

## Pre-chat survey

The pre-chat survey lets staff provide location and support details before a chat. It gives agents context about the case, enabling them to assist more effectively. The pre-chat survey makes the chat more efficient and helpful to your staff. To learn more about how a chat is initiated from the BLSP, see [Chat with Virtual Agent from the Business Organization Support Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/agent-chat-business-location-service-portal.md).

The pre-chat survey isn't displayed for service organization contributors who are associated with a single business organization . The location is picked by default.

The business organizations \(formerly business locations\) that are listed in the pre-chat configuration are limited to the locations that are assigned to the business location manager. You can't select a child business organization.

To learn more about the configuration of the pre-chat surveys, see [Define pre-chat survey configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/ac-configure-pre-chat-surveys.md).

**Related topics**  


[Chat with Virtual Agent from the Business Organization Support Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/agent-chat-business-location-service-portal.md)

