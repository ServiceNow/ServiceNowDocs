---
title: Grant visibility domains to an individual user
description: While it is possible to add visibility domains for specific users on the User form, it's best to add them only via groups. This controls permissions and access should individuals change departments or leave the company.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Expand domain scope, View domain relationships, Domain separation setup and administration, Domain separation for service providers, Access Management]
---

# Grant visibility domains to an individual user

While it is possible to add visibility domains for specific users on the User form, it's best to add them only via groups. This controls permissions and access should individuals change departments or leave the company.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **User**.

2.  Select the user you want to provide with visibility domains.

3.  Add the **Visibility domains** related list to the form.

4.  From the Visibility Domains related list, click **Edit**.

5.  Select the domains whose records you want the user to see.

6.  Click **Save**, and then click **Update**.

    ![](../image/Visibility_domains_user.png)

    The Visibility domain embedded list contains the following fields.

    |Field|Description|
    |-----|-----------|
    |Domain|Domain that is visible to the group or user.|
    |Inherited|Domain is inherited from domain visibility or a parent domain.|
    |Granted By|Name of the group that granted domain visibility.|
    |Parent visibility|Name of the parent domain and used for grouping records. If the parent record is deleted, then all records with the same parent are deleted as well.|


