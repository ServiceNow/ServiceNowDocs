---
title: Exploring Decision Tables
description: Decision tables in Workflow Studio enable developers to decouple decision logic from their code by creating and maintaining decision rules.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Decision tables, Workflow Studio, Build workflows]
---

# Exploring Decision Tables

Decision tables in Workflow Studio enable developers to decouple decision logic from their code by creating and maintaining decision rules.

## Demo

For an in-depth review and demo of decision table features and benefits, see [Decision Builder Testing and Publishing \| Creator Toolbox-ServiceNow](https://youtu.be/wOZs0Qew7t8).

## Announcements

-   As of the Washington DC release, Decision Builder is now part of Workflow Studio. Workflow Studio gives you a streamlined way to author, configure, and monitor processes, flows, subflows, playbooks, actions, and decision tables in one place.
-   The core Decision Builder feature is still available with the ServiceNow AI Platform® by default, but the latest updates are available for download through the Workflow Studio application in the ServiceNow® Store.
-   For more information about this update, see the [Washington DC Decision Builder release notes](https://www.servicenow.com/docs/access?context=decision-builder-rn&version=australia&pubname=australia-release-notes&ft:locale=en-US).

## Get started

<table id="table_p4v_mvz_nyb" class="nav-card"><tbody><tr><td>

[Explore![](../../../reuse/icons/brand-icons/bus-explore.svg)Learn about decision table concepts and features](exploring-decision-builder.md)

</td><td>

[Configure![](../../../reuse/icons/brand-icons/bus-sdlc.svg)Configure environments, tools, and user access for decision tables in Workflow Studio](configuring-decision-builder.md#)

</td></tr><tr><td>

[Use![](../../../reuse/icons/brand-icons/bus-service-aware-cmdb.svg)Build decision tables in Workflow Studio](using-decision-builder.md)

</td><td>

[Reference![](../../../reuse/icons/brand-icons/bus-learn.svg)Get details about decision table properties and Domain Separation](decision-builder-reference.md)

</td></tr></tbody>
</table>## Features

**Note:** After you install Workflow Studio decision tables, you can only access decision tables previously created in the classic environment through Workflow Studio. You can no longer create or modify decision tables in the classic environment.

Workflow Studio provides an intuitive interface to create and manage decision tables, which store sets of decision rules.

Decision tables embed business logic into a series of if-then decision rules. Decision tables read data from inputs and evaluate the data according to specified conditions. When all the conditions for a decision rule are met, the decision table returns one or more results.

Administrators can use the delegated development capability to manage workload efficiently by assigning the delegated development role to developers or non-admin users. A delegated developer has more permissions than a user, but less than an admin. Non-admin designated users can create and manage decision tables at the application level. For more information, see [Delegated development](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=australia&pubname=australia-application-development&ft:locale=en-US).

Decision tables in Workflow Studio enable you to do the following:

-   Create inputs that read data at runtime from existing records, external data sources, or hard-coded values.
-   Create and modify decision rules.
-   Change the order of evaluation criteria to optimize results.

## Benefits

Decision tables in Workflow Studio provide the following benefits:

-   Build complex decisions easily with decision tables.
-   Meet changing business requirements and quickly update decisions by modifying only the decision logic and not the application code.
-   Increase efficiency by reusing decision logic across multiple applications.
-   Evaluate data at runtime from multiple sources, including existing ServiceNow records and data from external sources.

## Workflow Studio integration with other applications

Extend the capabilities of decision tables in Workflow Studio by integrating with applications in the ServiceNow AI Platform® suite.

<table id="table_b4b_c2m_vsb"><thead><tr><th>

Application

</th><th>

Description

</th><th>

Reference

</th></tr></thead><tbody><tr><td>

[App Engine Studio](https://www.servicenow.com/docs/access?context=aes-overview&version=australia&pubname=australia-application-development&ft:locale=en-US)

</td><td>

-   App Engine Studio \(AES\) provides an Integrated Development Environment \(IDE\) application-like interface for app developers to build custom applications in one centralized location while maintaining your organization's brand and application development standards.
-   AES users can create decision tables using an AES wizard and access existing decision tables for their applications without leaving AES.

</td><td>

See [Add a decision](https://www.servicenow.com/docs/access?context=add-automation&version=australia&pubname=australia-application-development&ft:locale=en-US) in App Engine Studio.

</td></tr></tbody>
</table>## Troubleshoot and get help

-   Contact your company's Customer Admin to unlock or add user accounts, perform restores or zBoots, and more.

    Contact your company's Customer Admin

-   [Decision Builder in the ServiceNow Community](https://www.servicenow.com/community/workflow-automation-articles/getting-started-with-decision-builder-workflow-automation-coe/ta-p/2359919)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

