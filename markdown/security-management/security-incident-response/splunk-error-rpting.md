---
title: Splunk error reporting
description: Whenever a connectivity issue with your ServiceNow instance occurs, an error is logged in Splunk with information describing the problem.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ServiceNow Security Operations add-on for Splunk overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Splunk error reporting

Whenever a connectivity issue with your ServiceNow instance occurs, an error is logged in Splunk with information describing the problem.

Error messages are stored in a new index named **servicenow** with sourcetype **servicenow**.

To search for error logs, ensure you are specifying the **servicenow** index in your search. Alternatively, refer to the current Splunk documentation on how to add the new **servicenow** index to the default search indexes.

