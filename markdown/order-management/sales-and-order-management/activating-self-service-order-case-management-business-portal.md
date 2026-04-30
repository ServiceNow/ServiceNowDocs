---
title: Installing apps for self-service order case management on the Business Portal
description: Install the necessary plugins based on the self-service options that you want to offer customers for managing order cases on the Business Portal.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring the Business Portal, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Installing apps for self-service order case management on the Business Portal

Install the necessary plugins based on the self-service options that you want to offer customers for managing order cases on the Business Portal.

The apps that must be installed from the ServiceNow Store to enable your customers to create and view order cases from the Business Portal:

-   Order Case Self Service \[sn\_ord\_case\_ss\]
-   Order Case Playbook \[sn\_ord\_case\_pb\]

These plugins have the following dependencies:

-   Customer Service Portal \[com.snc.customer\_service\_portal\]
-   Order Operations Case Management \[sn\_order\_case\]
-   Playbooks for Customer Service Management \[sn\_csm\_playbook\]

If you want your customers to be able only to view order cases in the Business Portal, you do not need to install the Order Case Playbook \[sn\_ord\_case\_pb\] plugin and the Playbooks for Customer Service Management \[sn\_csm\_playbook\] plugin is not necessary.

You must also activate the Business Portal to make it accessible for your customers. The Business Portal is inactive by default. For more information, see [Configure Business Portal](https://www.servicenow.com/docs/access?context=configure-business-portal&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

