---
title: Configure CORS \(Cross-Origin Resource Sharing\) rules before embedding ServiceNow components
description: Configure a CORS rule to enable cross-domain requests between ServiceNow components and the website that you want to embed the web components.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up Web Embeddables, Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Configure CORS \(Cross-Origin Resource Sharing\) rules before embedding ServiceNow components

Configure a CORS rule to enable cross-domain requests between ServiceNow components and the website that you want to embed the web components.

## Before you begin

You must have the following setup in to configure CORS rules for components:

-   You must activate the ServiceNow components. For more information, see [Activate Web Embeddables](act-web-embeddables.md).
-   At least one ServiceNow component configured on your instance.

Role required: admin

## About this task

You can use the existing CORS rules to enable secure communication between ServiceNow components and the external website. You can also set up a CORS rule so that ServiceNow components are able to make cross-origin requests to retrieve dynamic translations. For more information on creating and defining CORS rules, see Define a CORS rule.

## Procedure

1.  Navigate to **All** &gt; **Web Embeddables** &gt; **Configure** &gt; **CORS rules**.

2.  In the **Domain name** field, enter the domain name that you want to embed the component.

3.  Select **Check status**.

    Displays all the CORS rules that must be configured. It shows both configured and unconfigured URLs.

4.  Select **Configure CORS rules**.

    Initiates CORS rules for all the unconfigured URLs.

    **Note:** The confirmation message `CORS rules configured successfully` appears.


## Result

The domain name that you’ve entered is configured with CORS rules and can be used to embed the component.

**Related topics**  


[bundle-crapiref.t_DefineACORSRule]

