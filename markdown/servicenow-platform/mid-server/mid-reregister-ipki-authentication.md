---
title: Reregister MID Servers to restore IPKI authentication
description: Generate a registration key and use it to get a new IPKI certificate for an existing MID Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/mid-server/mid-reregister-ipki-authentication.html
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-10-29"
reading_time_minutes: 1
keywords: [IPKI, MID Server reregistration, registration key]
breadcrumb: [MID Server IPKI authentication, Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Reregister MID Servers to restore IPKI authentication

Generate a registration key and use it to get a new IPKI certificate for an existing MID Server.

## Before you begin

Role required: admin or agent\_admin

## About this task

Reregister a MID Server when its IPKI certificate has expired, been revoked, is no longer valid, or when the keystore is corrupted.

A registration key lets the instance issue one new certificate. The key is single use and expires within 24 hours of creation.

## Procedure

1.  On your instance, navigate to **Workspaces** &gt; **ITOM Infra Services Workspace**.

2.  Select the **MID Servers** icon in the navigation panel.

3.  On the **MID Onboarding** tab, select the **Generate single-use registration key** link.

4.  On the **Select MID Server user to generate key** dialog, in the **MID Server user** list, select the MID Server user for which you're generating the key.

5.  Select **Generate registration key**.

6.  Copy the registration key and the sys\_id of the user.

7.  On the MID Server host, open `config.xml` in the agent folder and set these parameters:

    ```
    <parameter name="mid.ipki.enabled" value="true"/>
    <parameter name="mid.ipki.registration_key" value="<registration_key>"/>
    <parameter name="mid.ipki.user" value="<user_sys_id>"/>
    ```

8.  Restart the MID Server.

    The MID Server requests a new certificate with the key and installs it.


## Result

The MID Server has a new IPKI certificate and authenticates to the instance again. On the MID Server record, the **Validated** field is set to **true** and the **Status** field is set to **Up**.

**Parent Topic:**[MID Server IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-ipki-authentication.md)

