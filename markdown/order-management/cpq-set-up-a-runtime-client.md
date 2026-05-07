---
title: Set up a runtime client
description: Configure a runtime client. Doing so creates a token that you can use to authenticate runtime calls. This can be useful when CPQ is embedded in a VisualForce page.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ admin settings, CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# Set up a runtime client

Configure a runtime client. Doing so creates a token that you can use to authenticate runtime calls. This can be useful when CPQ is embedded in a VisualForce page.

## Before you begin

Role required: admin

## About this task

Runtime clients can be set up that provide a token for authentication of runtime calls when launching CPQ outside of the regular workflow. For example, CPQ may be started through a quote in Salesforce when embedding CPQ in a Visualforce page, Lightning web component, or HTML page.

**Note:** This authentication can be used only by end users launching a CPQ configuration in runtime. To authenticate admin calls, users should leverage [Admin API Keys](https://logikio3.my.site.com/s/article/Logik-io-admin-API-Keys).

## Procedure

1.  In the Utilities tab of the navigation pane, click **Runtime clients**.

2.  Click **New**.

    ![Runtime clients user interface](../images/cpq-runtime-client.png)

3.  Name the runtime client.

    ![Add a runtime client interface](../images/cpq-runtime-client-add.png)

4.  Set the user ID.

    Setting the user ID attaches the ID to all calls authenticated by this client. This can help track the origin of the calls.

5.  Set whether the permissions apply to Config or Config and Flightpath.

    Config enables launching configurations. Flightpath helps with debugging by allowing for accessing the flightpath data of the configuration.

6.  Set an expiration date for the runtime client \(optional\).

    The expiration date can be changed to extend or shorten the time frame during which this token can be used.

7.  Add a URL, such as `https://<yourLogikUrlName>.<sector>.logik.io` or `*.salesforce.com`, and then click `Add Origin`.

    Users must specify the origin of calls made using this token to authenticate. Make sure that the URL has no trailing slash. For example, use \*.salesforce.com and not `*.salesforce.com/`. You can continue adding origins by repeating this step. When all the origins have been entered, click **Save** \(6\).

8.  Click to open the new runtime client, and copy the token.

    ![Edit runtime client](../images/cpq-runtime-client-edit.png)


**Related topics**  


[Use case: Embed CPQ UI in a Salesforce VisualForce page](../concept/use_case_embed_logik_io_ui_in_salesforce_visualforce_page.md)

