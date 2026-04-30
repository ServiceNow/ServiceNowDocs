---
title: Document Intelligence roles
description: Document Intelligence is installed with these roles.Has full access to the Document Intelligence application, except for modifying a subset of system properties, and the billing and internal tables.Has view-only access on Document Intelligence document tasks that they are authorized to view.Extracts information from documents using the Document Intelligence workspace.Extracts information from documents using the Document Intelligence workspace. Also enables users to create Document Intelligence document tasks and submit them for processing.Creates and edits use cases, fields, field groups, and document tasks. Views, measures, and analyzes the usage and effectiveness of Document Intelligence using the Platform Document Intelligence Usage dashboard. Grants access to submit document tasks and interact with the Document Intelligence workspace.
locale: en-US
release: yokohama
product: Document Intelligence
classification: document-intelligence
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Document Intelligence references, Document Intelligence, Enable AI experiences]
---

# Document Intelligence roles

Document Intelligence is installed with these roles.

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and contact your account representative.

**Parent Topic:**[Document Intelligence references](docintel-references.md)

**Related topics**  


[Components installed with Document Intelligence](installed-with-document-intelligence.md)

[Confidence scores](../concept/docintel-confidence-scores.md)

[Data extraction modes](data-extraction-modes.md)

[Data normalization](../concept/data-normalization.md)

[Document field statuses](docintel-field-statuses.md)

[Document Intelligence forms](document-intelligence-forms.md)

[Document Intelligence properties](document-intelligence-properties.md)

[Document Intelligence terminology](../concept/docintel-terminology.md#)

[Document task statuses](docintel-task-statuses.md)

[Domain separation and Document Intelligence](domain-separation-and-doc-intel.md)

[Languages supported by Document Intelligence](../concept/languages-supported-by-document-intelligence.md)

[Limitations in Document Intelligence](hard-limits-in-doc-intel.md)

## DocIntel Admin \[sn\_docintel.admin\]

Has full access to the Document Intelligence application, except for modifying a subset of system properties, and the billing and internal tables.

### Contains Roles

List of roles contained within the role.

-   platform\_ml\_di.admin
-   action\_designer
-   flow\_designer
-   sn\_ace.ace\_user
-   canvas\_user
-   usage\_admin

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

## DocIntel Viewer \[sn\_docintel.viewer\]

Has view-only access on Document Intelligence document tasks that they are authorized to view.

### Contains Roles

List of roles contained within the role.

-   snc\_read\_only
-   platform\_ml\_di.viewer

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

## DocIntel Extraction Agent \[sn\_docintel.extraction\_agent\]

Extracts information from documents using the Document Intelligence workspace.

### Contains Roles

List of roles contained within the role: platform\_ml\_di.extraction\_agent.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

## DocIntel Creation Agent \[sn\_docintel.creation\_agent\]

Extracts information from documents using the Document Intelligence workspace. Also enables users to create Document Intelligence document tasks and submit them for processing.

### Contains Roles

List of roles contained within the role: platform\_ml\_di.creation\_agent.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

## DocIntel Manager \[sn\_docintel.manager\]

Creates and edits use cases, fields, field groups, and document tasks. Views, measures, and analyzes the usage and effectiveness of Document Intelligence using the Platform Document Intelligence Usage dashboard. Grants access to submit document tasks and interact with the Document Intelligence workspace.

### Contains Roles

List of roles contained within the role.

-   platform\_ml\_di.manager
-   action\_designer
-   flow\_designer
-   sn\_ace.ace\_user
-   canvas\_user
-   usage\_admin

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

