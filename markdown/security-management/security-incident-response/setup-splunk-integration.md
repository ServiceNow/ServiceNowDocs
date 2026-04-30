---
title: Splunk integration setup
description: Setup procedures for the ServiceNow Security Operations add-on for Splunk include downloading the add-on file in Splunk, installing the add-on, and setting up the ServiceNow instance where security incidents and events are created.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ServiceNow Security Operations add-on for Splunk overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Splunk integration setup

Setup procedures for the ServiceNow Security Operations add-on for Splunk include downloading the add-on file in Splunk, installing the add-on, and setting up the ServiceNow instance where security incidents and events are created.

## Required role

Before performing Splunk integration setup procedures, be sure to define an integration user with the sn\_si.integration\_user and sn\_si.analyst roles on your ServiceNow instance. Additionally, in order to perform imports, you need the import\_transformer role to obtain read and write permission to the security tables. The sn\_si.integration\_user role should be defined with the import\_transformer portion of the role.

