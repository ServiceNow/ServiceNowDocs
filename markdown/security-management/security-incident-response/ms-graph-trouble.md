---
title: Troubleshooting Microsoft Graph Security API integration
description: This section covers important troubleshooting tips and frequently asked questions related to the Microsoft Graph Security API alert ingestion integration.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft Graph Security API alert ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Troubleshooting Microsoft Graph Security API integration

This section covers important troubleshooting tips and frequently asked questions related to the Microsoft Graph Security API alert ingestion integration.

-   **Integration run**: When a scheduled job starts executing, an integration run record with logs, errors, and warnings is displayed. The number of alerts pulled and the number of incidents created in a scheduled job run are also displayed. Users with the `sn_si.analyst` role can see if any errors/profiles pulling failed during the integration run. Users with the `sn_si.analyst` role can check the `sn_event_ingestion_integration_run` table for any errors that have occurred. To troubleshoot any integration issues, you must first check the integration run. Errors are logged as worknotes in the integration run records for every scheduled job run.
-   ![Microsoft Graph Security API Integration Run](../image/ms-graph-trouble.png)

-   **Incomplete profile**: While configuring the profile, in the Additional Options \([Automate alert updates and closure based on SIR incident status](../task/ms-graph-create-profile-automate.md)\) section, you must click the **Finish** button to ensure that the profile is moved to Waiting state indicating that it is waiting for ingestion.
-   **Validate profile**: To validate if the integration is working correctly, check the profile states, last pulled date of profile, alert import table, alert to task table records.
-   **SSL issues**: When connecting through the Microsoft Graph Security API, ensure that the instance has a valid CA certificate which has not expired. You can import RSA or your own certificates into the platform and ensure that the common name of the certificate matches host name. See [KB0778285](https://support.servicenow.com/kb_view.do?sysparm_article=KB0778285) for details.

