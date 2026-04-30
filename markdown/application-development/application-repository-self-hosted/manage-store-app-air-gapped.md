---
title: Application Repository for self-hosted, air-gapped customers
description: This application feature enables self-hosted customers to use their own internal application repository just as cloud customers do. These customers don’t install the Application Repository via the ServiceNow Store; they use an alternative method.
locale: en-US
release: xanadu
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Application Repository for self-hosted, air-gapped customers

This application feature enables self-hosted customers to use their own internal application repository just as cloud customers do. These customers don’t install the Application Repository via the ServiceNow® Store; they use an alternative method.

## Overview

Customers whose instances are hosted on the ServiceNow® cloud have access to an application repository by default via the public ServiceNow® Store. However, self-hosted and air-gapped customers don’t have such access, and thus can’t take advantage of advanced application development features.

**Warning:** Most customers install applications through their networks from the ServiceNow® Store. This topic covers customers who aren’t using networked sources.

The term "air-gapped" refers to the condition when a computer or network has no network interfaces, either wired or wireless, connected to any outside networks. When you want to move data from one source to another, you must use an alternative method. To move data between sources that aren’t on a network, you must use an alternative such as the one described in this topic.

The ServiceNow® Application Repository is a scoped application that can be installed on a customer instance, and enables usage of the latest application development features inside their own private network without the need to communicate with external networks.

## Recommended installation

It is recommended to install the Application Repository on a dedicated instance used only for that purpose. Installing in this way reduces the load on other instances from other transactions and improves the experience of installing other Store applications. After you have successfully installed the application, other networked client instances can publish and install application artifacts to and from this instance.

## Acquiring the application

Before attempting to install the application, ServiceNow self-hosted "air-gapped" customers should reach out to their account representative. They will work with Support and your team to set up the installation process. To learn more, see the Knowledge Base article, [How On-Prem customers can request a Store App](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1641558).

## How the setup process works

Instances are authenticated with the repository via a “pairing” process that stores instance credentials on the server-side, and needs to be done only once per instance. After an instance is “paired” with the repository, it can start interacting with the repository via its various application development features.

