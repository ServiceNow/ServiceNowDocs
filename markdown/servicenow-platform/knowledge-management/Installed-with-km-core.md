---
title: Components installed with Knowledge Management Core
description: Several types of components are installed with activation of the Knowledge Management Core plugin \(com.glideapp.knowledge\) including user roles and tables.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Knowledge Management reference, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Components installed with Knowledge Management Core

Several types of components are installed with activation of the Knowledge Management Core plugin \(com.glideapp.knowledge\) including user roles and tables.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Demo data is available.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Knowledge\[knowledge\]

</td><td>

Users with the knowledge role can contribute to the default knowledge base and access the Knowledge application menu. The knowledge role is a fulfiller role and not a requester role.

</td><td>

None.

</td></tr><tr><td>

Knowledge administrator\[knowledge\_admin\]

</td><td>

Knowledge administrator can create new knowledge bases and manage all knowledge bases.

</td><td>

Knowledge administrator contains the knowledge role.

</td></tr><tr><td>

Knowledge manager\[knowledge\_manager\]

</td><td>

Knowledge managers perform administrative functions for knowledge bases they manage such as defining categories, pinning important articles, and approving changes to articles. Users selected as managers of a knowledge base receive this role automatically.

</td><td>

Knowledge manager contains the knowledge administrator role.

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CSM Table Map\[csm\_table\_map\]

</td><td>

Stores information about the mapping source and target table. For example, while creating a knowledge article from a customer service case, the source table would be customer service case \[sn\_customerservice\_case\] and the target table would be Knowledge \[kb\_knowledge\].

</td></tr><tr><td>

CSM Field Map\[csm\_field\_map\]

</td><td>

Stores information about the fields that are mapped from the source table to the target table in a given table map \(CSM Table Map\). For example, when creating a knowledge article from a customer service case \[sn\_customerservice\_case\], the source field value would be case.short description and the target field value would be knowledge.short description.

</td></tr><tr><td>

Related Articles\[kb\_2\_kb\]

</td><td>

Stores information about related knowledge articles.

</td></tr><tr><td>

Related Catalog Items\[kb\_2\_sc\]

</td><td>

Stores information about related catalog items.

</td></tr><tr><td>

Knowledge Category\[kb\_category\]

</td><td>

Stores the category of a knowledge article.

</td></tr><tr><td>

Knowledge Feedback Task\[kb\_feedback\_task\]

</td><td>

Stores information about the feedback task on a knowledge article.

</td></tr><tr><td>

Knowledge Feedback\[kb\_feedback\]

</td><td>

Stores information about flagged comments on a knowledge article.

</td></tr><tr><td>

Knowledge Keyword\[kb\_keyword\]

</td><td>

Stores information about keywords associated with the featured knowledge articles on the homepage of the Knowledge Management Service Portal.

</td></tr><tr><td>

Knowledge Base\[kb\_knowledge\_base\]

</td><td>

Stores information about knowledge bases that store knowledge articles.

</td></tr><tr><td>

Knowledge keyword\[kb\_knowledge\_keyword\]

</td><td>

Stores information related to mapping between knowledge articles and keywords.

</td></tr><tr><td>

Knowledge\[kb\_knowledge\]

</td><td>

Stores knowledge articles organized by knowledge base and category, as well as featured content and popular articles.

</td></tr><tr><td>

Who Can Contribute To Knowledge Base\[kb\_uc\_can\_contribute\_mtom\]

</td><td>

Stores information about who can read and write to a knowledge base.

</td></tr><tr><td>

Who Can Read Knowledge Base\[kb\_uc\_can\_read\_mtom\]

</td><td>

Stores information about who can read a knowledge base.

</td></tr><tr><td>

Who Cannot Contribute To Knowledge Base\[kb\_uc\_cannot\_contribute\_mtom\]

</td><td>

Stores information about who cannot read and write to a knowledge base.

</td></tr><tr><td>

Who Cannot Read Knowledge Base\[kb\_uc\_cannot\_read\_mtom\]

</td><td>

Stores information about who cannot read a knowledge base.

</td></tr><tr><td>

Knowledge Use\[kb\_use\]

</td><td>

Stores information about the number of times articles are viewed and the number of times knowledge articles are used in an incident, problem, or case.

</td></tr><tr><td>

Knowledge Related to Products\[m2m\_kb\_ci\]

</td><td>

Stores information about the products related to knowledge articles.

</td></tr><tr><td>

Knowledge Comment Likes\[m2m\_kb\_feedback\_likes\]

</td><td>

Stores information about users who like a comment in knowledge feedback.

</td></tr><tr><td>

Knowledge Applied to Tasks\[m2m\_kb\_task\]

</td><td>

Stores information about articles attached to tasks \(incident, case, or problem\).

</td></tr></tbody>
</table>