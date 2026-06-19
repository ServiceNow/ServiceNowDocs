---
title: Configuring Creator Studio
description: Admins need to install Creator Studio before it can be configured for users to start building apps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/creator-studio/configuring-creator-studio.html
release: australia
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Configuring Creator Studio

Admins need to install Creator Studio before it can be configured for users to start building apps.

## Configuration overview

The following is a general overview of installing and configuring Creator Studio.

1.  Decide on an instance strategy, for example, what are your development \(non-production\) and production instances. For more information, see [Creator Studio development instance strategy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/creator-studio-instance-strategy.md).
2.  Download Creator Studio from the ServiceNow Store and install it. For more information, see [Installing Creator Studio from the ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/installing-creator-studio-from-the-store.md).
3.  Run Guided Setup to configure administration and collaboration. For more information, see [Configure Creator Studio using Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/config-creator-studio-guided-setup.md).
4.  Ensure all users who need access have the correct role. For more information, see [Creator Studio roles and personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/roles-creator-studio.md).

## Using Guided Setup to implement Creator Studio

Guided Setup provides a sequence of tasks that help you configure Creator Studio on your ServiceNow instance. Currently, the Guided Setup helps you to set up the following:

-   The admin group to define who can administer Creator Studio
-   Collaboration descriptors to manage what app owners and editors can do
-   Who has full and restricted access to creating apps in Creator Studio

To open Guided Setup for Creator Studio, navigate to **All** &gt; **App Engine** &gt; **Guided Setup – Shared**.

For more information, see .

## Catalog configuration requirement for Creator Studio

To ensure that forms appear correctly for users, the non-production and production instances must have the same Service Catalog and all of its categories.

## Configuring Virtual Agent chatbot previews

If you want forms to appear in the Virtual Agent chatbot, you must install the necessary plugins. For more information, see .

-   **[Installing Creator Studio from the ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/installing-creator-studio-from-the-store.md)**  
Installing Creator Studio from the ServiceNow Store makes it available for people to build apps on your instance.
-   **[Configure Creator Studio using Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/config-creator-studio-guided-setup.md)**  
So you've installed Creator Studio on an instance. Now what? You must configure it before users can start building apps.
-   **[Configuring Pipelines and Deployments to deploy apps built in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/creator-studio-configuring-pipelines.md)**  
You can install Pipelines and Deployments and configure a controller instance to deploy apps built in Creator Studio to production instances.
-   **[Creator Studio roles and personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/roles-creator-studio.md)**  
Roles control what everyone you work with can do in Creator Studio. Administrators assign roles to give team members permission to configure or use Creator Studio.
-   **[Creator Studio and domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/creator-studio-domain-separation.md)**  
Domain separation is not supported in Creator Studio. This means that you can't separate data, processes, and administrative tasks into distinct groups, called domains, within the ServiceNow AI Platform.
-   **[Configuring form generation in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/creator-studio-configure-now-assist.md)**  
Install and configure Now Assist for Creator in Creator Studio.

**Parent Topic:**[Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/creator-studio-landing.md)

