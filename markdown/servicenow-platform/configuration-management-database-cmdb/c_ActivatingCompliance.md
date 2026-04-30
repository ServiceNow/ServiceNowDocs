---
title: Compliance Activation
description: Compliance functionality is provided by the Certification Core \(com.snc.certification\_core\) plugin which contains shared functionality required for certification audits.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Compliance Activation

Compliance functionality is provided by the Certification Core \(com.snc.certification\_core\) plugin which contains shared functionality required for certification audits.

The Certification Core \(com.snc.certification\_core\) plugin consists of the following plugins, and is activated by default.

-   Activated by default: [Desired State Certification](c_DesiredState.md) \(com.snc.certification\_desired\_state\)
-   [Activate](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US): [Architecture Compliance](c_ArchitectureCompliance.md) \(com.snc.architecture\_compliance\), which automatically activates the Version Management \(com.snc.version\) plugin that manages certification filter and template versions.
-   [Activate](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US): [Data Certification](../../data-certification/concept/c_DataCertification.md) \(com.snc.certification\_v2\), which automatically activates the Version Management \(com.snc.version\) plugin that manages certification filter versions.

