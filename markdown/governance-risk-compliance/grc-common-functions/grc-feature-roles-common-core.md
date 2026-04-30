---
title: GRC Feature roles
description: GRC Feature roles are specialized roles that grant access to capabilities of specific GRC features or application areas.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2025-09-05"
reading_time_minutes: 4
breadcrumb: [GRC reference, Common GRC features, Governance, Risk, and Compliance]
---

# GRC Feature roles

GRC Feature roles are specialized roles that grant access to capabilities of specific GRC features or application areas.

## GRC Feature roles plugin

Download and install the GRC Feature roles plugin \(sn\_grc\_ftr\_role\) from the ServiceNow Store to granular obtain access to individual IRM features. GRC Feature roles provide access to individual Integrated Risk Management \(IRM\) capabilities, instead of granting access to the entire IRM feature set. This approach enables users for granular access to specific functionalities, such as Compliance Library, Policy Management, and Control Attestations and Monitoring. It also enables precise control over what is shared with non-IRM products.

## Feature sets

GRC features are logically grouped into feature sets. Feature roles are associated with a specific feature set and provide access to the features available in that feature set.

Non-IRM users can perform the following actions when assigned appropriate feature roles:

-   Library and Control feature set
    -   Create and manage library objects such as authority documents, citations, and control objectives.
    -   Associate entity and entity types to control objectives and generate controls.
    -   Manage control workflows, monitor controls effectively using attestations and indicators, and generate issues.
-   Policy feature set
    -   Create and manage policies and the policy lifecycle.
    -   Create policy acknowledgments and policy exceptions.
-   Audit feature set

    Create and manage engagements, activities, and scoping entities within those engagements. This role also provides access to a lite version of audit workspace.

-   Evidence feature set

    Create and manage evidence requests, collection details, and evidence responses.


**Important:** GRC Feature roles uses the functional domain field on the individual record to identify the type of the record. Access to the record is restricted based on the functional domain enabling the required access to users who need it. For more information about functional domains, see [Tagging records with functional domain](../concept/tagging-records-with-functional-domain.md).

<table id="table_mwj_4c1_4gc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_compliance.library\_employee\_reader\[Employee Operator\]

</td><td>

Users with this role have read access to all library objects \(Authority documents, Citation, Control objectives, Policies\).

</td></tr><tr><td>

sn\_compliance.policy\_exception\_employee\_user\[Employee Operator\]

</td><td>

Users with this role have read access to library, implementation, and can request extension of a policy extension.

</td></tr><tr><td>

sn\_compliance.control\_employee\_reader\[Employee Operator\]

</td><td>

Users with this role have read access to library, implementation objects like controls and control requirements.

</td></tr><tr><td>

sn\_compliance.policy\_ack\_employee\_user\[Employee Operator\]

</td><td>

Users with this role have read access to library, policies, and acknowledge policies.

</td></tr><tr><td>

sn\_grc.issue\_employee\_user\[Employee Operator\]

</td><td>

Users with this role have read access to library, and policies.

</td></tr><tr><td>

sn\_grc.library\_reader\[Lite Operator\]

</td><td>

Users with this role have read access to entities, content, document, audience, audience filters.

</td></tr><tr><td>

sn\_grc.compliance\_assurance\_reader\[Lite Operator\]

</td><td>

Users with this role have read access to item, issues, assessments, indicators, and indicator templates.

</td></tr><tr><td>

sn\_compliance.library\_reader\[Lite Operator\]

</td><td>

Users with this role have read access to Compliance Library \(Authority Documents, Citations, Control Objectives, Policies\).

</td></tr><tr><td>

sn\_compliance.control\_framework\_reader\[Lite Operator\]

</td><td>

Users with this role have read access to controls and control requirements.

</td></tr><tr><td>

sn\_compliance.policy\_reader\[Lite Operator\]

</td><td>

Users with this role have read access to policies, policy exceptions, and policy acknowledgments.

</td></tr><tr><td>

sn\_grc.compliance\_assurance\_business\_user\[Lite Operator\]

</td><td>

Users with this role can create an issue, respond to indicator task, create remediation task, and associate issue to related objects.

</td></tr><tr><td>

sn\_compliance.control\_framework\_business\_user\[Lite Operator\]

</td><td>

Users with this role can associate impacted controls to policy exception.

</td></tr><tr><td>

sn\_compliance.policy\_business\_user\[Lite Operator\]

</td><td>

Users with this role can request policy exception, extension, acknowledge policies, and contribute to policies.

</td></tr><tr><td>

sn\_grc.shared\_configurator\[Lite Operator\]

</td><td>

Users with this role have enable access to common functionalities irrespective of the feature set.

</td></tr><tr><td>

sn\_grc.library\_user\[Operator\]

</td><td>

Users with this role can associate document/content with related objects like information objects, issues, and entities.

</td></tr><tr><td>

sn\_grc.compliance\_assurance\_user\[Operator\]

</td><td>

Users with this role can create item, define assessment grouping, associate item to entity/entity types, associate entity with content, document, indicator, and indicator templates.

</td></tr><tr><td>

sn\_compliance.library\_user\[Operator\]

</td><td>

Users with this role can create control objectives and policies.

</td></tr><tr><td>

sn\_compliance.control\_framework\_user\[Operator\]

</td><td>

Users with this role can create controls, control requirements, and associate controls to entities.

</td></tr><tr><td>

sn\_compliance.policy\_user\[Operator\]

</td><td>

Users with this role can create policies, acknowledgment campaign, and define policy exception related records.

</td></tr><tr><td>

sn\_grc.library\_manager\[Operator\]

</td><td>

Users with this role can create content, document, audience, indicator templates, entity, and entity types.

</td></tr><tr><td>

sn\_grc.control\_framework\_manager\[Operator\]

</td><td>

Users with this role can manage item, associate items to related objects, create indicators, supporting data, associate indicator to related objects, attestation designer, types, grouping criteria, associate control objectives to indicator templates, entities, and entity types.

</td></tr><tr><td>

sn\_compliance.library\_manager\[Operator\]

</td><td>

Users with this role can create authority documents, citations, control objectives, policies, and associate library to taxonomy

</td></tr><tr><td>

sn\_compliance.policy\_mgr\[Operator\]

</td><td>

Users with this role can manage compliance library objects, perform policy lifecycle, configure exception reasons, define policy exception approval rules, and configure dynamic approval rules.

</td></tr><tr><td>

sn\_grc.library\_admin\[Operator\]

</td><td>

Users with this role can delete or deactivate library.

</td></tr><tr><td>

sn\_grc.compliance\_assurance\_admin\[Operator\]

</td><td>

Users with this role can delete indicator, item, assessment criteria, and create or delete functional domain registry records.

</td></tr><tr><td>

sn\_compliance.library\_admin\[Operator\]

</td><td>

Users with this role can delete or deactivate library.

</td></tr><tr><td>

sn\_compliance.control\_framework\_admin\[Operator\]

</td><td>

Users with this role can delete control, control requirements, create association between control to control objectives and compliance score record.

</td></tr><tr><td>

sn\_compliance.policy\_admin\[Operator\]

</td><td>

Users with this role can delete policy, acknowledge campaign, policy, and policy exception.

</td></tr></tbody>
</table>**Parent Topic:**[Governance, Risk, and Compliance reference](../concept/grc-reference.md)

