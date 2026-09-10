---
title: Prepare to run the Salesforce collector
description: Set up access for cataloging Salesforce resources by configuring user credentials, security tokens, and connected applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/prepare-to-run-the-salesforce-collector.html
release: australia
topic_type: task
last_updated: "2026-07-28"
reading_time_minutes: 1
keywords: [Salesforce collector, connected application, OAuth, security token]
breadcrumb: [Salesforce metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the Salesforce collector

Set up access for cataloging Salesforce resources by configuring user credentials, security tokens, and connected applications.

## Before you begin

Role required: admin

## About this task

Before running the Salesforce collector, configure the necessary access credentials and permissions in Salesforce.

## Procedure

1.  Set up a user that the collector will use to connect to Salesforce.

2.  Set up a [security token](https://help.salesforce.com/s/articleView?language=en_US&id=sf.user_security_token.htm&type=5).

3.  Set up a connected application for OAuth.

    When setting up the connected application, confirm that the following scopes are enabled:

    -   Access Lightning applications
    -   Manage user data via APIs
    -   Perform requests at any time
4.  Follow the [Salesforce documentation](https://help.salesforce.com/s/articleView?id=xcloud.connected_app_client_credentials_setup.htm&type=5) to get the client credentials.

5.  Confirm that the user set up for running the collector has authorization to use APIs and the connected application.


**Parent Topic:**[Salesforce metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/salesforce-metadata-collector.md)

