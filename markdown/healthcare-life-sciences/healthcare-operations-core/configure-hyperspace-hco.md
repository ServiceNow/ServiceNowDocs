---
title: Configure the integration settings in the Hyperdrive Client Test Harness for Care Team Portal
description: Once the Care Team Portal is configured, create a launch URL that can then be configured inside the Epic Hyperdrive Client Test Harness for testing.
locale: en-US
release: australia
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Embed Care Team Portal in Epic, Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Configure the integration settings in the Hyperdrive Client Test Harness for Care Team Portal

Once the Care Team Portal is configured, create a launch URL that can then be configured inside the Epic Hyperdrive Client Test Harness for testing.

## Before you begin

Role required: admin

## About this task

You can download the latest Hyperdrive Client Test Harness from fhir.epic.com.

## About this task

Please work with your Epic team and Epic Technical Support for steps on how to configure the FDI integration within Hyperspace.

## Procedure

1.  Log in to the Epic Hyperdrive Client Test Harness.

2.  Select Integration Setup.

3.  Under Integration Type, select **SMART on FHIR**.

4.  In the URL, enter the launch URL for your Care Team Portal.

    For example, `https://<instance-name>.service-now.com/careteam?glide_sso_id=<identity-provider-sysid>`.

5.  In Client ID, enter the production or non-production client ID as appropriate from the FHIR app built on fhir.epic.com.

6.  Set your desired launch type.

7.  In the launch context, add any tokens you want to capture:

    For example:

    -   Key - sysparm\_workstation\_id
    -   %WORKSTATIONID%
    For more information on capturing token data in record producer variables, see [Update variables in record producers to capture tokenized data from Epic Hyperspace](hco-update-variables-portal.md).

8.  Select **Turn Test Integration On**.


## Result

The Care Team Portal has been configured to launch with the Epic Hyperdrive Client Test Harness.

## What to do next

To test the Care Team Portal integration, select Patient Chart &gt; Trigger No Patient Context. The Care Team Portal should launch based on your chosen launch type and automatically log you in.

**Note:** Your Epic login ID must match your ServiceNow user ID for the authentication to work.

