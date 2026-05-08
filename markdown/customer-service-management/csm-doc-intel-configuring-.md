---
title: Configure Document Intelligence for Customer Service
description: Enable Document Intelligence for Customer Service and create use cases to extract data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Task Intelligence for Customer Service, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Configure Document Intelligence for Customer Service

Enable Document Intelligence for Customer Service and create use cases to extract data.

<table id="table_ih2_hfc_5rb"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ensure that your instance is set up for Predictive Intelligence \(PI\).

</td><td>

Predictive Intelligence is a ServiceNow platform feature that provides a layer of artificial intelligence, which serves as a framework for machine learning models. For more information, see Predictive Intelligence.

</td></tr><tr><td>

Activate the Task Intelligence for Customer Service application \(com.snc.csm\_ml\_task\).

</td><td>

The Task Intelligence for Customer Service application enables customers to create use cases for Document Intelligence and extract relevant information from PDF and image files.

 This application automatically activates the following plugins:

-   Predictive Intelligence for Customer Service Management \(com.snc.csm\_ml\)
-   Customer Service \(com.sn\_customerservice\)
-   Skills Management \(com.snc.skills\_management\)
-   Dynamic Translation \(com.glide.dynamic\_translation\)
-   ServiceNow Language Detection Service Spoke \(com.glide.language\_detection\_spoke\)
-   Predictive Intelligence - Task Intelligence \(com.glide.platform\_ml\_task\)
-   Admin Center for Task Intelligence \(com.sn\_ti\_admin\)

</td></tr><tr><td>

Activate the Document Intelligence Admin application \(com.snc.docintel\_admin\)

</td><td>

The Document Intelligence Admin application enables customers to create and configure use cases for extracting data.Activating this application automatically activates the properties and flows used by Document Intelligence for Customer Service.

</td></tr><tr><td>

\(Optional\) Configure the sn\_csm\_ml\_task.case.docintel.parsing\_supported\_types system property.

</td><td>

Supported attachment types for Document intelligence include:-   image/png
-   image/jpeg
-   application/pdf

You can configure the property to use a subset of these attachment types.

</td></tr><tr><td>

Use the DocIntel Admin experience to create one or more use cases.

</td><td>

-   Create a use case that identifies the information to extract from email and case attachments.
-   Define the fields to be extracted.
-   Select conditions for a use case that tell the Document Intelligence feature when to run.

For more information, see [Create a Document Intelligence use case](csm-task-intel-create-di-use-case.md).

</td></tr></tbody>
</table>## Document Intelligence for case types

When you create a case type that extends the Case \[sn\_customerservice\_case\] table, you need to configure the **Review in DocIntel** UI action for the case type table.

**Related topics**  


[Document Intelligence for Customer Service](csm-document-intelligence.md)

[Review and submit values predicted by Document Intelligence](../task/csm-doc-intel-review-values.md)

[bundle-platai.document-intelligence-landing]

