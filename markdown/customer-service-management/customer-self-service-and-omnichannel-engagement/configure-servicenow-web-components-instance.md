---
title: Configure the ServiceNow component instance
description: Configure the component instance so that your user can embed the components onto their website to access component-related data in real-time.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Set up Web EmbeddablesWeb Embeddable, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Configure the ServiceNow component instance

Configure the component instance so that your user can embed the components onto their website to access component-related data in real-time.

## Before you begin

You must have the following setup to configure ServiceNow component instance:

-   Enable Web Embeddables in your instance. For more information, see [Activate Web Embeddables](act-web-embeddables.md)
-   [Set up a custom URL as the instance URL](set-up-custom-url.md)
-   Authenticate the ServiceNow components using OpenID Connect \(OIDC\) or non OIDC authentication. For more information, see [Authenticate the ServiceNow components using OIDC](authenticate-sn-webcomponents-oidc.md) and [Non OIDC authentication for ServiceNow components](../concept/auth-sn-webcomponents-non-oidc.md).

Role required: sn\_embeddable\_core.emb\_admin

## About this task

This procedure outlines the high-level steps that you must follow to set up Web Embeddables component instance.

## Procedure

1.  Navigate to **All** &gt; **Web Embeddables** &gt; **Homepage**.

2.  In the Homepage, select **Create module** or use the existing module.

    For more information on how to create a new module, see [Create a module](../concept/create-we-module.md).

3.  On the module page, in the Components tab, create a group and add a component instance.

    For more information on how to create a group and then add a component instance, see [Create a group and add a component instance](we-create-group-and-add-comp-instance.md).

4.  Toggle the **Show static preview** option to see a visual representation of a component when a live preview isn’t available.

    **Note:** The Show static preview option isn’t available for Data visualization component.

5.  Configure the component instance properties.

    The Preview tab displays real-time data according to choices set in the component properties.

6.  Select the **CORS rules** tab to configure the CORS rules.

    For more information about configuring CORS rules, see [Configure CORS \(Cross-Origin Resource Sharing\) rules before embedding ServiceNow components](configure-cors-for-web-components.md).

7.  Select **Component** tab.

8.  Select **Get embed code**.

    A pop-up window appears to display both Global code and Component code.

9.  In the Global code tab, review the generated code and select the **Copy global code**.

    The global code must be added once to your third-party website.

10. In the Component code tab, review the generated code and select the **Copy component code**.

11. In the Component Code tab, slide the **Enable event handler** toggle switch to handle events triggered by the user interactions on the webpage.

    **Note:** Enabling the event handler also modifies the component code.


## Result

The global and component codes are ready to be shared with the third-party admin to embed component instance on their third-party webpage.

## What to do next

[Embed ServiceNow components instance on the third-party website](embed-web-components-third-party-website.md)

