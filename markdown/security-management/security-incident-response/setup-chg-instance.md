---
title: Setup Splunk environment
description: ServiceNow Security Operations Integration enables seamless integration between Splunk and ServiceNow Security Operations. To set up or change the ServiceNow instance where new security incidents and security events are created, use the setup action in the application list.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Security Operations add-on for Splunk overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Setup Splunk environment

ServiceNow Security Operations Integration enables seamless integration between Splunk and ServiceNow Security Operations. To set up or change the ServiceNow instance where new security incidents and security events are created, use the setup action in the application list.

## Before you begin

Install **Event Management** plugin to access the em\_event table.

Role required: sn\_si.integration\_user, sn\_si.analyst

## About this task

**Note:** You're not required to have a profile for this addon. It directly creates the security event or the security incident.

If you want to export events manually and on-demand from your Splunk Enterprise console for the integration, download, install, and set up the ServiceNow Security Operations Integration add-on from Splunkbase in your Splunk Enterprise console.

This ServiceNow extension addon is required so that security incidents can be created from manually exported events in your ServiceNow AI Platform instance. This ServiceNow ServiceNow Security Operations Integration add-on is available on [splunkbase](https://splunkbase.splunk.com/).

## Procedure

1.  Log in to [Splunk Enterprise](https://splunk.secops-eng.com:8000/en-GB/app/launcher/home).

2.  Select **Manage Apps** gear icon on the menu drop-down list.

3.  In the list of applications, search for **ServiceNow** apps using the filter.

4.  Look for the **ServiceNow Security Operations Integration** add-on, and select the corresponding **Set up** action.

5.  On the form, fill in the fields.

<table id="choicetable_rrp_bwk_kdb"><thead><tr><th align="left" id="d484118e159">

Field

</th><th align="left" id="d484118e162">

Description

</th></tr></thead><tbody><tr><td id="d484118e168">

**URL**

</td><td>

URL of the ServiceNow instance for your Splunk Enterprise Security console or Splunk Cloud instance.

</td></tr><tr><td id="d484118e186">

**Auth type**

</td><td>

Authentication method to be used for API requests. The available options include:-   **Basic Authentication**: Uses username and password to authenticate requests.
-   **OAuth 2.0 Authentication**: Uses access tokens to authenticate requests.


</td></tr><tr><td id="d484118e207">

**Basic Authentication**

</td><td>

 

</td></tr><tr><td id="d484118e215">

**Username**

</td><td>

Username of the user.User with the \(sn\_si.integration\_user, sn\_si.analyst\) role should be present in the ServiceNow instance specified in the preceding URL field.

</td></tr><tr><td id="d484118e230">

**Password**

</td><td>

Password of the user.User with the \(sn\_si.integration\_user, sn\_si.analyst\) role should be present in the ServiceNow instance specified in the preceding URL field.

</td></tr><tr><td id="d484118e244">

**Confirm Password**

</td><td>

Renter the password to confirm it.

</td></tr><tr><td id="d484118e253">

**OAuth 2.0 Authentication**

</td><td>

 

</td></tr><tr><td id="d484118e261">

**Client ID**

</td><td>

Client ID of the app created on the ServiceNow Server. For information on how to get the Client ID, see [Configure Application Registry on the ServiceNow instance](configure-application-registry-splunk.md)

</td></tr><tr><td id="d484118e279">

**Client Secret**

</td><td>

Client Secret of the app created on the ServiceNow Server. For information on how to get the Client Secret, see [Configure Application Registry on the ServiceNow instance](configure-application-registry-splunk.md)

</td></tr><tr><td id="d484118e297">

**Redirect URL**

</td><td>

The URL to be redirected to. Copy and paste this URL in the redirect URL field of the Application Registries record.

</td></tr><tr><td id="d484118e309">

**Optional Proxy**

</td><td>

 

</td></tr><tr><td id="d484118e317">

**Proxy URL**

</td><td>

Proxy URL for your Splunk Enterprise Security console or Splunk Cloud instance.

</td></tr><tr><td id="d484118e332">

**Port**

</td><td>

Address of the port.

</td></tr><tr><td id="d484118e341">

**Username**

</td><td>

Username that you created for the Proxy account on the Splunk Enterprise Security console.

</td></tr><tr><td id="d484118e353">

**Password**

</td><td>

Password that you created for the Proxy account on the Splunk Enterprise Security console.

</td></tr><tr><td id="d484118e365">

**Confirm Password**

</td><td>

Renter the password to confirm it.

</td></tr><tr><td id="d484118e375">

**Logging Level Setup**

</td><td>

 

</td></tr><tr><td id="d484118e383">

**Logging Level**

</td><td>

The level of reporting logs generated by the integration, meaning the name of the type of information. You can also update the value to the following options:-   **info**
-   **error**
-   **warn**
-   **debug**
 By default, the value is **info**.

</td></tr><tr><td id="d484118e417">

**API Selection**

</td><td>

 

</td></tr><tr><td id="d484118e425">

**API Selection**

</td><td>

Select one of the following APIs:-   Table API
-   Import Set API


</td></tr></tbody>
</table>    ![ServiceNow Security Operations Integration set up on Splunk](../image/splunk-es-config.gif)

6.  Select **Save**.


## What to do next

[Using ServiceNow Security Operations Integration add-on](using-sn-secops-int-addon.md)

