---
title: ServiceNow AI Platform core feature release notes
description: The ServiceNow AI Platform core features provide configurations for applications and other parts of the ServiceNow AI Platform. The ServiceNow AI Platform core features were enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# ServiceNow AI Platform core feature release notes

The ServiceNow AI Platform® core features provide configurations for applications and other parts of the ServiceNow AI Platform. The ServiceNow AI Platform core features were enhanced and updated in the Australia release.

## ServiceNow AI Platform core features highlights for the Australia release

Control whether read-only fields can be updated through client scripts and server-side operations by configuring read-only options.

See Administer the ServiceNow AI Platform for more information.

## Important information for upgrading ServiceNow AI Platform core features to Australia

The dynamic schema application framework was revised in the Zurich release. If you implemented dynamic schema in the Xanadu or Yokohama releases, the application is automatically migrated to a new framework as part of the upgrade to releases starting with the Zurich release. For details on the migration and steps you might need to perform, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see Configuring read-only security options.

## New in the Australia release

-   **Enhance instance security for sandbox scripts with guarded script**

    The guarded script evaluator restricts the JavaScript features and APIs available to untrusted, client-generated scripts running in the script sandbox environment. Beginning with the Australia Patch 2 release, incompatible scripts sent to the server by guest users are rejected on all instances by default. Scripts sent by authenticated users are evaluated using a phased approach to enforcement that varies by the type of instance to provide time to detect and review incompatible scripts before rejecting them. Scripts that use unsupported features are recorded in the Incompatible Guarded Scripts list, where you can rewrite them or create exemptions for scripts that can't be rewritten.

-   **Granular read-only security options**

    Control the editability of read-only fields by configuring read-only options, allowing for customized behavior that balances usability and security. Read-only options provide granular control over whether read-only fields can be updated through client scripts and server-side operations. You can also test stricter read-only controls in non-production instances before implementing them in production.

-   **Support for reference data types in Dynamic Schema**

    Create dynamic attributes using reference data types.

-   **Work with Dynamic Schema elements in the Workspace condition builder**

    Filter Workspace lists using dynamic schema elements in the condition builder.

-   **Toggle the mail icon display**

    Show or hide the mail icon in email fields by configuring the hide\_email\_icon dictionary attribute.

-   **AI indicator in forms**

    Easily identify AI involvement across the ServiceNow AI Platform® through a visual cue that identifies form fields in configurable workspace and Core UI that have been updated with AI-generated content.

-   **Guest API access control**

    Manage guest access to REST and GraphQL API endpoints using path-based ACLs while maintaining separate authenticated user controls.

-   **Granular admin roles**

    Grant specific permissions to developers or users who perform minor administrative tasks without granting them unrestricted access to the full admin role by reviewing and assigning available granular admin roles.

-   **Optional trailing slash configuration**

    Align with external specifications and industry standards by configuring REST APIs with optional trailing slash support.

-   **Path-based REST ACL control**

    Control access to REST services by creating path-based ACLs using specific HTTP method and path combinations.

-   **Automatically generate request definitions for scripted REST API resources**

    Use sample requests made to an API resource to generate request header associations, query parameter associations, and a request schema for that resource and the related scripted REST API service.

-   **Resource-level security configuration**

    Enable public access or custom ACL authorization by configuring resource-level security settings.

-   **Address field type with auto-suggestions**

    Reduce manual entry errors through a new Address field type for Core UI and Workspace forms, which provides real-time address suggestions displayed as you type.


## Changed in this release

-   **Country setting added to Language and Region preferences**

    Users can select their country from the Next Experience language and region preferences.

-   **New options for date and time format in the User record**

    Users can select from new options for Date format and Time format in the User record.

-   **Control whether date and time formats reflect the user locale by default**

    Configure date and time formats to reflect the user locale when no date or time format has been selected in user preferences through the **glide\_i18n.date.default\_to\_locale** system property.

-   **Control how to set the language for guest users**

    Use a guest user's IP address to set their language through the **glide\_i18n.ip\_geolocation** system property.

-   **Activate additional choices for countries**

    Activate additional choices for countries in the Next Experience language and region preferences or in a User record.

-   **ECMAScript 2021 \(ES12\) JavaScript mode supports additional scripting features**

    Use additional scripting features in applications or scripts that use the ECMAScript 2021 \(ES12\) JavaScript mode.

-   **JavaScript engine updated with changes from the Rhino engine**

    The JavaScript engine on the ServiceNow AI Platform was updated to incorporate changes from the open-source Rhino JavaScript engine.

-   **New Normalization Data Services system property**

    Create duplicate records in core\_company extension tables by setting the **com.glide.acl\_check\_all\_filter\_on\_new** system property to true to reference account records.

-   **System properties secured by default**

    Glide properties that can impact instance security are set to secure values by default. For more information about which system properties are affected and why, see the [Glide Property Hardening \[KB1982254\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1982254) article in the Now Support Knowledge Base.

-   **Tracking records in unauthenticated users' sessions**

    Track records created, modified, or deleted by unauthenticated users to enable session-based ACL access on public forms, portals, or workflows.

-   **Manage guest user access to records**

    Restrict guest user access to records they created or updated during their current session using the 'is in session' condition builder on the ACL form for Sys ID fields.

-   **Session-based guest access**

    Manage REST GraphQL security with path-based ACLs that are enforced without needing to require authentication for access to an API.


-   **Support duplicate company names across core\_company extension tables**

    Avoid normalization conflicts when creating records with the same company name in both the Company \[core\_company\] table and its extension tables, such as Customer Account \[customer\_account\], using the **glide.cmdb.canonical.use\_base\_core\_company\_only** property. It ensures that uniqueness enforcement applies only to base core\_company records.


## Deprecated features

Starting with the Australia release, the legacy user interfaces commonly referred to as UI11 and UI15 are deprecated. These legacy UIs no longer receive enhancements or defect fixes, and will no longer be supported. Certain system features might continue to display through legacy rendering paths \(for example, printer‑friendly views\) and will be addressed case by case as part of ongoing platform improvements. Use the Next Experience for a modern, accessible, unified interface. For information about activating the Next Experience UI, see Considerations for activating Next Experience.

## Activation information

The ServiceNow AI Platform core features are active by default.

## Plugin information

-   **Plugins planned for deprecation**

    The following plugins are planned for deprecation in a future release:

    -   Form designer \(com.glide.ui.ng.fd\): Planned for deprecation in the C release. Form Builder is the recommended replacement for all form configurations. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.
    -   ServiceNow Subscription Management \(com.snc.usage\_admin.snc\): Planned for deprecation in August 2026. Update to the most recent version of the Subscription Management application through the Application Manager. For more information about the Subscription Management application, see Subscription Management.

## Accessibility information

Format Painter plugin for TinyMCE enables you to apply consistent font styles, sizes, and table formats within the HTML editor field. This improvement helps users with cognitive disabilities and low vision by reducing confusion and supporting clear, predictable formatting throughout documents. Keyboard navigation is supported, providing added ease of use for keyboard-only users. For more information, see Configure the HTML toolbar.

**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

