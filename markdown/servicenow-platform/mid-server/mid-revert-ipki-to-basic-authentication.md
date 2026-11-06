---
title: Revert MID Servers from IPKI to basic authentication
description: Move a MID Server that uses IPKI authentication back to basic authentication by changing its configuration and restarting the service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/mid-server/mid-revert-ipki-to-basic-authentication.html
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-11-03"
reading_time_minutes: 1
keywords: [IPKI, basic authentication, MID Server configuration]
breadcrumb: [MID Server IPKI authentication, Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Revert MID Servers from IPKI to basic authentication

Move a MID Server that uses IPKI authentication back to basic authentication by changing its configuration and restarting the service.

## Before you begin

Role required: admin or agent\_admin

## About this task

Revert a MID Server to basic authentication when it must no longer use IPKI. You need the credentials that the MID Server should use to authenticate to the instance.

## Procedure

1.  Stop the MID Server service.

2.  On the MID Server host, open `config.xml` in the agent folder and set these parameters:

    ```
    <parameter name="mid.ipki.enabled" value="false"/>
    <parameter name="mid.instance.username" value="<user_name>"/>
    <parameter name="mid.instance.password" value="<password>"/>
    ```

    Replace *user\_name* and *password* with the credentials that the MID Server should use.

3.  Start the MID Server service.


## Result

The MID Server authenticates to the instance with basic authentication. The certificate mapping record for the MID Server becomes inactive after the MID Server is running on basic authentication again.

**Parent Topic:**[MID Server IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-ipki-authentication.md)

