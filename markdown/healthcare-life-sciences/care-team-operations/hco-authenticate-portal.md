---
title: Authenticate SMART on FHIR for use with the Care Team Portal in Hyperspace via Hyperdrive
description: Set up your FHIR app with the correct configurations to allow single sign-on for EPIC users to access the Care Team Portal inside EPIC Hyperspace via Hyperdrive.
locale: en-US
release: yokohama
product: Care Team Operations
classification: care-team-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Embedding Care Team Portal in Epic Hyperspace via Hyperdrive, Configuring Healthcare Operations Core, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Authenticate SMART on FHIR for use with the Care Team Portal in Hyperspace via Hyperdrive

Set up your FHIR app with the correct configurations to allow single sign-on for EPIC users to access the Care Team Portal inside EPIC Hyperspace via Hyperdrive.

## Before you begin

Role required: admin

## About this task

The following steps assume you’ve already created a fhir.epic.com account. Please note that it is recommended that a member of the EPIC team for the customer organization creates this FHIR app. The customer is responsible for managing and maintaining this app for their organization. For more information, see [https://fhir.epic.com/Developer/Index](https://fhir.epic.com/Developer/Index).

## Procedure

1.  Log in to FHIR on EPIC.

2.  Select **Build Apps**.

3.  Click **Create**.

4.  Provide an application name.

    For example, Care Team Portal.

5.  Under Application Audience, select Clinicians or Administrative Users.

6.  Under Redirect URI, select **Add another URI**.

7.  Enter your instance name.

    For example, `<instance-name>.service-now.com/navpage.do`.

8.  Repeat this for each test, dev, or prod instance you want to use with Care Team Portal using Add another URI.

9.  Select **Save**.

10. Fill in the remaining fields as needed.

11. Click **Save &amp; Ready for Sandbox** to enable testing.


## Result

An app has been created in EPIC on FHIR that can be utilized for single sign on in Hyperspace for Care Team Portal.

**Note:** Upon submitting the app, note that it can take 24 hours or more for the app to sync.

