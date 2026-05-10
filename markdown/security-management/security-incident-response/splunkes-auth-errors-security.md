---
title: Authentication errors
description: This section describes some common authentication errors and how they can be resolved.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install and configure, Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Authentication errors

This section describes some common authentication errors and how they can be resolved.

## Certificate validation issue

If an error occurs during authentication, you may see the following screen:![Invalid certificate error](../image/new-images/authentication-errors.png)

If you have verified that your API account credentials and the Splunk Base URL information are correct, this error may be due to an issue with the Splunk certificate for the port 8089 communication. ServiceNow® instance requires a valid certificate with a common name that matches the server host name to establish secure connections. For more information, see [Certificates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_Certificates.md). If you see this error, you can verify that the issue is due to a certificate problem by viewing the system logs.

An error condition similar to the following will likely appear: ![Certificate error](../image/splunk_es_auth_error1.png)

To proceed with the authentication, you must replace the Splunk default certificate that is provided for API access on port 8089. For detailed instructions on how to replace the SSL certificate, see [KB0778285](https://support.servicenow.com/nav_to.do?uri=%2Fu_kb_template_kcs_how_to_for_cs.do%3Fsys_id%3D1cedb8cadb33374c5ed4a851ca961909%26sysparm_domain%3Dnull%26sysparm_domain_scope%3Dnull).

