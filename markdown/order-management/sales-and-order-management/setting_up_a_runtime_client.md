---
title: Set up a runtime client
description: Configure a runtime client. Doing so creates a token that you can use to authenticate runtime calls. This can be useful when CPQ is embedded within a VisualForce page.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Set up a runtime client

Configure a runtime client. Doing so creates a token that you can use to authenticate runtime calls. This can be useful when CPQ is embedded within a VisualForce page.

Runtime clients can be set up that provide a token for authentication of runtime calls when launching CPQ outside of the regular workflow. For example, CPQ may be started through a quote in Salesforce when embedding CPQ in a Visualforce page, Lightning web component, or HTML page.

**Note:** This authentication can be used only by end users launching a CPQ configuration in runtime. To authenticate admin calls, users should leverage admin API keys. For a more complete discussion of admin API keys, see [Intro to admin API keys](cpq-admin-api-keys.md).

## Create a runtime client

![runtime clients user interface](../images/cpq-runtime-client.png)

1.  Navigate to the Utilities tab of the left hand navigation pane, and click **Runtime Clients**.
2.  Click **New** in the upper right corner.

## Configure the new client

![Add a runtime client interface](../images/cpq-runtime-client-add.png)

1.  Create a name for your runtime client.
2.  Setting the User ID will attach it to any calls authenticated by this runtime client. This may be useful for tracking the origin of the calls.
3.  For Permissions, choose either Config or Config and Flightpath. Config will allow for launching configurations. Flightpath will allow for accessing Flightpath data of the configuration for use with debugging.
4.  Optionally, set an expiration date for the runtime client. This expiration date can be changed to extend or shorten the time frame during which this token can be used.
5.  Users must specify the origins of calls that aree made using this token as authentication. In the origins box, add the desired URL, such as `https://<yourLogikUrlName>.<sector>.CPQ` or `*.salesforce.com`. click `Add Origin` to add the origin, and continue adding more.

    **Note:** Make sure that your origin does not have a trailing slash. For example, use `*.salesforce.com` and not `*.salesforce.com/`.

6.  When all the origins have been added, click `Save`.

When the runtime client has been created, click into it and copy the token:

![Edit runtime client](../images/cpq-runtime-client-edit.png)

**Related topics**  


[Use case: Embed CPQ UI in a Salesforce VisualForce page](use_case_embed_logik_io_ui_in_salesforce_visualforce_page.md)

