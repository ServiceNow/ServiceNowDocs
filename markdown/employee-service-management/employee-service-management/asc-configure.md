---
title: Setting up your Alumni Center
description: Set up your Alumni Center so you can communicate with your former employees or non-employees.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Setting up your Alumni Center

Set up your Alumni Center so you can communicate with your former employees or non-employees.

The following plugins must be activated prior to activating the Alumni Center \(sn\_asc\) plugin:

-   Human Resources Scoped App: Core \(com.sn\_hr\_core\)
-   Employee Center \(sn\_ex\_sp\)

For more information on requesting activation of a plugin, see [Request a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_RequestAPlugin.md).

To set up Alumni Center, you must request activation for the following: Explicit Roles \(com.glide.explicit\_roles\). The Alumni Center uses this plugin to help segregate external users from internal users.

**Note:** The Explicit Roles \(com.glide.explicit\_roles\) plugin must be activated before activating the Alumni Center \(sn\_asc\). For information on installing a ServiceNow Store application, see [Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_InstallApplications.md).

-   **Roles installed**

    By activating the Alumni Center \[sn\_asc\] plugin, the following roles install and are required to configure your Alumni Center:

<table id="table_pp1_gvf_tmb"><thead><tr><th>

Alumni Center role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Alumni Center admin \[sn\_asc.admin\]

</td><td>

Lets you configure all aspects of Alumni Center.

</td><td>

-   Role delegator \[role\_delegator\]
-   Skill user \[skill\_user\]
-   Alumni Center manager \[sn\_asc.manager\]
-   Live feed administrator \[live\_feed\_admin\]
-   Chat administrator \[chat\_admin\}
-   Service Portal administrator \[sp\_admin\]
-   Service Catalog administrator \[catalog\_admin\]


</td></tr><tr><td>

Alumni Center Alumni \[sn\_asc.alumni\]

</td><td>

Lets you access Alumni Center as an alumnus.

</td><td>

External Alumni Center user \[snc\_external\]

</td></tr><tr><td>

Alumni Manager \[sn\_asc.manager\]

</td><td>

Lets you manage Alumni Center, which includes alumni records and some of the import process.

</td><td>

Content Delivery manager \[sn\_cd.content\_manager\]

</td></tr></tbody>
</table>-   **Alumni Center – Service Portal configuration update**

    After upgrading the latest platform version or the Alumni Center Store App version, manually update the following three fields in the Alumni Center – Service Portal record to preserve your customizations. These values do not update automatically.

    -   Home page: asc\_home
    -   Main menu: Alumni Center Header
    -   Theme: Alumni Center Coral Theme
    ![Service Portal configuration for Alumni Center](../image/alumni-service-portal-config.png)

-   **Supported task types**

    The base system supports the following task types:

    -   Collect Employee Input
    -   Checklist
    -   E-signature \(HR core only\)
    -   Mark when complete
    -   Take survey
    -   Upload documents
    -   URL
    -   View video
-   **Adding content**

    The Alumni Center uses the same widgets as the HR Service Delivery Employee Center. For more information, see [Employee Center widget instance options](../../employee-center/concept/emp-center-topic-inst-options.md).

    Use Content Publishing to add and display content to your Alumni Center. For more information, see [Content Publishing](../../employee-center/concept/ec-publish-content.md).

    To add content as part of a campaign, use **Content Automation**. For more information, see [Working on Campaigns](../../employee-center/concept/ecpro-campaigns.md).

-   **Load data**

    To add alumni users in bulk, use **System Import Sets**. For more information, see [Import sets key concepts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/c_ImportSetsKeyConcepts.md).

    At a minimum, the file you upload must have a header and the personal email for each alumnus.

    **Note:** Use the Imported Alumni \[sn\_asc\_user\_imp\] table when importing users.

-   **Transform and edit**

    After loading your file:

    -   Transform your import set so that it moves to staging.
    -   Go to **Staged Alumni** to view what was loaded from your file.
    -   You can edit the loaded users, ensure unique user IDs, or approve if they look valid.
    -   From the list view of Staged Alumni, click **Import All Approved** to start the Import Approved Staged to Alumni scheduled job.

