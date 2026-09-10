---
title: Create an alias for a basic authentication credential for IBM Flash System discovery
description: Create an alias for a basic authentication credential to run IBM Flash System discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/create-alias-basic-auth-cred-ibm-flash.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [IBM Flash System, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create an alias for a basic authentication credential for IBM Flash System discovery

Create an alias for a basic authentication credential to run IBM Flash System discovery.

## Before you begin

-   Verify you have a basic authentication account with read-only access configured on the IBM Flash System array.
-   Verify that you have at least version 1.35.0 of Discovery and Service Mapping Patterns.
-   Select the Application scope icon \[Omitted image "application-scope-icon.png"\] and verify that the scope is set to **Discovery and Service Mapping Patterns**. The pattern launcher only resolves credentials created in the **Discovery and Service Mapping Patterns** scope.

Role required: discovery\_admin

## About this task

The IBM Flash System pattern uses basic authentication credentials to authenticate with the storage system. The pattern exchanges the username and password for a session token, which it uses for all subsequent REST calls to retrieve storage data.

## Procedure

1.  Create an alias.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Select **New**.

    3.  Enter a unique name for the alias and select **Credential** for the alias type in the **Type** field.

    4.  Select **Submit**.

2.  Configure a basic authentication credential for the new alias.

    1.  Navigate to **Discovery** &gt; **Credentials**.

    2.  Select **New**.

    3.  Select **Basic Auth Credentials**.

    4.  Unlock the **Credential alias** field and select the alias you created.

    5.  Configure the rest of the **Basic Auth Credentials** form fields.

        For more information about Basic Auth Credentials form fields, see [Basic authentication credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/r_BasicAuthCredentialsForm.md).

    6.  Select **Submit**.


## What to do next

Create a serverless discovery schedule. For more information, see [Create a serverless discovery schedule for IBM Flash System discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-ibm-flash.md).

**Parent Topic:**[IBM Flash System pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/ibm-flash-system-pattern.md)

**Related topics**  


[IBM Flash System pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/ibm-flash-system-pattern.md)

