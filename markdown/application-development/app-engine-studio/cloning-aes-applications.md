---
title: Cloning instances with AES
description: Learn how to protect the data, tables, and templates you've created in App Engine Studio when using System Clone to copy instances from production to non-production.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Cloning instances with AES

Learn how to protect the data, tables, and templates you've created in App Engine Studio when using System Clone to copy instances from production to non-production.

## Preserving data and tables when cloning

The following are requirements for cloning instances with AES:

1.  Ensure that all of your AES plugins are installed across all instances.
2.  If you're cloning a production instance, verify that you've set up a data preserver on the target instances to preserve the Automated Test Framework \(ATF\) and Instance Scan properties. For more information about data preservers, see [Create a clone preserver](https://www.servicenow.com/docs/access?context=create-new-clone-preserver&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and [Create a data preserver \(legacy\)](https://www.servicenow.com/docs/access?context=t_CreateADataPreserver&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

    **Important:** By default, the ATF system property is disabled to prevent you from accidentally running these tests on a production system. Running ATF on a production instance is neither recommended nor supported due to the potential for data corruption or outages.

3.  If you're collecting development and deployment data, the App Engine Management Center \(AEMC\) plugin must be installed on all instances.

Cloning data and tables from a production instance over a non-production instance can overwrite data in your non-production tables. To ensure that data isn't lost in development environments, create a cloning strategy for collaboration.

1.  The following tables have data preservation to ensure that the tables are correctly cloned between instances:

    **Note:** For the following tables, preservation is for global scope only.

    -   Collaboration Descriptor tables:
        -   App Collaboration Descriptors \(sys\_appcollab\_descriptor\)
        -   App Collaboration Descriptor Permissions \(sys\_appcollab\_permission\_m2m\)
    -   Collaboration Users and Groups tables:
        -   App Collaboration Users \(sys\_appcollab\_user\)
        -   App Collaboration Groups \(sys\_appcollab\_group\)
    The data preservation ensures data is retained on the tables in the development instances.

2.  The following tables have clone exclusions:

    -   Collaboration Descriptor tables:
        -   App Collaboration Descriptors \(sys\_appcollab\_descriptor\)
        -   App Collaboration Descriptor Permissions \(sys\_appcollab\_permission\_m2m\)
    -   Collaboration Users and Groups tables:
        -   App Collaboration Users \(sys\_appcollab\_user\)
        -   App Collaboration Groups \(sys\_appcollab\_group\)
    Clone exclusions ensure data from production instances isn't copied to development instances.

3.  If AES is the only application using the Credentials table, consider creating data preservers for Credential Alias, Basic Auth, and Discovery credentials. Otherwise, you must ensure that these tables aren't overwritten when the production instance is cloned to non-production instances.
4.  The following users must be reassigned their roles after cloning:
    -   Users in the AES Users group
    -   Users in the AES User Limited group
    -   Users who have the sn\_app\_eng\_studio.user role in non-production instances
5.  After cloning, a **ReSync Collaborations Permissions** post-clone clean-up script runs automatically, so any applications that were the same on production and development instances are automatically have collaborators synced. Developers can resume development on them immediately.

    **Note:** The cloned instance must have the collaboration plugin enabled.

6.  If some applications were backed up prior to cloning and retrieved after cloning, you can use the **Resync collaboration permissions** related link on the sys\_app record to reassign users and groups to their appropriate delegated development permissions.
7.  If a collaboration descriptor is no longer associated with a user or group after cloning \(in the event that development apps were wiped out during cloning as they were not in the source instance\), select the **Clean up records with empty references** related link to remove the unreferenced user or group from the collaboration table. You should run this UI action after the cloning is done and all preserved applications have been retrieved \(with **Resync collaboration permissions** already run on them\).

The following tables have data preservation to ensure that the tables are correctly cloned between instances:

-   Pipeline Instance
-   Request Authorization Key
-   Deployment Request
-   Deployment Environment Request

## Preserving app templates when cloning

Admins must protect custom templates from being overwritten during the cloning process. Without protection, templates created in AES \(both from existing applications and from scratch\) are in danger of disappearing during a clone.

When you create a template in AES, a scoped app is automatically generated on the Custom Applications \[sys\_app.list\] table in your instance. Though they have different contents, template applications and standard custom applications are treated similarly on the ServiceNow AI Platform. So, preserving app templates during a system clone works the same way as preserving an application.

To protect app templates on your non-production instances, follow the process in [Create a clone preserver](https://www.servicenow.com/docs/access?context=create-new-clone-preserver&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) or [Create a data preserver \(legacy\)](https://www.servicenow.com/docs/access?context=t_CreateADataPreserver&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## More information on cloning and data preservation

See the following topics for more information on cloning and data preservation:

-   For more information on using the System Clone tool, see [Instance Clone](https://www.servicenow.com/docs/access?context=system-clone-landing&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
-   For more information on data preservation, see [Create a clone preserver](https://www.servicenow.com/docs/access?context=create-new-clone-preserver&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
-   For more details on cloning instances with AES, see the App Engine Studio System Administrator Guide on [ServiceNow University](https://learning.servicenow.com/).

<table id="table_m51_zrm_jtb-3"><thead><tr><th>

Learn more about cloning instances with AES

</th><th>

Additional ServiceNow resources

</th></tr></thead><tbody><tr><td rowspan="4">

ServiceNow provides several additional resources on cloning instances with App Engine Studio.

</td><td>

![](../../../reuse/icons/brand-icons/bus-webinar.svg) [Cloning basics knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1214608)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-whitepaper.svg)[Cloning instances tips and tricks knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1214621)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-3-person.svg) [Extensive FAQ knowledge article on cloning instances](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0715621)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-learn.svg) [App Engine Enterprise - Data Preservation During System Clone Whitepaper](https://learning.servicenow.com/nowcreate?id=nc_asset&asset_id=4b22db79479e91185cbdaf44846d43e1)

**Note:** You must log in to ServiceNow University to access this resource.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring App Engine Studio and related apps](aes-setup.md)

