---
title: Redirect UI16 module links to Service Operations Workspace
description: Redirect classic UI16 module navigation links to the equivalent Service Operations Workspace \(SOW\) experience.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Service Operations Workspace for ITSM to improve your experience, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Redirect UI16 module links to Service Operations Workspace

Redirect classic UI16 module navigation links to the equivalent Service Operations Workspace \(SOW\) experience.

## Before you begin

Role required: sn\_exp\_redirect.sn\_redirect\_config\_admin

## About this task

**Note:**

-   The option to enable the classic UI16 module navigation links redirection feature and configure as required is available in the SOW Admin Center only for the upgrade or existing instances.
-   In new instances, this feature is enabled by default at the base system and cannot be configured. All users are automatically redirected to the SOW. To modify this setting, you must consult ServiceNow.
-   When the **sn\_sow\_itsm\_admin.experience\_redirection\_enabled.sow** system property is set to true, selecting any configured UI16 module navigation link redirects all users to the equivalent SOW experience, bypassing all application-level and user group conditions.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Configurations**.

2.  On the Admin Center page, do one of the following:

    -   In the **Overview** tab, select the **Configure** button in the **Initial setup** section and then select **SOW vs Classic UI16 redirection**.
    -   In the **Configurations** tab, select **Initial setup** &gt; **SOW vs Classic UI16 redirection**.
3.  Configure any of the following options:

    -   **Global configuration for all users redirection**: Enables the classic UI16 module links including forms and lists across all applications, all users, and user groups to be redirected to the corresponding SOW experience, replacing the standard UI16 form, list, or page with its equivalent.
    -   **Custom configuration**: Enables you to configure the redirection of classic UI16 module links to the equivalent SOW experience at both the application or record level and the user group level. You can enable the redirection of classic UI16 module links for a custom table or specific application such as On-Call Scheduling or Incident Management. For each custom table or application in SOW, you can enable the redirection behavior for a selected user groups or all user groups. The following records or application are supported:
        -   Incident Management
        -   On-Call Schedule \(On-Call Scheduling\)
        -   Problem Management
        -   Major Incident Management
        -   Change Management
        -   Incident Alert Management
        -   Request Management
        -   Walk-up \(Walk-up Experience\)

## What to do next

Apart from the above admin configuration, the UI16 module must support the link redirect configuration. To verify, select the **Edit Module** option on the UI16 module and ensure the following:

-   The **Link Type** field is set to `URL`.
-   The **Argument** field must reference the Redirect Handler Endpoint \(sn\_exp\_redirect\_redirect\_handler.do\).
-   The required query parameters has the following format:
    -   coreui: URL for Classic UI \(Core UI\). For example, `incident.do%3Fsysparm_query%3D...`
    -   uib: URL for the UIB \(SOW experience\)
    -   type: Identifier of the module type
    -   product: Product identifier. For example, MIM \(for Major Incident Management\)
-   The URLs passed in the coreui and uib parameters must be URL-encoded. If the URLs contain special characters or spaces, the redirection fails because the system splits parameters at ampersand \(&amp;\) boundaries.

    -   &amp; \(ampersand\): %26
    -   \(space\): %20
    -   ? \(question mark\): %3F
    -   =\(equals\): %3D
    For example: A Core UI URL with additional query parameters must encode all internal special characters. For example, `incident.do%3Fsysparm_query%3Dcategory%3Dnetwork%2526state%3D1`

    **Note:** Do not pass raw URLs with unencoded special characters. The redirection fails if URL encoding is missing.


For example, the **Argument** field of the Candidates module of Major Incident Management must have the value in the format: `sn_exp_redirect_redirect_handler.do?coreui=incident_list.do?sysparm_query=major_incident_state%3Dproposed%5Eactive%3Dtrue%5EEQ&uib=/now/sow/list/params/list-id/b3ae077843887110f275a32d68b8f236&type=app_module&product=mim`

**Parent Topic:**[Configuring Service Operations Workspace for ITSM to improve your experience](../concept/configuring-sow-to-improve-experience.md)

