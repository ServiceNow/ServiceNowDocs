---
title: Installing the Application Repository store app on an air-gapped instance
description: Because self-hosted, air-gapped customers don't allow their instances to communicate with external networks, they don’t install the Application Repository directly from the ServiceNow Store. These customers should use the following procedure instead.
locale: en-US
release: australia
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application Repository for self-hosted, air-gapped customers, ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Installing the Application Repository store app on an air-gapped instance

Because self-hosted, air-gapped customers don't allow their instances to communicate with external networks, they don’t install the Application Repository directly from the ServiceNow® Store. These customers should use the following procedure instead.

## Before you begin

**Note:** Customization of the Application Repository is not supported or recommended.

Role required: You will need the maint role to install and configure, and then just the admin role once the configuration is complete.

**Warning:** If your instances are already connected to the public ServiceNow® Store, you should not install the Application Repository. Doing so causes these instances to lose access. This product is intended for customers who can't connect to the public store.

**Note:** Install on a dedicated ServiceNow® instance separate from your other instances.

## Procedure

1.  Install the application repository using the instruction in the following Knowledge Base article: [How On-Prem Customers Can Request a Store App](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0745101).

2.  After installing, complete the steps in [Configure the application repository on an air-gapped instance](configure-app-repo-air-gapped.md).


