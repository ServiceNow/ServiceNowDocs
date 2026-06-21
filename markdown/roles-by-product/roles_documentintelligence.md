---
title: Document Intelligence roles
description: These roles are available for the application
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/roles-by-product/roles\_documentintelligence.html
release: australia
topic_type: reference
last_updated: "2024-03-11"
reading_time_minutes: 1
breadcrumb: [Roles for all products]
---

# Document Intelligence roles

These roles are available for the application

<table><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th><th>

Groups with this role

</th><th>

Special considerations

</th></tr></thead><tbody><tr><td>

DocIntel Admin \[sn\_docintel.admin\]

</td><td>

Has full access to the Document Intelligence application, except for modifying a subset of system properties, and the billing and internal tables.

</td><td>

-   platform\_ml\_di.admin
-   action\_designer
-   flow\_designer
-   sn\_ace.ace\_user
-   canvas\_user
-   usage\_admin

</td><td>

None.

</td><td>

**Important:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

DocIntel Creation Agent \[sn\_docintel.creation\_agent\]

</td><td>

Extracts information from documents using the Document Intelligence workspace. Also enables users to create Document Intelligence document tasks and submit them for processing.

</td><td>

None

</td><td>

None.

</td><td>

**Important:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

DocIntel Extraction Agent \[sn\_docintel.extraction\_agent\]

</td><td>

Extracts information from documents using the Document Intelligence workspace.

</td><td>

None

</td><td>

None.

</td><td>

**Important:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

DocIntel Manager \[sn\_docintel.manager\]

</td><td>

Creates and edits use cases, fields, field groups, and document tasks. Views, measures, and analyzes the usage and effectiveness of Document Intelligence using the Platform Document Intelligence Usage dashboard. Grants access to submit document tasks and interact with the Document Intelligence workspace.

</td><td>

-   platform\_ml\_di.manager
-   action\_designer
-   flow\_designer
-   sn\_ace.ace\_user
-   canvas\_user
-   usage\_admin

</td><td>

None.

</td><td>

**Important:** Avoid granting an admin role when more specialized roles are available.

</td></tr><tr><td>

DocIntel Viewer \[sn\_docintel.viewer\]

</td><td>

Has view-only access on Document Intelligence document tasks that they are authorized to view.

</td><td>

-   snc\_read\_only
-   platform\_ml\_di.viewer

</td><td>

None.

</td><td>

**Important:** Avoid granting an admin role when more specialized roles are available.

</td></tr></tbody>
</table>**Parent Topic:**[Roles for all products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/roles-by-product/roles-for-all-products.md)

