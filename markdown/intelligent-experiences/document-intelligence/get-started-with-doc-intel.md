---
title: Set up Document Intelligence
description: Review the following information before you start setting up Document Intelligence.
locale: en-US
release: zurich
product: Document Intelligence
classification: document-intelligence
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Document Intelligence, Enable AI experiences]
---

# Set up Document Intelligence

Review the following information before you start setting up Document Intelligence.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](../concept/docintel-nowassist-landing.md).

<table id="table_mnf_lpg_tsb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that the ServiceNow core applications or plugins that are required to support Document Intelligence are installed and activated.

</td><td>

Verify that the following applications or plugins are installed and activated from the ServiceNow Store. When you activate the first plugin, its dependent plugins are activated automatically. If not installed, install and activate one application at a time in the following order to ensure a smooth implementation.-   Predictive Intelligence \(com.glide.platform\_ml\)
-   Platform Document Intelligence \(com.glide.platform\_ml\_di\)
-   Document Intelligence UIB Component \(sn\_docintel\_iframe\)

For more information, see [Install Document Intelligence](../task/install-document-intelligence.md).

</td></tr><tr><td>

\(Optional\) Install the Document Intelligence Admin application for an improved user experience for process owners to set up, configure, and monitor their document extraction solutions.

</td><td>

Install the [Document Intelligence Admin](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8700f4efc3a411101d9a3cadb140ddad/1.1.0) application from the ServiceNow® Store. Review the listing for information on dependencies, licensing or subscription requirements, and release compatibility.

 Key features of the application include:

 -   Easily configure your document extraction solutions by defining what you want to extract from your documents.
-   Monitor the performance of your document extraction solutions and adjust the level of automation.

</td></tr><tr><td>

Verify that you’ve assigned the required ServiceNow AI Platform roles.

</td><td>

The following roles are used across the Document Intelligence features:-   The administrator \(admin\) installs the application from the ServiceNow Store and assigns the roles.
-   sn\_docintel.admin
-   sn\_docintel.creation\_agent
-   sn\_docintel.extraction\_agent
-   sn\_docintel.manager
-   sn\_docintel.viewer

</td></tr><tr><td>

Domain separation

</td><td>

Review the [domain separation topic](domain-separation-and-doc-intel.md) information if you intend to separate data, processes, and administrative tasks.

 See [Domain separation and Document Intelligence](domain-separation-and-doc-intel.md).

</td></tr><tr><td>

Verify that file extensions required to support Document Intelligence are included in any glide.attachment.extensions system property customizations.

</td><td>

The glide.attachment.extensions system property is empty by default. When customizing it, ensure that the following file extensions are included:

 -   jpeg
-   jpg
-   png
-   pdf

 For more information, see [Restrict attachment file extensions](https://www.servicenow.com/docs/access?context=t_DisablingTheDragAndDropFeature&version=zurich&pubname=zurich-platform-administration&section=t_RestrictingFileExtensions&ft:locale=en-US).

</td></tr><tr><td>

Copy any use cases needed to support your Document Intelligence implementation.

</td><td>

Follow the steps in [Duplicate a document extraction use case](../task/duplicate-a-use-case.md) to copy a use case along with its fields, field groups, integrations, flows, and all the related machine learning \(ML\) models.

</td></tr><tr><td>

Import any use cases needed to support your Document Intelligence implementation.

</td><td>

Follow the steps in [Import a document extraction use case](../task/import-a-use-case.md) to import a use case along with its fields, field groups, integrations, flows, and all the related machine learning \(ML\) models.

</td></tr></tbody>
</table>