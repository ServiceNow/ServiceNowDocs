---
title: ServiceNow AI Platform core feature release notes
description: The ServiceNow ServiceNow AI Platform core features provide functionalities to applications and other parts of the ServiceNow AI Platform. The ServiceNow AI Platform core features were enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# ServiceNow AI Platform core feature release notes

The ServiceNow® ServiceNow AI Platform core features provide functionalities to applications and other parts of the ServiceNow AI Platform. The ServiceNow AI Platform core features were enhanced and updated in the Yokohama release.

## ServiceNow AI Platform core feature highlights for the Yokohama release

-   Streamline how you access help content on the system events and job scheduling dashboard by accessing the appropriate help content in each tab.
-   Insert, update, and delete data in an external data source from a remote table.

See [Administer the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/intro-now-platform-landing.md) for more information.

## New in the Yokohama release

-   **[Enhance instance security for sandbox scripts with guarded script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/scripts/guarded-script.md)**

    The guarded script evaluator restricts the JavaScript features and APIs available to untrusted, client-generated scripts running in the script sandbox environment. Beginning with the Yokohama Patch 13 release, incompatible scripts sent to the server by guest users are rejected on all instances by default. Scripts sent by authenticated users are evaluated using a phased approach to enforcement that varies by the type of instance to provide time to detect and review incompatible scripts before rejecting them. Scripts that use unsupported features are recorded in the Incompatible Guarded Scripts list, where you can rewrite them or create exemptions for scripts that can't be rewritten.

-   **[Add dynamic attributes to a dynamic category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/add-dynamic-attributes-dynamic-category.md)**

    Add individual attributes or a group of attributes to a dynamic category.

-   **[Reference a dynamic attribute or a list of dynamic attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/create-dynamic-schema-reference.md)**

    Build a dependency between a dynamic attribute store field and either a dynamic attribute or a list of dynamic attributes.

-   **[Edit data in remote tables on an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/create-remote-table-script.md)**

    Insert, update, and delete data in an external data source from a remote table on an instance when you enable editing for the table. Customize the script definitions that enable you to insert, update, or delete data from a remote table.


## Changed in this release

-   **[Updated Access Control Lists \(ACLs\) for Transaction tables and Session Management tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/exploring-access-control-list.md)**

    The ACLs for a number of Transaction Management tables and Session Management tables have been updated to enhance security using a combination of Deny and Allow ACLs. All new ACLs have a security attribute. You must have the security attribute to add to the role list of an ACL. For more information, see [Configure an ACL rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/t_CreateAnACLRule.md), [Deny-Unless ACL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/acl-denial-behavior.md), and .

    The updated Transaction Management tables include:

    -   syslog
    -   syslog\_ajax
    -   syslog\_email
    -   syslog\_transaction
    -   syslog\_script
    The updated Session Management tables include:

    -   sys\_audit
    -   sys\_security\_acl
    -   sys\_user\_auth
    -   sys\_user\_session
-   **[Configuring plugins for the TinyMCE HTML editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/configuring-the.md-plugins-for-tinymce.md)**

    The Accessibility Checker \(a11ychecker\) plugin is now available in the TinyMCE HTML editor. The plugin identifies WCAG and Section 508 accessibility violations and provides an auto-repair feature where applicable. To configure the plugin, see [Change the TinyMCE HTML editor plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/configuring-the.md-plugins-for-tinymce.md). Additional configurations to the accessibility rules, like changing the WCAG level and HTML versions can also be done via **TinyMCEconfigscript** script.

-   **[Field types supported in a configurable workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/r_FieldTypes.md)**

    The following field types are now supported for use in a configurable workspace:

    -   Documentation\_field
    -   Domain\_path
    -   HTML\_Script
    -   Long
    -   Longint
    -   multi\_small
    -   Order index
    -   Radio
    For more information, see [Field types reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/r_FieldTypes.md).

-   **[Specify the tables that a REST API access policy restricts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/create-api-access-policy.md)**

    Specify the tables that a Table REST API access policy applies to on the API Access Policy form.

-   **[Use ISO currency codes with the FX Currency field type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/fx-currency.md)**

    Use three-digit ISO 4217 currency codes from the **Numeric code** field on the Currency \[fx\_currency\] table with fields of the FX Currency field type.

-   **[Sorting according to the session language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/sorting-session-language.md)**

    Configure whether string values in columns are sorted according to the user's session language or English.

-   **[Columnstore index type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/t_CreateCustomIndex.md)**

    Optimize data storage and retrieval by creating a columnstore index. This index type is available with RaptorDB Professional.


## Activation information

The ServiceNow AI Platform core features are active by default.

**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-admin-rn-landing.md)

