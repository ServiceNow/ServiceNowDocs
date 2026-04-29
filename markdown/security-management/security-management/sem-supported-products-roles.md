---
title: Supported products and roles in
description: The Users and Groups page displays products and roles based on installed plugins and feature configuration. This reference provides a complete list of supported products, role names, and role identifiers.
locale: en-us
release: australia
topic_type: reference
last_updated: "2026-03-25"
reading_time_minutes: 1
keywords: [Security Exposure Management, Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, Configuration Compliance, roles, role identifiers, user management, group management]
---

# Supported products and roles in 

The Users and Groups page displays products and roles based on installed plugins and feature configuration. This reference provides a complete list of supported products, role names, and role identifiers.

The following products and roles are supported in the Users and Groups management interface within the Security Management Workspace. Role availability depends on installed plugins and feature configuration.

## Supported products and roles

|Product \(Workspace\)|Role Name|Role|
|---------------------|---------|----|
|Security Exposure Management|Security Exposure Management Admin|sn\_vul\_cmn.usem\_admin|
|Vulnerability Response|Vulnerability Admin|sn\_vul.vulnerability\_admin|
|Vulnerability Analyst|sn\_vul.vulnerability\_analyst|
|Remediation Owner|sn\_vul.remediation\_owner|
|Vulnerability Event Manager|sn\_vul\_analyst.vul\_event\_manager|
|Application Vulnerability Response|Application Security Manager|sn\_vul.app\_sec\_manager|
|Application Developer|sn\_vul.app\_developer|
|Application Security Champion|sn\_vul.app\_security\_champion|
|Container Vulnerability Response|Container Vulnerability Admin|sn\_vul\_container.vulnerability\_admin|
|Container Vulnerability Analyst|sn\_vul\_container.vulnerability\_analyst|
|Container Remediation Owner|sn\_vul\_container.remediation\_owner|
|Container CI Manager|sn\_vul\_container.ci\_manager|
|Configuration Compliance|Configuration Compliance Admin|sn\_vulc.admin|
|Configuration Compliance Vulnerability Analyst|sn\_vulc.vulnerability\_analyst|
|Configuration Compliance Remediation Owner|sn\_vulc.remediation\_owner|
|Configuration Compliance Auditor|sn\_vulc.auditor|

Only explicit role assignments made through the Users and Groups page are managed in this interface. Role inheritance through other roles or group membership isn’t modified through this interface.

