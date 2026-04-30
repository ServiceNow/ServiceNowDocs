---
title: Creating your own API connectors in Security Posture Control
description: Create your own Security Posture Control \(SPC\) API connectors using the connector framework that is included with the application.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2026-01-14"
reading_time_minutes: 2
breadcrumb: [Use the workspace, Security Posture Control, Security Operations]
---

# Creating your own API connectors in Security Posture Control

Create your own Security Posture Control \(SPC\) API connectors using the connector framework that is included with the application.

## Overview for the connector builder framework

## Benefits

Create your own SPC API connectors quickly to help you integrate with security tools and import asset data that is based on the unique requirements of your environment. Use imported data to help you monitor your overall security posture and identify assets that are missing key security tools.

The connector framework includes the following features.

-   Starting with Yokohama Patch 11, you have the option to get guidance for selecting a template with a Now Assist skill for this step. See [Exploring Now Assist for Vulnerability Response](../../now-assist-vulnerability-response/concept/exploring-ai-for-now-assist-for-vulnerability-response.md) for more information about the generative AI skill and [Using Now Assist for Vulnerability Response in Security Posture Control](../../now-assist-vulnerability-response/concept/using-now-assist-api-connector.md) about using the skill in connector framework.
-   A step-by-step process to guide you through the connector builder.
-   A single place to build and maintain all your SPC integrations to import custom data into your CMDB.
-   After you publish them, monitor your API connectors on the SPC API Integrations tab in the **Security Posture Control** workspace.

## The API connector builder

You use the Connector builder in the Security Posture Control workspace to create and publish your customized API connectors.

## Prerequisites

Before you start creating your API connector, you might prefer to set up any credentials for the service \(vendor\) that you want to implement with and have their API documentation and credentials handy as you work through the Connector builder. See [Enter metadata](../task/spc-sgc-template-stepper1.md) for more information.

## Required applications and plugins

The following applications and plugins are required.

For more information about applications in the ServiceNow® Store, see [Exploring the ServiceNow Store](https://www.servicenow.com/docs/access?context=exploring-servicenow-store&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and downloading and activating applications [Download an application from the ServiceNow Store for the first time](../../security-incident-response/reference/download-app-first-time.md).

**Note:** If you're downloading applications to non-production or development instances, it's not necessary to get entitlements.

Role required: admin for download, installation, and activation of all applications and plugins.

|Application|Application ID and version|
|-----------|--------------------------|
|Security Posture Control API Connectors|sn\_spc\_cxf v2.0.0|
|Security Posture Control|sn\_sec\_spc\_core v7.0.1|
|Asset Security Posture Management|sn\_sec\_caasm v5.5.1|
|Mitigation Controls Monitoring|sn\_sec\_mit\_ctrl v4.1.4|
|Integrations Commons for CMDB|sn\_cmdb\_int\_util v2.20.0|

|Plugin|Plugin ID|
|------|---------|
|IntergationHub Action Template - Data Stream|com.glide.hub.action\_type.datastream|

## Required roles

Role required: admin

Assign the sn\_sec\_spc\_core.developer role to the users who you want to view and configure SPC API connectors with the Connector builder in the Security Posture Control workspace.

Assign the sn\_spc\_cxf.admin role if you want users to configure SPC API connectors with advance scripting with the Connector builder.

See [Install the supported applications for Security Posture Control](https://www.servicenow.com/docs/bundle/zurich-security-management/page/product/security-posture-control/task/spc-install.html) for information about assigning roles to Security Posture Control groups.

