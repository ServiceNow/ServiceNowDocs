---
title: ServiceNow AI Platform core feature release notes
description: The ServiceNow ServiceNow AI Platform core features provide functionalities to applications and other parts of the ServiceNow AI Platform. The ServiceNow AI Platform core features were enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# ServiceNow AI Platform core feature release notes

The ServiceNow® ServiceNow AI Platform core features provide functionalities to applications and other parts of the ServiceNow AI Platform. The ServiceNow AI Platform core features were enhanced and updated in the Yokohama release.

## ServiceNow AI Platform core feature highlights for the Yokohama release

-   Streamline how you access help content on the system events and job scheduling dashboard by accessing the appropriate help content in each tab.
-   Insert, update, and delete data in an external data source from a remote table.

See [Administer the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=intro-now-platform-landing&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[Add dynamic attributes to a dynamic category](https://www.servicenow.com/docs/access?context=add-dynamic-attributes-dynamic-category&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Add individual attributes or a group of attributes to a dynamic category.

-   **[Reference a dynamic attribute or a list of dynamic attributes](https://www.servicenow.com/docs/access?context=create-dynamic-schema-reference&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Build a dependency between a dynamic attribute store field and either a dynamic attribute or a list of dynamic attributes.

-   **[Edit data in remote tables on an instance](https://www.servicenow.com/docs/access?context=create-remote-table-script&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Insert, update, and delete data in an external data source from a remote table on an instance when you enable editing for the table. Customize the script definitions that enable you to insert, update, or delete data from a remote table.


## Changed in this release

-   **[Updated Access Control Lists \(ACLs\) for Transaction tables and Session Management tables](https://www.servicenow.com/docs/access?context=exploring-access-control-list&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    The ACLs for a number of Transaction Management tables and Session Management tables have been updated to enhance security using a combination of Deny and Allow ACLs. All new ACLs have a security attribute. You must have the security attribute to add to the role list of an ACL. For more information, see [Configure an ACL rule](https://www.servicenow.com/docs/access?context=t_CreateAnACLRule&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US), [Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US), and .

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
-   **[Configuring plugins for the TinyMCE HTML editor](https://www.servicenow.com/docs/access?context=configuring-the-html-plugins-for-tinymce&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The Accessibility Checker \(a11ychecker\) plugin is now available in the TinyMCE HTML editor. The plugin identifies WCAG and Section 508 accessibility violations and provides an auto-repair feature where applicable. To configure the plugin, see [Change the TinyMCE HTML editor plugins](https://www.servicenow.com/docs/access?context=configuring-the-html-plugins-for-tinymce&version=yokohama&pubname=yokohama-platform-administration&section=change-the-tinymce-html-editor-plugins&ft:locale=en-US). Additional configurations to the accessibility rules, like changing the WCAG level and HTML versions can also be done via **TinyMCEconfigscript** script.

-   **[Field types supported in a configurable workspace](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The following field types are now supported for use in a configurable workspace:

    -   Documentation\_field
    -   Domain\_path
    -   HTML\_Script
    -   Long
    -   Longint
    -   multi\_small
    -   Order index
    -   Radio
    For more information, see [Field types reference](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

-   **[Specify the tables that a REST API access policy restricts](https://www.servicenow.com/docs/access?context=create-api-access-policy&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Specify the tables that a Table REST API access policy applies to on the API Access Policy form.

-   **[Use ISO currency codes with the FX Currency field type](https://www.servicenow.com/docs/access?context=fx-currency&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Use three-digit ISO 4217 currency codes from the **Numeric code** field on the Currency \[fx\_currency\] table with fields of the FX Currency field type.

-   **[Sorting according to the session language](https://www.servicenow.com/docs/access?context=sorting-session-language&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Configure whether string values in columns are sorted according to the user's session language or English.

-   **[Columnstore index type](https://www.servicenow.com/docs/access?context=t_CreateCustomIndex&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Optimize data storage and retrieval by creating a columnstore index. This index type is available with RaptorDB Professional.


## Activation information

The ServiceNow AI Platform core features are active by default.

**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

