---
title: Linking issues to multiple objects using Many-to-many table relationship
description: Issues can be linked to different types of objects such as risk, entity, control, control objective, engagement, policy, authority document, and others to determine issue impact. Use the many-to-many relationship tables for each of the objects to link similar issues to an object.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-compliance-management-workspace/control-issue-setup-compliance-ws.html
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage issues using the Compliance Workspace, Use, GRC Compliance workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Linking issues to multiple objects using Many-to-many table relationship

Issues can be linked to different types of objects such as risk, entity, control, control objective, engagement, policy, authority document, and others to determine issue impact. Use the many-to-many relationship tables for each of the objects to link similar issues to an object.

**Note:** The Issue record has controls, control objectives, authority documents, policy, and engagements that can be associated with it as related items. However, you must associate the issue and each object as a corresponding m2m record which is stored in the corresponding m2m tables.

For example, issues are configured as a related list in the Controls form and you can link the issue to the control parent object. When you add an issue to a control, a record is created associating the item that is the control with the issue, in the Issue to Control \[sn\_grc\_m2m\_issue\_item\] table.

Viewing the issues related to a control was mainly only for reference. However, you can also link as many issues that are related to the control within the Control form. With this enhancement, you have the ability of:

-   visibility of viewing, and consolidating all related issues raised on the control
-   determining the impact analysis of all related issues
-   reducing the effort in working on duplicate issues and manage issue impact analysis

A user with sn\_compliance\_ws.corporate\_compliance\_analyst, sn\_compliance\_ws.corporate\_compliance\_manager, sn\_compliance\_ws.it\_compliance\_manager, or sn\_compliance.admin roles can create and delete the records in the many-to-many tables. However, users with these roles cannot update an existing record in the m2m tables. To update a record, you require GRC admin \(sn\_grc.admin\) role.

Many-to-many tables used in Compliance Workspace for creating and deleting the issue to object relationships are:

-   sn\_grc\_m2m\_issue\_item – Issue to control
-   sn\_grc\_m2m\_issue\_content – Issue to control objective
-   sn\_grc\_m2m\_issue\_engagement – Issue to Engagements
-   sn\_grc\_m2m\_issue\_document – Issue to Policy and Issue to Authority document

For more information, see:

-   [Tables installed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/policy-and-compliance-management/r_InstallWPolAndCompl.md) for descriptions of the m2m tables.
-   [Create GRC issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-compliance-management-workspace/manually-create-issues-ws.md) for the different compliance objects that are linked to the issue.
-   [Create a control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-compliance-management-workspace/create-control-ws.md) using the Compliance Workspace to link issues to a control.
-   [Linking automatically generated issues to a control in Many-to-many relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-compliance-management-workspace/originator-automatic-issues-ws.md) to know how multiple issues linked to a control are categorized as automatically generated or manually created.
-   [Create an authority document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-compliance-management-workspace/create-authority-doc-ws.md) using the Compliance Workspace to link issues to an authority document.
-   [Create a control objective](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-compliance-management-workspace/create-ctrl-objective-ws.md) using the Compliance Workspace to link issues to a control objective.
-   [Create an audit engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/audit-management/create-engagement-ws.md) in Audit Workspace to link issues to an engagement.
-   [Create a policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-compliance-management-workspace/create-policy-ws.md) using the Compliance Workspace to link issues to a policy.
-   [360° view of compliance objects and issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/policy-and-compliance-management/grc-policy-data-navigtor.md) for a comprehensive and detailed overview of all object data that the issue is linked to in a many-to-many relationship.

