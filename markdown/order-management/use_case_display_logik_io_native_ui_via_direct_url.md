---
title: Use case: Displaying the CPQ native UI via direct URL
description: Learn how to initialize a configuration UI using a URL instead of an external library.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use cases, Using CPQ, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Use case: Displaying the CPQ native UI via direct URL

Learn how to initialize a configuration UI using a URL instead of an external library.

This article provides an outline of how a CPQ Configuration UI can be initialized using a configuration URL rather than relying on an external library \(such as easyXDM\).

The base configuration URL is in the format `https://{tenant}.logik.io/ui/configure/{configurableProductId}`, where:

-   \{tenant\} is the CPQ tenant that you are using, which can be found in Salesforce or if using CPQ headless, the base URL of the Admin experience
-   \{configurableProductId\} is the Product ID of the CPQ Configurable Product to use for the configuration

Example configuration URL: `https://demo6.demo.logik.io/ui/configure/01t5f000006QKynAAG?v=1`

## Configuration URL query parameters

Additional settings and data can be passed via URL query parameters.

<table><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Required

</th><th>

Values / Notes

</th></tr></thead><tbody><tr><td>

v

</td><td>

Version

</td><td>

true

</td><td>

1

</td></tr><tr><td>

pid

</td><td>

Pricebook ID

</td><td>

 

</td><td>

Salesforce Pricebook ID

</td></tr><tr><td>

id

</td><td>

Configuration ID

</td><td>

 

</td><td>

Logik UUID of existing configuration to load

</td></tr><tr><td>

lid

</td><td>

Quote Line ID

</td><td>

 

</td><td>

Salesforce Quote Line ID

</td></tr><tr><td>

qid

</td><td>

Quote ID

</td><td>

 

</td><td>

Salesforce Quote ID

</td></tr><tr><td>

log

</td><td>

Log Execution \(Flightpath\)

</td><td>

 

</td><td>

None \| Available \| ActiveThis parameter is case sensitive.

</td></tr><tr><td>

cm

</td><td>

Committed Configuration ID

</td><td>

 

</td><td>

When a contracted order is amended, CPQ identifies the prior configuration ID. That ID then becomes the committed Configuration ID.

</td></tr><tr><td>

fields

</td><td>

Fields

</td><td>

 

</td><td>

Array of field objects. For example, `[{"variableName ":"textField1","value":"test"},{…}]`

 In JavaScript, use encodeURI to ensure any special characters are escaped

</td></tr><tr><td>

ac

</td><td>

Action Context

</td><td>

 

</td><td>

null or "Amendment"

</td></tr><tr><td>

e

</td><td>

Editability

</td><td>

 

</td><td>

One of:-   "Tm9uZQ" \(None\)
-   "QXZhaWxhYmx l" \(Available\)
-   "QWN0aXZl" \(Active\)

This parameter is case sensitive.

</td></tr><tr><td>

layout

</td><td>

Layout Variable Name

</td><td>

 

</td><td>

Name of the layout to load from the blueprint of the configurable product

</td></tr><tr><td>

return

</td><td>

Return URL

</td><td>

 

</td><td>

URL to set window.location to on save or cancel. Needs to be encoded and URL-safe

</td></tr><tr><td>

rt

</td><td>

Runtime Token

</td><td>

See note below

</td><td>

Runtime token from CPQ Admin Setup

</td></tr><tr><td>

rta

</td><td>

Runtime API URL

</td><td>

 

</td><td>

Needs to be encoded and URL-safe. Highly recommended if using the runtime token parameter. Use encodeURI in Javascript to ensure that any special characters are escaped, especially when calling an API.

</td></tr><tr><td>

currency

</td><td>

Currency ISO Code

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>**Note:** When using the runtime token \(rt\) parameter, it is highly recommended to also include the rta as well to ensure that all of the requests can be authenticated when using the Firefox or Safari browsers.

If you are not accessing the configuration URL where you have already authenticated \(via Salesforce or directly\), the runtime token will be required to authenticate. If you are accessing the configuration URL before authenticating through the associated SFDC environment or accessing the configuration URL for a headless environment, the CPQ tenant URL needs to be listed as an origin for the leveraged runtime client. For example, `https://<yourLogikUrl>.test.logik.io`.

If the version parameter is not included, the UI will not load, and you will receive the following error: "Error: A version must be specified."

If a return URL is not included, the UI will broadcast a postMessage up to the parent, with the UUID on save \(such as `{"uuid": "8b88c843-d10b-468b-8c49-17f8c9698799"}`\) and an empty object on cancel \(`{}`\).

## Using the configuration URL

The configuration URL can be used either as the top level window or in an iframe on a page.

Unlike when using the easyXDM example to initialize a configuration, configuration data will not be sent to the browser console in Javascript when using the configuration URL.

Considerations for using the configuration URL as the top level window URL:

-   On the save or cancel actions, the CPQ UI will make the call to the CPQ backend to save or cancel the configuration. These calls can be viewed in the Network tab of the browser to see the data being sent and returned.
-   If a return URL is included, the UI will attempt to set the window location to that URL on save \("Quote"\) or on cancel.

Considerations for using the configuration URL in an iframe:

-   If a return URL is included, the UI will attempt to set the window location to that URL on save \("Quote"\) or on cancel. If a return URL is not included, the CPQ UI will broadcast a postMessage up to the parent, with the UUID on save \(such as `{"uuid": "8b88c843-d10b-468b-8c49-17f8c9698799"}`\) and an empty object on cancel \(`{}`\).
-   For either implementation, after executing the save or cancel action, the configuration is removed. Subsequent save actions will result in a 404 error with an error message: "No Rules Engine found for Tenant with Config ID '&lt;Logik UUID&gt;'. Subsequent cancel actions will also result in a 404 error.

## Configuration result

The result of the saved Configuration can be accessed by using the GET API to retrieve the BOM data.

[Postman Collection with Config API URL](https://drive.google.com/file/d/1uHyPsUROr7JI84RZ0Ac2ogqcl7-kxL8J/view?usp=share_link)

The result can be sent to a downstream system via Webhook. See [Webhooks](cpq-webhooks.md).

**Parent Topic:**[Use cases](use-cases.md)

