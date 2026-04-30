---
title: Security incident automatic creation
description: Third-party monitoring tools, such as Splunk, can be integrated with Security Incident Response so that security events imported from those tools automatically generate security incidents. You can also import data from third-party tools into security alerts.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security incident creation, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security incident automatic creation

Third-party monitoring tools, such as Splunk, can be integrated with Security Incident Response so that security events imported from those tools automatically generate security incidents. You can also import data from third-party tools into security alerts.

To integrate alert monitoring tools to Security Incident Response, you must use the [REST API](https://www.servicenow.com/docs/access?context=c_RESTAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) to write to the Security Incident Import \[sn\_si\_incident\_import\] table. Then, using the **Security Incident Transform** [transform maps](https://www.servicenow.com/docs/access?context=c_CreatingNewTransformMaps&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US), the import set source table is mapped to fields in the target Security Incident \[sn\_si.incident\] table.

If you attempt to import CI records that are not recognized by the transform map, the transform map script checks the record for the following \(in this order\) in an attempt to make a match:

-   sys\_id
-   CI name
-   fully qualified domain name
-   IP address

**Note:** If you find that the **Security Incident Transform** transform map is not adequate for the third-party alert monitoring tool you are using, duplicate the transform map, create a new one, and edit the fields, as needed.

