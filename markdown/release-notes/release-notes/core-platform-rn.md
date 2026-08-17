---
title: ServiceNow AI Platform core feature release notes
description: The ServiceNow AI Platform core features provide configurations for applications and other parts of the ServiceNow AI Platform. The ServiceNow AI Platform core features were enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
---

# ServiceNow AI Platform core feature release notes

The ServiceNow AI Platform® core features provide configurations for applications and other parts of the ServiceNow AI Platform. The ServiceNow AI Platform core features were enhanced and updated in the Zurich release.

## ServiceNow AI Platform core features highlights for the Zurich release

-   Simplify and build queries with fewer conditions by leveraging hierarchical relationships in a condition builder.
-   Use additional scripting features, including Promises and Async await, with the ECMAScript 2021 \(ES12\) JavaScript mode.
-   Define dynamic categories and dynamic attributes once and reuse them using dynamic namespaces across multiple tables and dynamic attribute store fields.

See [Administer the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/intro-now-platform-landing.md) for more information.

Use the Feature Preview Program to choose which pre-release capabilities to activate and test on your instance.

## Important information for upgrading ServiceNow AI Platform core features to Zurich

The dynamic schema application framework has been revised in the Zurich release. If you implemented dynamic schema in Xanadu or Yokohama, the application is automatically migrated to a new framework as part of the upgrade to the Zurich release. For details on the migration, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.

## New in the Zurich release

-   **[Access and test pre-release features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/feature-preview-program.md)**

    The Feature Preview Program provides a centralized location to discover, activate, and test pre-release capabilities on your instance. When a pre-release feature is added to your instance, you receive a notification and can access the Feature Preview Program to review feature details, activate features for testing, and provide feedback.

-   **[Enhance instance security for sandbox scripts with guarded script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/scripts/guarded-script.md)**

    The guarded script evaluator restricts the JavaScript features and APIs available to untrusted, client-generated scripts running in the script sandbox environment. Beginning with the Zurich Patch 9 release, incompatible scripts sent to the server by guest users are rejected on all instances by default. Scripts sent by authenticated users are evaluated using a phased approach to enforcement that varies by the type of instance to provide time to detect and review incompatible scripts before rejecting them. Scripts that use unsupported features are recorded in the Incompatible Guarded Scripts list, where you can rewrite them or create exemptions for scripts that can't be rewritten.

-   **[Hierarchical queries in condition builders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/data-hierarchies.md)**

    Simplify and build queries with fewer conditions using existing hierarchical data in a table. You can also define new hierarchical relationships between records that are in the same table.

-   **[Dynamic namespaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-dynamic-namespace.md)**

    Define categories and attributes once and reuse them using dynamic namespaces across multiple tables and dynamic attribute store fields. A dynamic namespace is automatically created when you add a dynamic attribute store field.

-   **[Experimentation framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/experimentation-framework.md)**

    Help enable innovation by trying new ServiceNow® feature variants in your instance. Only single customer instances or Gen AI Innovation Program participants have early access to new innovations via experimentation framework. You can opt out of specific experiments or turn off the framework entirely.

-   **[Audit Management Console and audit retention](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/audit-mgmt-console.md)**

    Simplify your audit data management and configuration by using the Audit Management Console module. It includes a new Retention option, which automates and simplifies the deletion of audit data based on your requirements.

