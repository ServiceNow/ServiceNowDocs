---
title: In Epic: Build the FHIR App to Authenticate with ServiceNow
description: Set up your FHIR app with the correct configurations to allow single sign-on for EPIC users to access the Care Team Portal inside EPIC Hyperspace via Hyperdrive.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/healthcare-life-sciences/healthcare-and-life-sciences/hco-authenticate-portal.html
release: zurich
product: Healthcare and Life Sciences
classification: healthcare-and-life-sciences
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Embed Care Team Portal in Epic, Configure, Care Team Portal, Healthcare Operations, Healthcare and Life Sciences]
---

# In Epic: Build the FHIR App to Authenticate with ServiceNow

Set up your FHIR app with the correct configurations to allow single sign-on for EPIC users to access the Care Team Portal inside EPIC Hyperspace via Hyperdrive.

## Before you begin

Role required: admin

## About this task

The following steps assume you’ve already created a fhir.epic.com account. Please note that it is recommended that a member of the EPIC team for the customer organization creates this FHIR app. The customer is responsible for managing and maintaining this app for their organization. For more information, see [https://fhir.epic.com/Developer/Index](https://fhir.epic.com/Developer/Index).

## Procedure

1.  Log in to FHIR on EPIC \([https://fhir.epic.com/](https://fhir.epic.com/)\).

2.  Select **Build Apps**.

3.  Click **Create**.

4.  Provide an application name.

    For example, Care Team Portal.

5.  Under Application Audience, select Clinicians or Administrative Users.

6.  Under Redirect URI, select **Add another URI**.

7.  Enter your instance name.

    For example, `<instance-name>.service-now.com/navpage.do`.

8.  Enter the Redirect URI to allow for patient context to be refreshed from the Care Team Portal.

    For example, `<instance-name>.service-now.com/careteam`

9.  Repeat this for each test, dev, or prod instance you want to use with Care Team Portal using Add another URI.

10. Select **Save**.

11. Fill in the remaining fields as needed.

12. Click **Save &amp; Ready for Sandbox** to enable testing.

13. Ensure the FHIR app has been approved.

    **Note:** Once created it must be approved for Non-Production/Production before it can be used for authentication. Once approved it can take up 12 hours before it becomes available to use.

14. Store the Production and Non-Production Client ID's in a secure location for later access.

    The Non-Production Client ID will be used when integrating Epic with a non-production ServiceNow instance, and the Production Client ID will be used when integrating Epic with a production ServiceNow environment.

15. Identify the FHIR server \(Interconnect\) URL endpoint that is used to support OAuth authentication for the FHIR app."

    Note the test and production URLs. When setting up the identity provider in ServiceNow, these URLs will determine the FHIR server ServiceNow authenticates with.

16. Verify the E0E record for the FHIR app has been generated in your Epic environment and is ready used for authentication with ServiceNow \(this can take up to 12-24 hours once the FHIR application has been approved\).

    **Note:** Configuration is necessary on the E0E record before it can be used to authenticate. For specific setup instructions, refer to Epic product documentation. If assistance is needed, contact Epic Technical Support for help.


## Result

An app has been created in EPIC on FHIR that can be utilized for single sign on in Hyperspace for Care Team Portal.

**Note:** Upon submitting the app, note that it can take 24 hours or more for the app to sync.

