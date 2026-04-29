---
title: LDAP integration troubleshooting
description: If you are integrating your LDAP server and have questions, these items may help you troubleshoot the issue.
locale: en-US
release: australia
product: LDAP integration
classification: ldap-integration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [LDAP integration, Authentication, Access Management]
---

# LDAP integration troubleshooting

If you are integrating your LDAP server and have questions, these items may help you troubleshoot the issue.

## Preliminary checks

-   If the LDAP is unavailable, users cannot log in to the instance. A good practice is to have local accounts for administrators so that if the LDAP is down, administrators can still access the instance.
-   Check the service account to ensure that it is not expired or locked out.
-   Check the format of the username. Instead of using just the username, try using the domain with the username, or username@domain.
-   Verify that you have changed the `system_id` entry on the `ldap_server_config` record. If you modify the `system_id` unintentionally with an update set, `system_id` points to the wrong node for the target instance and does not work.

## Error codes

The LDAP log file lists industry standard error codes for both LDAP and Active Directory \(AD\). The LDAP log file is contained in the wrapper file. The LDAP error codes are two-digit numbers, while the Active Directory error codes are three-digit numbers. For a list of the most-common error codes, see [LDAP Error Codes](../../../administer/reference-pages/reference/r_LDAPErrorCodes.md).

## Multiple domain integration

You can integrate multiple domains within the same forest or in completely non-trusted domains. It is recommended that you create a separate [LDAP server record](../task/t_DefineAnLDAPServer.md) for each domain. Each LDAP server record must point to a domain controller for that given domain. This means you will have to allow connections to each of the domain controllers. Multiple AD forests through LDAP with one LDAP account is not supported.

When you expand to more than one domain, it is critical that you identify unique LDAP attributes for the application usernames and import coalesce values. A common unique coalesce attribute for Active Directory is `objectSid`. Unique usernames will vary based on your LDAP data design. Common unique attributes are `email` or `userPrincipalName`.

## Incoming records

See [LDAP transform maps](c_LDAPTransformMaps.md) to set how the integration processes incoming LDAP records that are missing matching values in reference fields.

## Common authentication errors

-   User Cannot Log In \(Invalid DN\)
-   Invalid CN
-   Invalid Connection

## Automatic LDAP connection tests

You can manually test connections to LDAP servers or allow ServiceNow to automatically test the connections.

The system tests the connection automatically:

-   Every time a user opens the LDAP Server form.
-   Through the LDAP Connection Test scheduled job, which runs every 15 minutes by default.

    You can change how often this scheduled job runs. If this scheduled job is not able to establish a connection, a new one-time schedule job retries the connection test after either five minutes, or half the **Repeat Interval** value in the scheduled job, whichever occurs first.


Error messages appear on the form if there are any issues connecting to the LDAP server. Also supported are test connections for servers behind a MID server.