-   **[Monitor requestors' API usage rates through the Inbound API Integration Usage dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/web-services/inbound-api-integration-usage-dashboard.md)**

    Inbound integrations track web service requests for OAuth registered applications and user accounts making those requests.

-   **[Use schemas to define the structure and format of REST API responses and requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/define-scripted-rest-api-schema.md)**

    When you define a schema in the ServiceNow AI Platform, the schema can be used to define the structure of requests and responses within the associated REST API. The schema data for the requests and responses is then available in the exportable OpenAPI specification for the API.

-   **[Automatically generate request definitions for scripted REST API resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/autogenerate-api-request-definitions.md)**

    Use sample requests made to an API resource to generate request header associations, query parameter associations, and a request schema for that resource and the related scripted REST API service.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **AI indicator in forms**

    The AI indicator is a visual cue that identifies form fields in configurable workspace and Core UI that have been updated with AI-generated content. This feature enhances user experience by providing a consistent and clear indication of AI involvement across the platform.


## Changed in this release

-   **[ECMAScript 2021 \(ES12\) JavaScript mode supports additional scripting features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/scripts/javascript-engine-feature-support.md)**

    Use additional scripting features, including Promises and Async await, in applications or scripts that use the ECMAScript 2021 \(ES12\) JavaScript mode.

-   **[Stream multipart responses with REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/r_AvailableSystemProperties.md)**

    Stream multipart responses rather than buffering responses until complete by default with REST APIs that support the multipart/mixed requests, such as the Batch API. The **glide.rest.serialize.disable\_response\_stream\_buffering** system property controls this behavior and applies only to instances configured with Application Delivery Controller, version 2 \(ADCv2\).

-   **[Additional field types supported in a configurable workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/r_FieldTypes.md)**

    The following field types are now supported for use in a configurable workspace:

    -   **datetime**
    -   **email\_script**
    -   **int**
    -   **integer\_time**
    -   **related\_tags**
    -   **user\_input**
-   **[Vertical layout configuration for radio buttons in a configurable workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/r_FieldTypes.md)**

    Configurable workspaces now support a vertical layout configuration of radio buttons.

-   **[More dictionary attributes available for selected fields in a configurable workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/r_FieldTypes.md)**

    Applicable fields used in a configurable workspace now support the following dictionary attributes:

    -   **choice**
    -   **decimal**
    -   **float**
    -   **html\_editor**
    -   **integer**
    -   **ip\_addr**
    -   **is\_searchable\_choice**
    -   **phone\_number\_e164**
    -   **readonly\_clickthrough**
    -   **ref\_ac\_columns**
    -   **translated\_html\_editor**
    -   **types**
-   **[New plugins available for the TinyMCE HTML editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/configuring-the.md-plugins-for-tinymce.md)**

    The TinyMCE HTML editor now supports two new plugins in Core UI and configurable workspaces:

    -   The Image Editing \(editimage\) plugin adds a contextual editing toolbar to images in the editor.
    -   The Help plugin \(help\) enables you to check shortcuts and keyboard navigation for accessibility.
-   **[New run types available for scheduled jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/c_ScheduledJobs.md)**

    The following run types are now available for all scheduled job types, enabling flexible scheduling:

    -   **Day and Month in Year**
    -   **Day in Week in Month in Year**
    -   **Week in Month**
    The new run types are available in the following standard scheduled job types:

    -   **Scheduled Email of Report**
    -   **Scheduled Entity Generation**
    -   **Scheduled Script Execution**
    To enable these new run types in other scheduled job child tables, you must configure your applicable form view to include the fields **Day**, **Month**, and **Year**. For more information, see [Enable run types for scheduled job child tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/customize-run-times-for-scheduled-jobs.md).

-   **[New advanced options available for scheduled jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/c_ScheduledJobs.md)**

    The following new advanced options are available when configuring scheduled jobs, offering greater flexibility in job planning, execution, and recurrence:

    -   **Starting**
    -   **Ending**
    -   **Repeat every**
-   **[Export lists to Google Sheets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/setup-gsheet-export.md)**

    Export your lists to Google Sheets directly from the Export menu.


## Removed in this release

-   The **glide.script.use.sandbox** system property has been removed. The script sandbox is enabled by default.
-   Dynamic groups have been removed. Instead, use dynamic attributes in dynamic categories to simplify administration and improve the dynamic schema user experience.

## Deprecations

Starting with the Zurich release, Application Insights is no longer deployed, enhanced, or supported. Instead, [Overview of Instance Observer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/impact/io-overview.md) offers a powerful solution for enhancing system performance. Contact your account manager to discover more. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

The ServiceNow AI Platform core features are active by default.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-platform-admin-rn-landing.md)

