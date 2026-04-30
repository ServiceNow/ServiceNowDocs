---
title: Control access at the knowledge article level through user criteria
description: You specify user criteria for a knowledge article to control which users are granted read access to the knowledge article.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Managing access to knowledge bases and knowledge articles, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Control access at the knowledge article level through user criteria

You specify user criteria for a knowledge article to control which users are granted read access to the knowledge article.

## Before you begin

Role required: knowledge\_manager, knowledge\_admin

**Note:** You may need to configure the form to add **Can Read** and **Cannot Read** fields.

## About this task

Try to use only user criteria, which were introduced in Knowledge Management v3, to control access to knowledge articles. Roles were used for this purpose in Knowledge Management v2. For more information, see [Managing access to knowledge bases and knowledge articles](../concept/user-access-knowledge.md).

**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in a future release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers beginning with the Madrid release. For more information about the new experience, see [Knowledge Management Service Portal homepage features](../concept/knowledge-service-portal-pages.md).

As a knowledge base owner or a manager if the **glide.knowman.apply\_article\_read\_criteria** property is enabled and you don't satisfy the article level user criteria, then the article will not be visible in portal search. To be able to view the article in the portal search, you must configure article level user criteria accordingly.

If you are a part of the ownership group associated with the article then you can see the article in portal search, irrespective of the article level user criteria.

## Procedure

1.  Open a knowledge article.

    **Note:** You can update only the latest version of the knowledge article.

2.  Assign access based on user criteria.

<table id="choicetable_sqz_z3v_qjb"><thead><tr><th align="left" id="d547833e127">

Access

</th><th align="left" id="d547833e130">

Procedure

</th></tr></thead><tbody><tr><td id="d547833e136">

**Allow read access**

</td><td>

In the **Can Read** field, search for and add user criteria. For example, to allow read access to a user, search for a user criteria that the user matches and add it to this field.

</td></tr><tr><td id="d547833e148">

**Deny read access**

</td><td>

In the **Cannot Read** field, search for and add user criteria. For example, to deny read access to a user, search for a user criteria that user matches and add it to this field.**Note:**

-   If users have contribute access to the knowledge base, they also have read access to the knowledge article regardless of the **Cannot Read** setting.

Activate the property \(glide.knowman.apply\_article\_read\_criteria\) to override contribute access to a knowledge article based on **Can Read** and **Cannot Read** user criteria at the article level. For more information, see [Knowledge Management properties](../reference/r_KnowledgeProperties.md#).

-   Users who meet both **Can Read** and **Cannot Read** user criteria are denied read access to the knowledge article. The **Cannot Read** setting overrides the **Can Read** setting for the knowledge article.


</td></tr></tbody>
</table>    **Note:** If the **Can Read** and **Cannot Read** fields aren't visible, configure the Knowledge form to display them. For more information, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

3.  On the Knowledge form, click **Update**, and then click **Publish** to apply the changes.


## What to do next

After you add user criteria, you can use the user criteria diagnostics feature to verify the access users have to a knowledge base or a knowledge article. For more information, see [User criteria diagnostics for Knowledge Management](../concept/diagnose-knowledge-user-criteria.md).

**Important:** After making user criteria additions or changes, you may need to log out and log back in to clear the prior configuration.

**Parent Topic:**[Managing access to knowledge bases and knowledge articles](../concept/user-access-knowledge.md)

**Related topics**  


[Create user criteria for controlling access to knowledge bases and articles](create-user-criteria-record-in-knowledge-management.md)

[Control access at the knowledge base level through user criteria](t_SelectUserCriteria.md)

