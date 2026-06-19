---
title: In Epic: Configure Epic Hyperspace Integration
description: To launch ServiceNow from within Epic, a button needs to be added within Epic, which requires multiple integration records to be set up.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/healthcare-life-sciences/healthcare-and-life-sciences/hco-configure-epic-integration.html
release: zurich
product: Healthcare and Life Sciences
classification: healthcare-and-life-sciences
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 1
breadcrumb: [Embed Care Team Portal in Epic, Configure, Care Team Portal, Healthcare Operations, Healthcare and Life Sciences]
---

# In Epic: Configure Epic Hyperspace Integration

To launch ServiceNow from within Epic, a button needs to be added within Epic, which requires multiple integration records to be set up.

## Before you begin

Role required: admin

## About this task

For specific setup instructions, refer to Epic product documentation. If assistance is needed, contact Epic Technical Support for help with completing the Epic integration steps within Epic.

## Procedure

1.  Create an FDI Integration record.

    -   Use the **PACS** type.
    -   Set the Model record to **SMART ON FHIR**.
    -   Use the following format for the URL: `https://<instanceName>.service-now.com/careteam?glide_sso_id=<ServiceNow OIDC Identity Provider sys_id>`.
    -   It is recommended to use a LAUNCHTYPE of **7**, which opens ServiceNow within an iframe, but other launch types are available.
    -   The CONTEXT field controls the token data that is sent to ServiceNow within the authorization token, which makes it accessible within ServiceNow record producers. For example: `sysparm_caller_id=%SYSLOGIN%&sysparm_logindepid=%LOGINDEPTID%`.
    **Note:** You may need to revisit the FDI record and update the CONTEXT if at a later time it is decided that more data should be accessible in ServiceNow from Epic. For a full list of available data that can be sent from Epic, as well as the contexts in which that data can be sent, refer to the Epic Token Library within Epic's product documentation.

2.  Create an Activity record \(E2N\) and attach the FDI record.

    This maps a button to a specific activity. When the button is pressed, Epic launches the activity set in the E2N record. This should be mapped to the FDI record created in the previous step.

3.  Create a Menu Record \(E2U\) for the button and attach the Activity record \(E2N\).

    The menu record determines where in Epic the button is placed. When determining placement, consider what makes the most sense for the clinicians who will press the button in order to launch the Care Team Portal. After configuring the E2U button, it must be assigned to target users' Epic toolbar profile before it becomes visible in Epic.

4.  Once the button has been created within the toolbar in Epic, press the configured button to open the ServiceNow Care Team Portal from within Epic.


## Result

An Epic button is configured in Hyperspace that launches the ServiceNow Care Team Portal with the appropriate authorization token data from Epic.

