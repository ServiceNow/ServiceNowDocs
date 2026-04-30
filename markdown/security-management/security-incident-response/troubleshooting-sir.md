---
title: Troubleshooting Security Incident Response
description: This section covers important troubleshooting tips and frequently asked questions related to Security Incident Response.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Troubleshooting Security Incident Response

This section covers important troubleshooting tips and frequently asked questions related to Security Incident Response.

## Access Control Rules issues

Access Control Rules allow access to the specified resource if all the following three conditions are met:

-   The user has one of the roles specified in the **Role** list, or the list is empty.
-   Conditions in the **Condition** field evaluate to true, or conditions are empty.
-   The script in the **Script** field \(advanced\) evaluates to true, or sets the variable **answer** to true, or is empty.

For more information on Access Control Rules, see [Exploring Access Control Lists](https://www.servicenow.com/docs/access?context=exploring-access-control-list&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

**Important:** If the **Admin overrides** option is unchecked for a security incident table, and if the Admin is able to access the security incident table, see [KB1444673](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do%3Fsys_id=806165f097143910dfd73dae2153af6b)

