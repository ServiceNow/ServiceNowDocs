---
title: Create a new security policy
description: Administrators can specify which security profiles WS-Security communications must meet by creating a new security policy.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Create a new security policy

Administrators can specify which security profiles WS-Security communications must meet by creating a new security policy.

## Before you begin

Role required: web\_service\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **SOAP Security Policies**.

2.  Click **New**.

3.  Fill out the SOAP Security Policy form \(see table\).

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique name for the security policy. Use this name to set the default security policy with the `glide.soap.default_security_policy` property.|
    |Type|Select whether the SOAP security policy applies to inbound or outbound traffic.|
    |Required to Sign SOAP Request|Select this checkbox to require signed SOAP requests. Clear the checkbox to allow unsigned SOAP requests. When enabled, the instance will produce an error for any SOAP request that does not include a valid signature. When disabled, the instance still verifies any signature included with a SOAP request.|
    |Authenticate|Select if a SOAP request must authenticate against all security profiles or at least one security profile.|
    |Security Profiles|Select the [security profiles](../reference/ws-security-reference.md) you want to apply to this SOAP security policy. You must select at least one security profile.|

4.  Click **Submit**.


**Parent Topic:**[SOAP web service](../concept/c_SOAPWebService.md)

